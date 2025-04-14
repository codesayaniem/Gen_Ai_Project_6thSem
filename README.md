# 🧠 Question Answering Web Application – Setup Guide

This guide will walk you through the prerequisites, setup, and usage of the QA Web App powered by a custom-trained Transformer-based model and Flask.

---

## ✅ Prerequisites

Ensure the following tools and dependencies are installed on your system:

1. **Visual Studio Code (VS Code)** – for code editing  
2. **Python 3.10+** – preferably Python 3.10 or 3.11  
3. **pip** – Python package installer  
4. **Anaconda (Recommended)** – for Python and virtual environment management

---

## 🧩 Project Structure & Setup

### 1. Create Project Folder

Create a folder named `qa_web_app` and structure it as follows:

```
qa_web_app/
├── app.py
├── model/
│   ├── config.json
│   ├── tokenizer_config.json
│   ├── vocab.txt
│   ├── model.safetensors
│   └── special_tokens_map.json
└── templates/
    └── index.html
```

- Place your **trained model files** inside the `model/` directory.  
- Place your **frontend HTML** (user interface) inside the `templates/` directory.

---

## 🛠️ Environment Setup (Using Anaconda)

### Step 1: Open Anaconda Prompt

Navigate to your project directory:

```bash
cd path\to\qa_web_app
```

### Step 2: Create a Virtual Environment

```bash
conda create -n qaenv python=3.10
```

### Step 3: Activate the Environment

```bash
conda activate qaenv
```

---

## 📦 Install Required Python Libraries

Within the activated environment, install the necessary dependencies:

```bash
pip install flask transformers torch safetensors
```

### 🔧 Optional: Manually Install Missing Dependencies

If you encounter import errors, install the missing libraries individually:

```bash
pip install numpy protobuf packaging requests typing-extensions
```

---

## ▶️ Running the Flask Web Application

To start the web server, run the following command:

```bash
python app.py
```

If successful, you’ll see output similar to:

```
 * Running on http://127.0.0.1:5000/
```

Open the URL in your browser to access the QA interface.

---

## 🌐 Using the QA Web Interface

1. Navigate to: [http://127.0.0.1:5000/](http://127.0.0.1:5000/)  
2. Enter a **context** (e.g., a paragraph of text).  
3. Enter your **question** based on that context.  
4. Click **Submit**.  
5. The model will return an answer based on the given context.
