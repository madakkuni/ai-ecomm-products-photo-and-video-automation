# 🚀 E-Commerce Products Photo & Video Generation


![n8n](https://img.shields.io/badge/n8n-Workflow_Automation-ff6d5a?style=for-the-badge&logo=n8n&logoColor=white)
![Google Vertex AI](https://img.shields.io/badge/Vertex_AI-Gemini_Models-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![AI](https://img.shields.io/badge/AI-Generative_AI-black?style=for-the-badge)
![Automation](https://img.shields.io/badge/Automation-End_to_End-blueviolet?style=for-the-badge)

Transform a simple clothing photo into studio-quality product images AND cinematic short videos using AI-driven automation.

This project demonstrates an end-to-end workflow built with n8n, integrating Google Vertex AI (Gemini models) and generative media APIs to automate fashion product photography and videography.

---

📌 Overview

E-commerce businesses often rely on expensive photoshoots and manual editing.
This workflow replaces that with an automated, scalable AI pipeline:

👉 Upload a basic clothing image → get high-quality product images + AI-generated model videos

🎯 Features

📸 Convert low-quality clothing images into professional visuals
🤖 AI-generated photorealistic models wearing the product
🎬 Generate short-form videos from static images (AI motion + posing)
🎭 Automatic generation of multiple scene variations
🧠 Meta-prompting for dynamic prompt creation
🗂️ Auto folder creation with structured naming (Google Drive)
🔄 Fully automated workflow using n8n

⚙️ Tech Stack
Component	Purpose
n8n	Workflow orchestration
Google Vertex AI	AI reasoning + orchestration
Gemini 2.5 Pro	Prompt generation (Brain)
Gemini 2.5 Flash Image	Image generation (Artist)
Google Veo	Video generation (Director)
Google Drive API	Storage & organization
🧠 Model Roles in the Workflow

This system uses a multi-model architecture:

Model	Role	Purpose
gemini-2.5-pro	🧠 Brain	Prompt generation, analysis, meta-prompting
gemini-2.5-flash-image	🎨 Artist	Image generation
Google Veo	🎬 Director	Video generation from images

👉 Conceptually:
AI (thinking) → AI (creating images) → AI (creating motion/video)

One model decides what to create
Another generates visuals
Another brings it to life with motion

This separation improves quality, realism, and scalability.

🧠 Workflow Architecture

(Add architecture diagram here — strongly recommended)

🔄 How It Works
1. Input

A simple image of a clothing item (mobile photo works).

2. Model Generation

AI generates a realistic human model wearing the exact garment.

Maintains garment accuracy (color, texture, fit)
Avoids redesign or hallucination
3. Meta-Prompting (Core Logic)

Instead of writing static prompts, this workflow uses meta-prompting.

💡 What is Meta-Prompting?

👉 AI generates prompts for another AI

Instead of:
Human → writes prompt → Image generated

It becomes:

AI → generates prompt → AI → generates image/video

🧠 Why Meta-Prompting is Important

🔄 Handles Variety
Works across jeans, shirts, jackets, etc.

🎯 Adds Domain Expertise
Uses photography concepts (lighting, angles, composition)

📈 Scales Content Creation
Generates multiple scene ideas instantly

4. Image Generation

Two categories of outputs:

🏢 Studio Shots
Front view
Side/angle view
Back view
Detail close-up
🌆 Lifestyle Shots
Context-aware environments
Real-world usage scenarios
Marketing-ready visuals
5. 🎬 Video Generation (NEW 🔥)

Using Google Veo, the workflow extends static images into short cinematic videos.

What it does:
Generates 8–10 second model videos
Adds natural human motion (posing, turning, subtle movement)
Simulates camera motion (pan, zoom, angle shifts)
Maintains garment consistency
Example video behaviors:
Model slowly turning (front → side → back)
Light fabric motion simulation
Lifestyle motion (walking, adjusting outfit)

👉 This turns static product listings into high-engagement content

6. Storage & Organization
Creates a unique folder per run
Uses sequential naming
Stores all generated images & videos in Google Drive
🧪 Example Use Cases
E-commerce product listings
Fashion catalogs
Marketplace sellers (Amazon, Shopify, etc.)
Social media content generation (Reels, Ads)
Automated marketing pipelines
📂 Project Structure (Enhanced)
ecom-ai-photoshoot/
│
├── 📁 workflows/
│   ├── image-generation.json
│   ├── video-generation-veo.json
│   └── master-pipeline.json
│
├── 📁 prompts/
│   ├── meta-prompts/
│   │   ├── base-meta.txt
│   │   └── fashion-meta.txt
│   │
│   ├── image-prompts/
│   │   ├── studio.txt
│   │   ├── lifestyle.txt
│   │   └── pose.txt
│   │
│   └── video-prompts/
│       ├── veo-motion.txt
│       └── camera-behavior.txt
│
├── 📁 config/
│   ├── env.example
│   ├── vertex-config.json
│   └── model-config.json
│
├── 📁 scripts/
│   ├── base64-utils.js
│   ├── retry-handler.js
│   └── naming-utils.js
│
├── 📁 samples/
│   ├── inputs/
│   ├── outputs/images/
│   └── outputs/videos/
│
├── 📁 docs/
│   ├── architecture.md
│   ├── workflow.md
│   └── veo-integration.md
│
├── 📁 assets/
│   ├── demo.gif
│   ├── architecture.png
│   └── preview.png
│
├── README.md
└── LICENSE
📂 Project Structure (n8n Flow)
Upload / Input Node
Image Processing (Base64 conversion)
AI Model Generation
Meta Prompt Generation
Image Generation API Call
Convert Base64 → Binary
Video Generation (Veo API call)
Create Folder (Google Drive)
Upload Images & Videos
⚠️ Challenges & Learnings
Handling binary vs JSON data flow in n8n
Managing rate limits (429 errors) in AI APIs
Ensuring exact garment consistency in generated images
Designing robust and reusable prompt pipelines
Synchronizing image → video pipeline timing
🚀 Future Improvements
Real-time preview UI
Multi-model fallback strategy
Style personalization (brand-specific looks)
Batch processing at scale
Fine-tuned motion control for videos
🎬 Demo


🤝 Contributing

This project is part of ongoing experimentation and learning.
Suggestions, improvements, and ideas are welcome.

📜 License

MIT License (or update as needed)

🙌 Acknowledgement

Special thanks to @LucasWalterAI for sharing insights and workflows that inspired this project.
This implementation was built and customized as part of my own learning and development.
