# real-fake-face-detection-transfer-learning-
Real vs. Fake Face Detection: A Comparative Study of CNN Architectures
This repository showcases an academic mini-project where two popular convolutional neural network (CNN) architectures, VGG16 and MobileNetV2, were fine-tuned on a real vs. fake face dataset. Below is a detailed analysis of the project, including dataset details, model performance, and key takeaways.

📁 Dataset Details
The dataset was split into three sets:

Training set: 1428 images
Validation set: 306 images
Test set: 307 images
This dataset posed a unique challenge due to its small size and the subtle differences between real and fake faces.

🧠 Model Architectures
1. VGG16
Description:
VGG16 is a deep CNN with 16 layers, comprising convolutional layers with 3x3 filters, followed by max pooling and fully connected layers for classification.

Advantages:
Effective for learning intricate patterns.
Proven robustness in many image classification tasks.

Disadvantages:
A large number of parameters (~138M), making it computationally expensive.
Prone to overfitting on smaller datasets.

2. MobileNetV2
Description:
MobileNetV2 is a lightweight CNN with fewer parameters (~3.4M). It uses depthwise separable convolutions for efficiency and incorporates inverted residual blocks and linear bottlenecks for better feature extraction.

Advantages:
Highly efficient and suitable for smaller datasets.
Better gradient flow due to residual connections.

Disadvantages:
May sacrifice some accuracy on highly complex datasets compared to larger architectures.


📊 Performance Results
After fine-tuning both models on the dataset, the results were as follows:

VGG16: Test accuracy 59%
MobileNetV2: Test accuracy 65%
Both models struggled to generalize beyond 65%, despite extensive hyperparameter tuning. Interestingly, other groups working on the same dataset also reported lower or comparable results, highlighting the dataset's inherent difficulty.

⚙️ Analysis

Why MobileNetV2 Outperformed VGG16

Efficient Design: MobileNetV2's lightweight architecture reduced overfitting on the small dataset.
Better Feature Extraction: Depthwise separable convolutions and residual connections allowed MobileNetV2 to capture subtle differences more effectively.
Fewer Parameters: MobileNetV2's smaller size was better suited for the dataset size, compared to VGG16's heavyweight structure.

Why Accuracy Was Capped at 65%

Dataset Challenges:
Small size limited the ability to generalize.
Subtle differences between real and fake faces increased the task complexity.

Overfitting: Regularization techniques helped, but the dataset's size still constrained generalization.

General Trends: Other groups using the same dataset reported similar results, suggesting inherent challenges in the dataset.

🔍 Lessons Learned
This project reinforced key lessons:

Model Architecture Matters: Lightweight architectures like MobileNetV2 are often better for small datasets.
Dataset Quality and Size Are Critical: Larger and more diverse datasets improve model performance significantly.
Experimentation is Essential: Iterating through hyperparameters is crucial for optimization.

🎯 Conclusion
This project was a valuable learning experience, highlighting the practical trade-offs between model complexity, dataset size, and task difficulty. While the results were modest, they provided deep insights into CNN architectures and their behavior on challenging datasets.

Feel free to explore the code and replicate the experiments. Contributions, suggestions, or discussions are always welcome!

