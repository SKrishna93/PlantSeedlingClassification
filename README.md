# PlantSeedlingClassification

### Objective
The objective is to create a 12-class classifier capable of determining plant’s species from the various stages of grown plant seedlings images.

### Details:
* Dataset consists of images of plant species with 12 classes.
* The distribution of the images is difficult to distinguish when visualized using t-Distributed Stochastic Neighbor Embedding (t-SNE).
* Imbalanced data – Treated using Synthetic Minority Oversampling Technique (SMOTE) to balance the dataset. 
* Preprocessing: Resizing of the images
* In-memory dynamic image augmentation techniques like crop, flips, rotate, brightness, contrast were used.
* Transfer learning: Used ImageNet pretrained model ResNet-50 and InceptionResNetV2 to extract the features and the last layer is passed on to a multinomial logistic regression classifier. 
* For faster model convergence, cyclic learning rates with cosine annealing technique was used for tuning.
* After 50 epochs of training resulted in ~98% accuracy in validation set and for better understanding of individual classes performances confusion matrix was obtained.
