# Generate-images-for-stories

## Code Rview
For code review of each other's work, we work on our own part of the project, and coordinate on the overall progress during each week's group meeting. We all contribute enough effort to this project. 

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

## ControlNet

To run the ControlNet module, run through the notebook, and call the appropriate following class functions to generate background:

    - generate_image_from_sketch(image_path, prompt, outfile)  
    - generate_image_from_sample(image_path, prompt, outfile)

To modify between conditioning checkpoints, modify the class initialization parameter to the desired detector (scribble or mlsd)

Sources for conditioning Checkpoints: 
[M-LSD](https://huggingface.co/lllyasviel/sd-controlnet-mlsd), 
[HED](https://huggingface.co/lllyasviel/sd-controlnet-hed), 
[Scribble](https://huggingface.co/lllyasviel/sd-controlnet-scribble)

## Style Transfer Experiments
The code for training CycleGAN and running style transfer on pretrained CartoonGAN and AnimeGAN are located in the jupyter notebooks. For CycleGAN, we modified the stucture of the model by adjusting the number of attention layers and the size of the attention layer. We also manipulated the hyperparameters including learning rate and batch size to optimize the generated images.

For CartoonGAN and AnimeGAN, we fed testing images to the pre-trained Hayao and Shinkai style models, and obtained the transferred images.

Source code for CartoonGAN:
https://github.com/FilipAndersson245/cartoon-gan

Source code for AnimeGAN:
https://github.com/TachibanaYoshino/AnimeGANv3

Source code for CycleGAN:
https://github.com/junyanz/CycleGAN

