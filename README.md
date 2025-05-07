# 🛋️ Sketch-to-Image Furniture Generation

Generate realistic furniture images from hand-drawn sketches using ControlNet and Stable Diffusion.

# 📌 Overview

This project implements a sketch-to-image generation system tailored for furniture design. By leveraging ControlNet with Stable Diffusion, the model can turn simple hand-drawn furniture sketches into realistic image.

# ✨ Features

- 🎨 Sketch-to-Photorealism – Generate realistic furniture images from basic hand-drawn sketches.
- 🧠 Diffusion-Based Architecture – Powered by Stable Diffusion + ControlNet for high-quality and controllable outputs.
- 🔁 Augmented Training – Advanced image augmentations to improve model generalization.
- 🧰 Modular Pipeline – Easy-to-modify structure for training, evaluation, and inference.
- 🗣️ Prompt Engineering – Uses fine-tuned text prompts to direct generation quality and detail.

# 🧱 Dataset Structure
- 📁 Paired dataset with:
  
    - `*_drawn.png` - Sketches of furniture
    - `*_original.png` - Matching photorealistic images

# 🧠 Technical Approach

The system is based on a Conditional Diffusion Model architecture:
- Base Model: Stable Diffusion v1.5
- Conditioning: ControlNet conditions the diffusion process on sketches
- Training: Fine-tuned using paired sketch-photo data and prompt engineering
- Data Pipeline: Normalization, augmentation, and train/val/test split
- Components: VAE, UNET, CLIP (Text Encoder), ControlNet Module

# 🛠️ What Happens During Training?

This script performs the following steps automatically:
1. 📁 Data Processing
   
     It normalizes the sketches and photos, organizes them into training, validation, and test splits, and ensures everything is prepped for the model.
3. 🧠 Model Initialization
   
     Loads a pre-trained Stable Diffusion backbone and applies the ControlNet conditioning layers.
5. 🚂 Training Begins
   
     The model is fine-tuned using dataset. It learns to generate high-quality furniture images guided by the structure and content of sketches.
7. 💾 Progress Tracking
   
     Throughout training, it saves checkpoints, logs progress, and generates intermediate samples so you can monitor how well your model is doing.

# 📊 Results

The model successfully transforms rough furniture sketches into realistic, high-quality images that closely resemble the intended designs. This section highlights the model's performance and the kind of outputs you can expect after training.

###  🖼️ Visual Examples
Each result is composed of:
- ✏️ Input Sketch – A hand-drawn outline of the furniture
- 🧠 Generated Image – The model's photorealistic rendering
- 📷 Target Image – The actual reference photo used for training

These comparisons are saved in the inference_results/ folder, making it easy to track model improvements and benchmark quality.

###  ⚙️ Performance Notes
- Visual Fidelity: The model captures fine furniture details such as legs, armrests, and textures.
- Prompt Responsiveness: When paired with descriptive prompts, it adapts styles (e.g., modern, rustic) with impressive accuracy.
- Consistency: Maintains shape consistency across varying sketch qualities due to strong ControlNet guidance.

###  🧪 Sample Comparison
  ![image](https://github.com/user-attachments/assets/4aa3a851-d867-4513-8797-34d9634198af)
  ![image](https://github.com/user-attachments/assets/e20e9c7c-c3a3-4dd8-95d8-f7eaedb3169e)

# 🐞 Known Issues
- The model usually take several hours to train .
- Some images may have slight color inconsistencies due to model limitations.

# 📈 Future Improvements

- Make UI to visualize generated images from sketches
- Adding more diverse sketch styles

## 👥 Team
**Done by Suhani Pandey** 
