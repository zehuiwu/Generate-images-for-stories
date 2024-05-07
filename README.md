# Generate-images-for-stories

## DEMO
![image](https://github.com/zehuiwu/Generate-images-for-stories/assets/35386051/7cbebb17-ce01-4148-84ae-50763bfca9a1)

## Dataset
Link for our dataset: [dataset](https://drive.google.com/drive/folders/1hjxs5-X9-ES40j6gF1VVLcAw1ROuN2nX?usp=sharing)

## Model Checkpoint
Base Model: [SDXL1.0](https://huggingface.co/stabilityai/stable-diffusion-xl-base-1.0)

LoRA checkpoint: [Chihiro Ogino](https://drive.google.com/file/d/1ZBYxd7YFpYxGkUj3yB6Mj-HHX8KO3XWq/view?usp=drive_link)

## LoRA Training method and config
We use stable diffusion LoRA fine-tuning code from [kohya-ss](https://github.com/kohya-ss/sd-scripts) and the [web UI](https://github.com/bmaltais/kohya_ss) version of it. The training config is in the config file: CO_config.json.

![image](https://github.com/zehuiwu/Generate-images-for-stories/assets/35386051/e0f4b266-e302-4743-a204-a3732a83959b)

## LoRA Inference
To use our LoRA checkpoint, please download the SDXL base model and the LoRA checkpoint mentioned above and use the [AUTOMATIC1111](https://github.com/AUTOMATIC1111/stable-diffusion-webui) stable diffusion web UI. 

![image](https://github.com/zehuiwu/Generate-images-for-stories/assets/35386051/548783e0-122a-48b7-a5f5-79895b46e511)
