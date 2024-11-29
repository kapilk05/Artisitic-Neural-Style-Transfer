# Dynamic Multi-Style Transfer for Artistic Image Generation

![Header Image](images/header.jpg)  
*A robust system for real-time multi-style artistic transformations.*

---

## Overview

This repository contains the implementation and findings of the research project titled **Dynamic Multi-Style Transfer for Artistic Image Generation**. The project focuses on developing a robust and flexible system for real-time multi-style transfer using convolutional neural networks (CNNs). By leveraging the power of the VGG19 network and advanced neural training techniques, the system offers high-quality stylization with dynamic customization of style weight ratios while minimizing computational overhead.

![Example Style Transfer](images/overview_example.jpg)  
*Example of multi-style artistic transformations.*

---

## Features

- **Multi-Style Transfer:**  
   Blend multiple artistic styles into a single target image with customizable style weights.

- **Efficient Implementation:**  
   Uses VGG19 for high-quality feature extraction with optimal performance.

- **Dynamic Adjustability:**  
   Real-time adjustments to style-to-content weight ratios for tailored outputs.

- **Content Preservation:**  
   Retains the structural integrity of the content image during stylization.

- **Iterative Optimization:**  
   Combines multiple styles while preserving clarity and diversity.

---

## Methodology

### Data Preprocessing
- Resize and normalize content and style images for consistent processing.

### Feature Extraction
- Content features: Extracted from layer `conv4_2` of VGG19.  
- Style features: Derived from layers (`conv1_1`, `conv2_1`, `conv3_1`, `conv4_1`, `conv5_1`).

### Style Transfer Process
- Style features represented as **Gram Matrices** to capture textures and patterns.  
- Iterative updates ensure a seamless blend of content and multiple styles.

![Process Diagram](images/process_diagram.jpg)  
*Diagram showing the style transfer process.*

### Loss Function
- **Content Loss:** Ensures structural integrity.  
- **Style Loss:** Maintains artistic elements.  
- Combined as:
  \[
  L_{\text{total}} = \alpha \cdot L_{\text{content}} + \beta \cdot L_{\text{style}}
  \]

### Dynamic Customization
- Adjust content-style weights for diverse outputs.

---

## Results

### Qualitative Analysis
- Rich, stylized images preserving content details.  
- Outputs blend multiple styles seamlessly.

![Style Comparison](images/style_comparison.jpg)  
*Comparison: Single-style vs Multi-style.*

### Quantitative Analysis
- Loss curves demonstrate rapid convergence for both style and content optimization.

![Loss Curves](images/loss_curves.jpg)  
*Graphs showing loss decay over iterations.*

---

## Applications

- **Digital Art Creation:** Tools for professional artists.  
- **Content Creation:** Enhance creative outputs for media.  
- **Interactive Tools:** Real-time style manipulation for developers.

---

## Example Outputs

### Style Examples
- **Style 1:** Monet-inspired artistic textures.  
  ![Monet Style](images/monet_style.jpg)  
- **Style 2:** Sandstone-inspired patterns.  
  ![Sandstone Style](images/sandstone_style.jpg)  

### Final Stylized Image
![Final Output](images/final_output.jpg)  
*Content combined with multiple artistic styles.*

---

## Future Scope

1. **Real-Time Processing:**  
   Optimizing for faster style application.

2. **Video Style Transfer:**  
   Applying consistent stylization across video frames.

3. **Interactive UI:**  
   Creating a user-friendly interface for real-time adjustments.

4. **Advanced Neural Models:**  
   Exploring deeper architectures for improved quality.

---

## How to Use

1. **Clone this repository:**  
   ```bash
   git clone https://github.com/kapilk05/Artistic-Neural-Style-Transfer.git
