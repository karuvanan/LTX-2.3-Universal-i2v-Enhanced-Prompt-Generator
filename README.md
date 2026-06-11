# LTX-2.3 Universal i2v Enhanced Prompt Generator

Universal i2v Enhanced Prompt Generator is a Python-based desktop and web tool for generating structured image-to-video prompts. It combines a Tkinter Py GUI with a Gradio WebUI, allowing users to analyze a reference image, generate environment-aware prompt components, recommend the best camera shot genres, automatically build multiple action-camera motion plans, score them for coherence, and generate a final Universal i2v prompt for video generation workflows.

## 中文简介

LTX-2.3 Universal i2v Enhanced Prompt Generator 是一个基于 Python 的图生视频提示词生成工具，结合 Py GUI 与 Gradio WebUI。  
它可以根据参考图片进行场景分析，自动推荐 5 个最佳镜头流派，生成多套动作与镜头组合方案，并根据动作冲突与连贯性进行评分，最后输出适合 Universal i2v / LTX 类图生视频工作流使用的完整 Prompt。

---
PY GUI

https://github.com/user-attachments/assets/887c506d-40e9-4ea3-a5c9-cef530295bdd


WEBUI

https://github.com/user-attachments/assets/d7bce2a5-a024-411e-8c1d-1246fab320f0



## 当前项目功能可以整理成：

1. Py GUI 桌面界面
   - 使用 Tkinter 构建传统桌面 GUI。
   - 包含 Prompt Generator、Config & Nodes、Negative & Segments、Action & Camera、AI Scene Analyzer 等 Tab。

2. Gradio WebUI
   - 通过浏览器 / 手机访问。
   - 支持上传参考图片。
   - 支持分析图片场景。
   - 支持显示 AI 场景描述、构图、光影和环境标签。
   - 支持生成 Universal i2v Prompt。

3. AI Scene Analysis
   - 根据参考图生成场景描述。
   - 分析构图类型。
   - 分析光影方向和环境特征。
   - 推荐适合的环境标签。

4. Top 5 Best Shot Genres
   - 根据图片分析结果推荐 5 个最佳镜头流派。
   - WebUI 中以点击式选择呈现。

5. Action & Camera Compatibility Matrix
   - 内置镜头流派与动作兼容矩阵。
   - 根据用户选择的镜头流派自动推荐动作。

6. 自动生成 5 套动作方案
   - 根据所选流派生成多套动作组合。
   - 自动检测动作冲突。
   - 自动评分。
   - 输出 Top 5 动作方案。

7. 点击式多选
   - AI 推荐的 5 个最佳镜头流派支持点击式选择。
   - 最终动作方案支持点击式选择。
   - 类似 Custom Environments 的 CheckboxGroup 效果。

8. Universal i2v Prompt 生成
   - 合并参考图分析、环境标签、光影、镜头、动作方案。
   - 输出正向 Prompt。
   - 输出 Negative Prompt。
   - 输出 Segmented Prompt Template。

9. 一键复制 Prompt
   - WebUI 支持一键 Copy Universal i2v Prompt。

10. Py GUI 与 Py WebUI 同时运行
   - 可以同时打开桌面 GUI 和网页 WebUI。
   - 可以从 GUI 控制打开 / 关闭 WebUI。

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

## 当前项目主要文件和文件夹说明

根据当前已知文件，建议项目结构整理成这样：
```text
universal-i2v-enhanced-prompt-generator/
│
├─ Universal_i2v_Enhanced_Prompt_v11_webui_auto5_checkbox_copy_guiweb_control_FIXED.py
│  主程序文件。包含 Tkinter Py GUI、Gradio WebUI、AI 场景分析、镜头流派推荐、动作方案自动生成、Prompt 输出等核心逻辑。
│
├─ README.md
│  GitHub 项目说明文件。
│
├─ requirements.txt
│  Python 依赖包列表。
│
├─ .gitignore
│  Git 忽略规则，防止上传缓存、模型、日志、数据库、密码等敏感文件。
│
├─ env_config.json
│  可选。自定义环境标签配置文件。如果里面没有敏感资料，可以上传；如果包含私人项目配置，建议忽略或提供 env_config.example.json。
│
├─ hf_models/
│  本地 Hugging Face 模型缓存目录。不要上传 GitHub。
│
├─ logs/
│  日志目录。不要上传 GitHub。
│
├─ temp/
│  临时文件目录。不要上传 GitHub。
│
├─ output/
│  输出结果目录。如果包含生成图片、视频、客户资料，不要上传 GitHub。
│
└─ screenshots/
   可选。README 用的界面截图。如果没有敏感内容，可以上传。

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
```

## 安装步骤 step by step
Step 1：安装 Python

到 Python 官网安装 Python 3.10 或 3.11。

## 安装时必须勾选：

Add Python to PATH

## 检查：

py --version
Step 2：安装 Git for Windows

## 安装后检查：

git --version
Step 3：打开项目文件夹

## 例如你的项目在：

D:\comfui ui and sulphur

## 在 VS Code 打开这个文件夹。

或者 CMD：

cd /d "D:\comfui ui and sulphur"
Step 4：创建虚拟环境
py -m venv .venv

## 启用虚拟环境：

.venv\Scripts\activate
Step 5：安装依赖

如果已有 requirements.txt：

pip install -r requirements.txt

如果还没有，可以先手动安装：

pip install gradio Pillow transformers torch huggingface_hub opencv-python numpy
## Step 6：运行项目
py "main.py"

## 运行后应该可以同时使用：

Py GUI 桌面窗口
Gradio WebUI 浏览器页面
