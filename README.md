# Universal i2v Enhanced Prompt Generator

Universal i2v Enhanced Prompt Generator is a Python-based desktop and web tool for generating structured image-to-video prompts. It combines a Tkinter Py GUI with a Gradio WebUI, allowing users to analyze a reference image, generate environment-aware prompt components, recommend the best camera shot genres, automatically build multiple action-camera motion plans, score them for coherence, and generate a final Universal i2v prompt for video generation workflows.

## 中文简介

Universal i2v Enhanced Prompt Generator 是一个基于 Python 的图生视频提示词生成工具，结合 Py GUI 与 Gradio WebUI。  
它可以根据参考图片进行场景分析，自动推荐 5 个最佳镜头流派，生成多套动作与镜头组合方案，并根据动作冲突与连贯性进行评分，最后输出适合 Universal i2v / LTX 类图生视频工作流使用的完整 Prompt。

---

## Features

- Tkinter-based desktop GUI
- Gradio-based WebUI for browser and mobile access
- Reference image input
- AI scene analysis fields
- Environment tag selection
- Lighting preset selection
- Top 5 camera shot genre recommendation
- Click-style multi-select camera genre selection
- Automatic generation of 5 action-camera motion plans
- Action compatibility scoring
- Collision checking for action combinations
- Universal i2v prompt generation
- Negative prompt generation
- Segmented prompt template generation
- One-click copy for Universal i2v prompt
- Py GUI and Py WebUI can run at the same time
- WebUI can be opened and closed from the GUI

---

## Project Structure

```text
universal-i2v-enhanced-prompt-generator/
│
├─ Universal_i2v_Enhanced_Prompt_v11_webui_auto5_checkbox_copy_guiweb_control_FIXED.py
│  Main application file. Includes Tkinter GUI, Gradio WebUI, scene analysis,
│  camera genre recommendation, action pack generation, scoring, and prompt output.
│
├─ README.md
│  Project documentation.
│
├─ requirements.txt
│  Python dependencies.
│
├─ .gitignore
│  Git ignore rules for cache, models, logs, databases, secrets, and local files.
│
├─ env_config.json
│  Optional custom environment tag configuration.
│
├─ hf_models/
│  Local Hugging Face model cache. Do not upload this folder to GitHub.
│
├─ logs/
│  Runtime logs. Do not upload.
│
├─ temp/
│  Temporary files. Do not upload.
│
└─ screenshots/
   Optional safe screenshots for README.