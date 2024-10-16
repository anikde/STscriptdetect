# Script Identification
Script Identification is designed to identify the script (language) of text within images from natural scenes. This repository includes the inference code and models needed for prediction. Each model is structured as a triplet, with Hindi and English as common languages alongside a third language listed below. 

## Installation
Create a conda environment and install the dependencies.
```
conda create -n scriptdetect python=3.9 -y
conda activate scriptdetect

conda install pytorch==2.3.1 torchvision==0.18.1 torchaudio==2.3.1 pytorch-cuda=11.8 -c pytorch -c nvidia
pip install openai-clip==1.0.1
```

## Inference
To get started, clone the repository and make "models" direcotory so that model gets downloaded as we inference script.
```
git clone https://github.com/anikde/STscriptdetect.git
cd STscriptdetect
mkdir models
```

Script detection can be done using ```infer.py``` on a single image as input.

```python
python infer.py --image_path demo_images/D_image_149_9.jpg hinengodi
# {'predicted_class': 'odia'}
```
Simply replace ```demo_images/D_image_149_9.jpg``` with your image path and ```hinengodi``` with the model name for desired language detection.

To process a batch of images
```python
python infer.py --image_dir demo_images/ hinengodi --batch
# {'A_image_101_1.jpg': 'english', 'A_image_72_3.jpg': 'hindi', 'D_image_149_9.jpg': 'odia'}
```
using the ```image_dir``` and ```--batch``` argument predictions can be made on a batch of images.


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
