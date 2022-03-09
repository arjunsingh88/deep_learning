# Deep learning Portfolio
All the projects make use of deep learning frameworks
- ## `Project 1:`[ Image deduplication detector](https://github.com/arjunsingh88/deep_learning/tree/main/image_duplication_detector)
  - A Use-case Analysis and proposed solution for Deduplication of images on Classified advertisements on marketplace using Deep learning Frameworks
  - In a marketplaces users can post classified ads for objects they wish to sell. For various reasons, users might post multiple classified ads for the same item, i.e. creating duplicate classified ads. We’d like to avoid this, as it makes the user experience more confusing for other users. 
  - In this analysis, I have strategically broken the said use-case and proposed deep learning solution to detect such duplicate classified ads just by comparing the feature vectors of the 2 images from the classified ads. 

    <img width="852" alt="image" src="https://user-images.githubusercontent.com/45566835/157437992-25daa175-f13a-475c-93d4-dcb74fd00080.png">
    
  - Proposed Approach    
    1. Resize image & Data Augmentation using Tensorflow’s ImageDatagenerator and applied following augmentations to generate a set of 7(try as many as possible) augmented image map for every image.
    2. A pretrained CNN model called VGG16, by removing the last layer and using its dense layer to obtain a feature vector with learned values is obtained.
    3. Distance between two feature vector is then computed, in this case Euclidean distance is used but we have option to switch such as Manhattan, Hamming and the Cosine distance.
    4. The model takes two images and computes distance between then to classify if images are duplicates or different
    5. The notebook `final.ipynb` contains the entire deep learning solution to our problem. 
