# llava-cpp-offline 🧠🖼️  
Offline image analysis with LLaVA 1.6 + Visual Studio build  
by **Baris**

This project shows how to compile and run LLaVA locally on Windows – without any API, without cloud, and without Python dependencies.

## 🔥 Features

- Fully offline LLaVA Vision model
- Compiled llama-llava-cli (.exe)
- GGUF model support
- GUI + image understanding
- Python wrapper via `llava_cpp.py`

## 📦 Repository contents

- `llama-llava-cli.exe` → compiled CLI interface for LLaVA
- `llava_cpp.py` → Python wrapper for CLI calls
- `example_usage.py` → test script
- `models/` → place your LLaVA + MMProj models here
- `screenshots/` → test images

## 🧠 Download models

👉 Main model:  
https://huggingface.co/liuhaotian/llava-v1.6-mistral-7b-GGUF

👉 MMProj encoder:  
https://huggingface.co/liuhaotian/llava-v1.6-mistral-7b-GGUF/tree/main/mmproj

Put both files inside the `models/` folder:

## 🐍 Python example

```python
from llava_cpp import analyze_image

response = analyze_image("screenshots/test_gui.png")
print("Response:", response)

