# MAJID A-Z Guide — colibri (Reminder)

> Fork/copy on Majid7692. Original: JustVugg/colibri. Original credit and Apache-2.0 license preserved (see LICENSE). This copy does NOT claim original code was written by Majid7692. Only change so far: this A-Z guide added.

## 1. Ye kya hai?
Tiny engine, immense model. Bahut bare open MoE models ko usi machine par chalata hai jo tumhare paas already hai — har token ke liye model ka sirf chhota hissa use hota hai, wo RAM me rehta hai, baaqi experts disk se parhe jate hain. Pure C, GPU zaroori nahi.

## 2. Benefits
- Bara model, chhoti machine — GPU ke baghair bhi chalta hai; CPU, Vulkan (any GPU), aur CUDA (NVIDIA) support hai.
- 13 engines: language models (GLM-5.2/5.3, Mistral-Large-4, Kimi K3, DeepSeek V4 Flash, MiMo-V2.6, Qwen3.8, Qwen3.6, OLMoE, etc.), image (Qwen-Image-2.1), decision models (Laya, GLiNER2.5-Decide).
- GGUF files jaisi hain waisi hi parhi jati hain.
- Free aur open source.

## 3. Requirements
- Kam se kam 8 GB RAM (16 GB ya zyada behtar).
- Sab se chhote model ke liye 22 GB free disk.
- Internet connection (model download ke liye).
- Graphics card optional hai.

## 4. Install — A to Z
A. Windows: repo download/unzip karo, phir `START-HERE.bat` double-click karo. Python missing ho to wo install offer karega.
B. Linux (Ubuntu/Debian):
   ```
   sudo apt install git python3 build-essential
   git clone https://github.com/JustVugg/colibri
   cd colibri
   ./start-here.sh
   ```
C. macOS (Homebrew):
   ```
   xcode-select --install
   brew install libomp git python
   git clone https://github.com/JustVugg/colibri
   cd colibri
   ./start-here.sh
   ```
D. Ek sawal ka jawab do — kaun sa model — aur Enter dabao.

## 5. First use
- `./coli chat` chalao — example: colibri v2.1.0, GLM-5.2, 744B MoE, int4, streaming CPU, ready in ~32s, resident ~9.9 GB (tumhare machine/model par farq hoga).
- Model choose karte waqt apni RAM/disk dekh kar chhota model lo, bara model zabardasti mat chalao.

## 6. Safety — IMPORTANT
- Is repo me koi personal data, password, ya API key commit NAHI karni.
- Model files bare hote hain — disk full hone se pehle check karo.

## 7. Reminder
- Upstream update aaye to fork sync karo, phir start-here script dobara check karo.
- Agar model slow ho: pehle RAM/disk, phir chhota/quantized model try karo.
