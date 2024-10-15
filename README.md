# ScriptIdentification
ScriptIdentification is designed to identify the script (language) of text within images from natural scenes. This repository includes the inference code and models needed for prediction. Each model is structured as a triplet, with Hindi and English as common languages alongside a third language listed below. 

## Installation
Create a conda environment and install the dependencies.
```
conda create -n scriptdetect python=3.9 -y
conda activate scriptdetect

conda install pytorch==2.3.1 torchvision==0.18.1 torchaudio==2.3.1 pytorch-cuda=11.8 -c pytorch -c nvidia
pip install openai-clip==1.0.1
```

## Inference
Download the models and save them to a particular location.
```
wget -O model.zip "https://github.com/username/repository/releases/download/tag/model.zip"
mkdir models
unzip model.zip -d models

```

Script detection can be done using ```infer.py``` with an image as input.

```
python infer.py demo_images/D_image_149_9.jpg hinengodi
#{'predicted_class': 'odia'}
```
Simply replace ```demo_images/D_image_149_9.jpg``` with your image path and ```hinengodi``` with the model name for desired language detection.


## Supported Languages
Each model includes Hindi and English, with the third language varying as follows:

- hineng: Hindi, English
- hinengasm: Hindi, English, Assamese
- hinengben: Hindi, English, Bengali
- hinengguj: Hindi, English, Gujarati
- hinengkan: Hindi, English, Kannada
- hinengmal: Hindi, English, Malayalam
- hinengmar: Hindi, English, Marathi
- hinengmei: Hindi, English, Meitei
- hinengodi: Hindi, English, Odia
- hinengpun: Hindi, English, Punjabi
- hinengtam: Hindi, English, Tamil
- hinengtel: Hindi, English, Telugu
- hinengurd: Hindi, English, Urdu