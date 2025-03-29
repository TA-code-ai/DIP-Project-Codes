# DIP-Project-Codes
This repository contains the complete implementation of my Digital Image Processing course project, which focuses on constructing a Goosefoot weed detection dataset using advanced image processing techniques and synthetic data generation. It includes Jupyter notebooks, datasets, and output results. The project uses ExG and Otsu methods for weed isolation, trains a stable diffusion model for generating synthetic weeds, segments soybean crops using the LeafOnlySAM model, and overlays weed images onto realistic crop backgrounds to create agricultural scenes. The final dataset is used to train a YOLOv12 model for Goosefoot detection
# Code Pipeline
This project introduces a multi-phase methodology for building a dataset for Goosefoot weed detection in soybean fields, utilizing synthetic data generation and advanced image processing techniques:
1.
Initial Dataset and Preprocessing
o
332 images of Goosefoot from the GitHub repository: GitHub - zhangchuanyin/weed-datasets as the primary source.
o
Isolate weeds using Excess Green (ExG) (Woebbecke, 1995) and Otsu’s method (Otsu, 1979) to generate masked weeds placed on black backgrounds.
2.
Synthetic Data Generation
o
Train a stable diffusion model (Rombach R. B., 2022) to generate synthetic weed images, increasing dataset variability and improving model generalization.
3.
Background Image Creation
o
Process soybean field images from the TerraByte Research Group (Beck, 2024).
o
Use the LeafOnlySAM segmentation model (Williams, 2024) to isolate soybean leaves and build a background image library.
4.
Agricultural Scene Synthesis
o
Overlay synthetic and real weed images onto isolated soybean crop backgrounds to create realistic agricultural scenes.
5.
Model Training and Evaluation
o
The final dataset will be split up into training and testing. The YOLOv11 (Khanam, 2024) model will be trained for Goosefoot weed detection and its performance will be evaluated on the testing data using common metrics like accuracy, precision, recall and F1-score.

Evaluated performance using accuracy, precision, recall, and F1-score. 
# Initial Dataset
# Digital Image Processing Techniques
# Stable Diffusion 3.5 Model
# Training Scences
# Training YOLOv12
# Results
