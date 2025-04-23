# DIP-Project-Codes
This repository contains the complete implementation of my Digital Image Processing course project, which focuses on constructing a Goosefoot weed https://foragingguru.com/goosefoot-plant/ detection dataset using advanced image processing techniques and synthetic data generation. It includes Jupyter notebooks, datasets, and output results. The project uses ExG and Otsu methods for weed isolation, trains a stable diffusion 3.5 model (https://github.com/Stability-AI/sd3.5) for generating synthetic weeds, segments soybean crops using the LeafOnlySAM model (https://github.com/Dom3442/leafonlysam), and overlays weed images onto realistic crop backgrounds to create agricultural scenes. The final dataset is used to train a YOLOv12 model (https://github.com/sunsmarterjie/yolov12) for Goosefoot detection
## 🔄 Code Pipeline

This project introduces a multi-phase methodology for building a dataset for Goosefoot weed detection in soybean fields, utilizing synthetic data generation and advanced image processing techniques:

1. **Initial Dataset and Preprocessing**  
   - 332 images of Goosefoot from the GitHub repository: [zhangchuanyin/weed-datasets](https://github.com/zhangchuanyin/weed-datasets) as the primary source.  
   - Isolate weeds using Excess Green (ExG) ([Woebbecke, 1995](https://doi.org/10.13031/2013.27838)) and Otsu’s method ([Otsu, 1979](https://ieeexplore.ieee.org/document/4310076)) to generate masked weeds placed on black backgrounds.

2. **Synthetic Data Generation**  
   - Train a stable diffusion model ([Rombach R. B., 2022](https://arxiv.org/abs/2112.10752)) to generate synthetic weed images, increasing dataset variability and improving model generalization.

3. **Background Image Creation**  
   - Process soybean field images from the [TerraByte Research Group](https://terrabyte.acs.uwinnipeg.ca/index.html) ([Beck, 2024](https://example.com)).  
   - Use the LeafOnlySAM segmentation model ([Williams, 2024](https://doi.org/10.1016/j.atech.2024.100515)) to isolate soybean leaves and build a background image library.

4. **Agricultural Scene Synthesis**  
   - Overlay synthetic and real weed images onto isolated soybean crop backgrounds to create realistic agricultural scenes.

5. **Model Training and Evaluation**  
   - The final dataset will be split into training and testing. The YOLOv12 ([Khanam, 2024](https://example.com)) model will be trained for Goosefoot weed detection and its performance will be evaluated on the testing data using common metrics like **accuracy**, **precision**, **recall**, and **mAP@0.5**.
 
# Initial Dataset
332 images of Goosefoot weed were used from the GitHub repository: [zhangchuanyin/weed-datasets](https://github.com/zhangchuanyin/weed-datasets) as the primary source.
![Goosefoot Sample](images/goosefoot_sample.png)

# Digital Image Processing Techniques
The provided Python script performs weed isolation using a combination of image processing techniques. It processes a batch of Goosefoot weed images and removes background noise to create clean, black-background images suitable for dataset construction. The main steps include:

Excess Green (ExG) Calculation to highlight vegetation.

Binary Thresholding to separate plant from background.

Small Object Removal to clean noise.

Green Segmentation in HSV Space to preserve true plant areas.

Output Generation of isolated weed images with visualization.
📥 [Click here to download the full notebook from the release page](https://github.com/TA-code-ai/DIP-Project-Codes/releases/tag/v1.0)
# Stable Diffusion 3.5 Model
# Training Scences
# Training YOLOv12
# Results
