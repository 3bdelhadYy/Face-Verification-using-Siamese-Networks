🧠 Face Verification using Siamese Networks

A deep learning project for face verification (not classification) using Siamese Networks on the LFW (Labeled Faces in the Wild) dataset. The system learns to determine whether two face images belong to the same person based on similarity in embedding space.

🚀 Features
🔹 Siamese Network architecture for similarity learning
🔹 Custom CNN backbone (built from scratch)
🔹 Transfer Learning using VGG16
🔹 Implementation of:
Contrastive Loss
Triplet Loss
🔹 Data pipeline for generating:
Image pairs (same/different)
Triplets (anchor, positive, negative)
🔹 Evaluation using:
Accuracy
Loss curves
Distance distribution plots
🔹 Inference system for real-time face verification

📊 Methodology
🔹 Siamese Network

Two (or three) identical networks share weights to learn feature embeddings.

Input: two images
Output: embedding vectors
Decision based on Euclidean distance

🔹 Loss Functions
✔ Contrastive Loss
Minimizes distance for same-person pairs
Maximizes distance for different-person pairs
✔ Triplet Loss
Anchor closer to Positive than Negative
Improves embedding separation
🔹 Models Used
Custom CNN (Conv → BatchNorm → Pooling → Dropout)
VGG16 (pretrained on ImageNet, used as feature extractor)

📈 Results & Evaluation
Compared 4 experiments:
CNN + Contrastive
CNN + Triplet
VGG16 + Contrastive
VGG16 + Triplet
Metrics:
Verification Accuracy
Distance distributions
Optimal threshold selection

🧪 Inference

The model can verify two images:
verify_faces(img1, img2, backbone, threshold)

Output:

Distance score
Same/Different decision
Confidence estimate

🏆 Key Learnings
Metric learning for similarity-based tasks
Siamese network design and training
Contrastive vs Triplet loss comparison
Transfer learning integration
Practical evaluation of embedding spaces
👨‍💻 Author

Abdelhady Mohamed 
Communication and Information Engineering Student | Deep Learning & Computer Vision
