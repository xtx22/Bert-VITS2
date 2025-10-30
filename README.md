```
conda create -n bert-vits2 python=3.11

git clone https://gh-proxy.com/https://github.com/xtx22/Bert-VITS2.git -b Extra-Fix

hf download hfl/chinese-roberta-wwm-ext-large --local-dir bert/chinese-roberta-wwm-ext-large
hf download ku-nlp/deberta-v2-large-japanese-char-wwm --local-dir bert/deberta-v2-large-japanese-char-wwm
hf download microsoft/deberta-v3-large --local-dir bert/deberta-v3-large
hf download microsoft/wavlm-base-plus --local-dir slm/wavlm-base-plus

hf download weslie520/Erlangshen-MegatronBert-1.3B-Chinese --local-dir bert/Erlangshen-MegatronBert-1.3B-Chinese
openi model download Stardust_minus/Bert-VITS2 G2PWModel-v2-onnx --save_path ./g2pW/ --filename g2pW.onnx

openi model download Stardust_minus/Bert-VITS2 Bert-VITS2_中文特化修复底模 --save_path data/cc-voice/models/
openi model download Stardust_minus/Bert-VITS2 clap-htsat-fused --save_path emotional/clap-htsat-fused/

[ -d tarepan-SpeechMOS-ed25eac] || wget https://gh-proxy.com/https://codeload.github.com/tarepan/SpeechMOS/legacy.zip/refs/tags/v1.2.0 -O tarepan-SpeechMOS-ed25eac.tar.gz && tar zxvf tarepan-SpeechMOS-ed25eac.tar.gz
[ -d /root/.cache/torch/hub/tarepan_SpeechMOS_v1.2.0 ] || mv tarepan-SpeechMOS-ed25eac /root/.cache/torch/hub/tarepan_SpeechMOS_v1.2.0
[ -f /root/.cache/torch/hub/checkpoints/utmos22_strong_step7459_v1.pt ] || wget https://gh-proxy.com/https://github.com/tarepan/SpeechMOS/releases/download/v1.0.0/utmos22_strong_step7459_v1.pt -O /root/.cache/torch/hub/checkpoints/utmos22_strong_step7459_v1.pt
```
