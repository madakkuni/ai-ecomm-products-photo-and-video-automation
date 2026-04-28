# 🚀 E-Commerce Products Photo & Video Generation

![n8n](https://img.shields.io/badge/n8n-Workflow_Automation-ff6d5a?style=for-the-badge&logo=n8n&logoColor=white)
![Google Vertex AI](https://img.shields.io/badge/Vertex_AI-Gemini_Models-4285F4?style=for-the-badge&logo=googlecloud&logoColor=white)
![AI](https://img.shields.io/badge/AI-Generative_AI-black?style=for-the-badge)
![Automation](https://img.shields.io/badge/Automation-End_to_End-blueviolet?style=for-the-badge)

---

## 📌 Overview

Transform a simple clothing photo into **studio-quality product images AND cinematic short videos** using AI-driven automation.

This project demonstrates an end-to-end workflow built with **n8n**, integrating Google Vertex AI (Gemini models) and generative media APIs to automate fashion product photography and videography.

👉 Upload a basic clothing image → get **high-quality product images + AI-generated model videos**

---

## 🎯 Features

* 📸 Convert low-quality clothing images into professional visuals
* 🤖 AI-generated photorealistic models wearing the product
* 🎬 Generate short-form videos from static images (AI motion + posing)
* 🎭 Automatic generation of multiple scene variations
* 🧠 Meta-prompting for dynamic prompt creation
* 🗂️ Auto folder creation with structured naming (Google Drive)
* 🔄 Fully automated workflow using n8n

---

## ⚙️ Tech Stack

| Component              | Purpose                      |
| ---------------------- | ---------------------------- |
| n8n                    | Workflow orchestration       |
| Google Vertex AI       | AI reasoning + orchestration |
| Gemini 2.5 Pro         | Prompt generation (Brain)    |
| Gemini 2.5 Flash Image | Image generation (Artist)    |
| Google Veo             | Video generation (Director)  |
| Google Drive API       | Storage & organization       |

---

## 🧠 Model Roles in the Workflow

This system uses a **multi-model architecture**:

| Model                  | Role        | Purpose                                     |
| ---------------------- | ----------- | ------------------------------------------- |
| gemini-2.5-pro         | 🧠 Brain    | Prompt generation, analysis, meta-prompting |
| gemini-2.5-flash-image | 🎨 Artist   | Image generation                            |
| Google Veo             | 🎬 Director | Video generation from images                |

👉 Conceptually:
**AI (thinking) → AI (creating images) → AI (creating motion/video)**

---

## 🔄 How It Works

### 1. Input

A simple image of a clothing item (mobile photo works).

---

### 2. Model Generation

AI generates a realistic human model wearing the exact garment.

* Maintains garment accuracy (color, texture, fit)
* Avoids redesign or hallucination

---

### 3. Meta-Prompting (Core Logic)

Instead of writing static prompts, this workflow uses **meta-prompting**.

#### 💡 What is Meta-Prompting?

👉 AI generates prompts for another AI

Instead of:
Human → writes prompt → Image generated

It becomes:
AI → generates prompt → AI → generates image/video

---

### 🧠 Why Meta-Prompting is Important

* 🔄 Handles variety across clothing types
* 🎯 Adds photography domain expertise
* 📈 Scales content creation automatically

---

### 4. Image Generation

#### 🏢 Studio Shots

* Front view
* Side/angle view
* Back view
* Detail close-up

#### 🌆 Lifestyle Shots

* Context-aware environments
* Real-world usage scenarios
* Marketing-ready visuals

---

### 5. 🎬 Video Generation (NEW)

Extends static images into **short cinematic videos**.

**What it does:**

* Generates 8 second model videos
* Adds natural human motion (posing, turning)
* Simulates camera movement (pan, zoom)
* Maintains garment consistency

**Example behaviors:**

* Model rotation (front → side → back)
* Subtle fabric motion
* Lifestyle movement (walking, adjusting outfit)

---

### 6. Storage & Organization

* Creates a unique folder per run
* Uses sequential naming
* Stores images & videos in Google Drive

---

## 🧪 Example Use Cases

* E-commerce product listings
* Fashion catalogs
* Marketplace sellers (Amazon, Shopify)
* Social media content (Reels, Ads)
* Automated marketing pipelines

---

## 📂 n8n Flow

* Upload / Input Node
* Image Processing (Base64 conversion)
* AI Model Generation
* Meta Prompt Generation
* Image Generation API Call
* Convert Base64 → Binary
* Video Generation (Veo API)
* Create Folder (Google Drive)
* Upload Images & Videos

---

## ⚠️ Challenges & Learnings

* Binary vs JSON handling in n8n
* API rate limits (429 errors)
* Maintaining garment accuracy
* Designing reusable prompt pipelines
* Syncing image → video generation

---

## 🚀 Future Improvements

* Real-time preview UI
* Multi-model fallback
* Brand-specific styling
* Batch processing
* Advanced motion control

---

## 🎬 Demo






---

## 🤝 Contributing

Suggestions and improvements are welcome.

---

## 📜 License

MIT License

---

## 🙌 Acknowledgement

Special thanks to @LucasWalterAI for inspiration and insights.
