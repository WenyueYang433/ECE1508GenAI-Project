# ECE1508GenAI-Project

Topic: C-3 Text-guided Image Editing through Latent Modification in VAEs.

Group Members: Lingyun Guo, Ruizhi Niu, Wenyue Yang, Yile Ji



## The team has currently tried two implementation methods:
1. Training a CVAE model with CLIP-generated text features jointly with the original images, enabling the model to perform semantic image editing. This method was inspired by [6]. 
2. Using a pre-trained VAE model, we perform latent-space editing by linear shift, interpolation and latent optimization.


## Operating environment and deployment:
All the codes were completed using Colab, upload the notebook files to Colab and it will be ready to run. If it is running locally, check the "Install" section at the top of the main notebook file.

You can also view the input-output in /notebook.

## Document Description:
| File Path                             | Type            | Description |
|--------------------------------------|-----------------|-------------|
| `/notebook/CVAE.ipynb`                    | Main Notebook   | Implements the CVAE + CLIP method for latent-guided image editing. Includes all outputs. |
| `/notebook/Pretrain_VAE.ipynb`            | Main Notebook   | Implements AutoencoderKL and integrates all latent editing methods:<br>**linear shift**, **interpolation**, and **latent optimization**. |
| `/trained_model/conv_vae_512_64.pth` | Model Checkpoint| A trained **CVAE** model with input image size **64×64**. |
| `/notebook/Interpolation.ipynb`          | Editing Method  | Attempts latent vector editing using **interpolation**. <br>_Integrated into `Pretrain_VAE.ipynb`._ |
| `/notebook/Latent_Optimization_4.ipynb`  | Editing Method  | Attempts latent vector editing using **latent optimization**. <br>_Integrated into `Pretrain_VAE.ipynb`._ |
| `/notebook/Linear_Shift.ipynb`           | Editing Method  | Attempts latent vector editing using **linear shift**. <br>_Integrated into `Pretrain_VAE.ipynb`._ |

# References
[1] D. P. Kingma and M. Welling, “An introduction to variational autoencoders,” Foundations and Trends® in Machine Learning, vol. 12, no. 4, p. 307–392, 2019.

[2] K. Sohn, H. Lee, and X. Yan, “Learning structured output representation using deep condi-tional generative models,” in Advances in Neural Information Processing Systems (C. Cortes,N. Lawrence, D. Lee, M. Sugiyama, and R. Garnett, eds.), vol. 28, Curran Associates, Inc., 2015.

[3] A. Radford, J. W. Kim, C. Hallacy, A. Ramesh, G. Goh, S. Agarwal, G. Sastry, A. Askell,P. Mishkin, J. Clark, G. Krueger, and I. Sutskever, “Learning transferable visual models fromnatural language supervision,” 2021.

[4] D. P. Kingma and M. Welling, “Auto-encoding variational bayes,” 2022.

[5] C. Szegedy, S. Ioffe, V. Vanhoucke, and A. Alemi, “Inception-v4, inception-resnet and the impact of residual connections on learning,” 2016.

[6] Meanna, “Cvae_conv.” https://github.com/meanna/CVAE_CONV, 2023. Accessed: 2025-08-09.

[7] O. Patashnik, Z. Wu, E. Shechtman, D. Cohen-Or, and D. Lischinski, “Styleclip: Text-driven manipulation of stylegan imagery,” 2021.
