# Brain Tumor Classification Using Deep Neural Networks

## Why This Project?
The classification of brain tumors is a critical task in medical imaging, facilitating early diagnosis and effective treatment planning. Automating this process using deep learning models can:
- Reduce human error.
- Accelerate diagnosis.
- Support clinical decision-making.

However, traditional deep neural networks face challenges like the vanishing gradient problem, especially with deeper architectures. This project was undertaken to address these challenges and explore how advanced architectural designs can improve the performance of models in classifying brain tumors from MRI scans.

## What Was Done?
### Objective
The goal of this project was to evaluate the impact of skip connections in residual networks (ResNets) on the performance of deep neural networks for MRI-based brain tumor classification. The research focused on:
1. Comparing plain deep networks with ResNets.
2. Mitigating training challenges such as vanishing and exploding gradients.
3. Optimizing hyperparameters for stability and performance.

### Dataset
The dataset used consisted of 7,023 MRI images, categorized into four classes:
- Glioma
- Meningioma
- No Tumor
- Pituitary

The images were preprocessed and augmented to ensure robustness and generalizability. Augmentation techniques included rotation, translation, shearing, zooming, and horizontal flipping.

### Models Explored
1. **Plain Networks:**
   - Configurations of 18, 34, and 40 layers.
   - Struggled with vanishing gradients as depth increased.

2. **Residual Networks (ResNets):**
   - Leveraged skip connections to address the vanishing gradient problem.
   - Showed significant improvements in gradient flow and performance metrics.

### Performance Metrics
Models were evaluated using:
- Accuracy
- Precision
- Recall
- F1-score

## How It Was Done?
1. **Data Preprocessing:**
   - Resized images to 224x224 pixels.
   - Normalized pixel values to the range [0,1].
   - Split data into training, validation, and test sets.

2. **Data Augmentation:**
   - Applied transformations to enhance variability and reduce overfitting.

3. **Model Construction:**
   - Designed plain networks to analyze the effects of increasing depth.
   - Integrated skip connections in ResNets for better gradient flow.

4. **Mitigating Vanishing and Exploding Gradients:**
   - **Vanishing Gradient:** Skip connections in ResNets helped maintain effective gradient propagation.
   - **Exploding Gradient:** Gradient clipping and reducing the learning rate were employed to stabilize training.

5. **Hyperparameter Tuning:**
   - Used dynamic learning rates to adapt during training.
   - Implemented dropout for regularization.
   - Employed the Adam optimizer for efficient weight updates.

### Key Results
- Plain networks struggled with deeper architectures, achieving a maximum accuracy of 86.42%.
- ResNet architectures demonstrated superior stability and performance, with the 40-layer ResNet achieving a test accuracy of 91.76%.

### Challenges and Solutions
- **Vanishing Gradient Problem:** Addressed using skip connections in ResNets.
- **Exploding Gradient Problem:** Mitigated using gradient clipping (maximum norm of 1) and reducing the learning rate (from 0.001 to 0.00008).

## Conclusion
This project highlights the importance of architectural innovations like skip connections in training deep neural networks effectively for medical imaging tasks. ResNets outperformed plain networks, proving their robustness and efficiency in handling complex datasets. Future work can focus on transfer learning and utilizing pre-trained models to further enhance performance and generalization.

---
This repository contains all the code and resources used in the project, along with detailed analysis and visualizations of the results. Feel free to explore and contribute!

