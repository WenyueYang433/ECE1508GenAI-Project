# ECE1508GenAI-Project

Topic: C-3 Text-guided Image Editing through Latent Modification in VAEs.

Group Members: Lingyun Guo, Ruizhi Niu, Wenyue Yang, Yile Ji


The team has currently tried two implementation methods:
1. Training a CVAE model with CLIP-generated text features jointly with the original images, enabling the model to perform semantic image editing.
2. Using a pre-trained VAE model, we perform latent-space editing by computing direction vectors, which allows us to achieve image editing through image.


Document Description:
1. notebook/ECE1508_GENAI_CVAE.ipynb: The implementation code of CVAE
2. TODO:Pretrain_VAE, Modification of the latent space
3. trained_model/: It contains the pre-trained model parameters for images of sizes 64 and 128 respectively.
