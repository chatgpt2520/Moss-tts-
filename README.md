this one click colab (https://colab.research.google.com/drive/1sjdsCzGdzDLv6Gj3Gzt4wsfwgPLqx0DP?usp=sharing)

more about this model https://github.com/OpenMOSS/MOSS-TTS/tree/main

also this cell codes 
1 cell !git clone https://github.com/OpenMOSS/MOSS-TTS.git
%cd MOSS-TTS
2 cell !pip install --extra-index-url https://download.pytorch.org/whl/cu128 -e ".[torch-runtime]"
3 cell !pip uninstall -y torchvision

!pip install torchvision==0.24.1+cu128 \
  --extra-index-url https://download.pytorch.org/whl/cu128
  4 cell %cd /content/MOSS-TTS

!python clis/moss_tts_local_v1.5_app.py \
  --codec-weight-dtype bf16 \
  --codec-compute-dtype bf16 \
  --no-warmup \
  --no-preload

 optional cell 5 
 this one just creating new url thats run your ui
 
cell 5 from google.colab.output import eval_js
print(eval_js("google.colab.kernel.proxyPort(7861)")) 

if i doing any mistake fix them or suggest me to fix 
