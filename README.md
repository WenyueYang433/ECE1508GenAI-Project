# ECE1508GenAI-Project

Topic: C-3 Text-guided Image Editing through Latent Modification in VAEs.

Group Members: Lingyun Guo, Ruizhi Niu, Wenyue Yang, Yile Ji



## The team has currently tried two implementation methods:
1. Training a CVAE model with CLIP-generated text features jointly with the original images, enabling the model to perform semantic image editing.
2. Using a pre-trained VAE model, we perform latent-space editing by linear shift, interpolation and latent optimization.


## Operating environment and deployment:
All the codes were completed using Colab, upload the notebook files to Colab and it will be ready to run.
You can also view the output in /notebook.

## Document Description:
| File Path                             | Type            | Description |
|--------------------------------------|-----------------|-------------|
| `/src/CVAE.ipynb`                    | Main Notebook   | Implements the CVAE + CLIP method for latent-guided image editing. Includes all outputs. |
| `/src/Pretrain_VAE.ipynb`            | Main Notebook   | Implements AutoencoderKL and integrates all latent editing methods:<br>**linear shift**, **interpolation**, and **latent optimization**. |
| `/trained_model/conv_vae_512_64.pth` | Model Checkpoint| A trained **CVAE** model with input image size **64×64**. |
| `/src/Interpolation.ipynb`          | Editing Method  | Attempts latent vector editing using **interpolation**. <br>_Integrated into `Pretrain_VAE.ipynb`._ |
| `/src/Latent_Optimization_4.ipynb`  | Editing Method  | Attempts latent vector editing using **latent optimization**. <br>_Integrated into `Pretrain_VAE.ipynb`._ |
| `/src/Linear_Shift.ipynb`           | Editing Method  | Attempts latent vector editing using **linear shift**. <br>_Integrated into `Pretrain_VAE.ipynb`._ |
