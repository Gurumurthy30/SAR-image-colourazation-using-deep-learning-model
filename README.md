# SAR image colourazation using deep learning model

## Overview
This project focuses on enhancing grayscale Synthetic Aperture Radar (SAR) images by applying advanced deep learning techniques for colorization. SAR images, known for capturing data in any weather or lighting conditions, are valuable for Earth observation. However, the lack of color makes them harder to interpret. This project aims to bridge that gap by developing a deep learning model that adds color to SAR images while maintaining their structural integrity and fine details.

## Key Components
Input SAR Image and Preprocessing
SAR images often contain noise and distortions. Before feeding the images into the model, preprocessing steps like noise reduction (using Lee and Frost filters) and radiometric corrections are applied to enhance clarity and accuracy.

### 1,Swin Transformer Encoder
The Swin Transformer captures both global and local features of the SAR images. This helps the model understand spatial relationships and assigns accurate colors to objects in the scene, making features like the sky or vegetation more identifiable.

### 2,ECA Net (Efficient Channel Attention)
ECA Net ensures that the model focuses on the most important features by emphasizing critical channels related to textures and colors, resulting in vibrant and accurate colorization.

### 3,HR Net Decoder
HR Net maintains high resolution throughout the decoding process, which is essential for preserving fine details in small objects, such as roads or rivers, that are crucial for applications like disaster monitoring.

### 4,EDSR (Enhanced Deep Super-Resolution)
EDSR improves the final output by refining details and enhancing the overall resolution, making the images ready for practical applications like urban planning and environmental monitoring.

## Final Output
The final product is a high-resolution, colorized SAR image that is geo-referenced and suitable for applications such as disaster management, urban planning, and other fields that rely on precise geospatial data.

## Why This Approach?
While GANs (Generative Adversarial Networks) are powerful for generating new images, they often struggle with maintaining fine details and may introduce artifacts. This project uses a combination of Swin Transformer, ECA Net, HR Net, and EDSR to ensure detail preservation, structural integrity, and high-resolution outputs.
