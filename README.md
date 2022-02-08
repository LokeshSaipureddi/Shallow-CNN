## Dynamic Mode Decomposition Based Features for the Detection of COVID-19 From CT Scan Images

### Dataset
COVID Chest CT dataset proposed by Yang et al. [3]is used for evaluating the proposed model. The dataset comprises 746 CT scan images of various patients. The entire dataset has two categories (397 images each) of COVID positive samples and Non-COVID samples. Without any other modifications on the data set, the latter was then split into 3 parts -60 %, 20 %, 20 % - for training, testing, and validation, respectively. Detailed information on the distributions of the COVID data set is shown in Table 2. </br>
![alttext](https://github.com/LokeshSaipureddi/Shallow-CNN/blob/main/Screenshot%202022-02-08%20154929.png)

### Image Preprocessing
Dynamic mode decomposition (DMD) is a popular data decomposition algorithm introduced in 2010 mainly in the field of Fluid dynamics [13] and later extended to computer vision, smart grid, language processing, etc [14,15,16]. The foundation for DMD is based on the well-known linear Koopman operator which captures the non-linear data dynamics [13]. The DMD algorithm identifies the spatial and temporal dynamics from the measured data and is considered as the most prominent feature of DMD as existing methods generally identify either of the dynamics. DMD algorithm merges the characteristics of proper orthogonal decomposition (POD) and Fourier transform. In the DMD algorithm, the measured data is decomposed into Spatio-temporal modes to estimate the underlying dynamics of the data.

### Proposed Architecture
   We proposed the Shallow Convolutional Neural Network [5], which can produce the same results as other deep neural networks reported in the literature. The proposed model consists of 9 Layers with 6 Convolutional Layers, 2 Maxpool layers, and a single Fully connected layer. The Proposed Model has 3 blocks, where each block is constituted of 1 convolution layer with kernel size (3,3) along with a short cut convolution layer with kernel size (1,1). This is shown in fig 1.</br>
![alttext](https://github.com/LokeshSaipureddi/Shallow-CNN/blob/main/Screenshot%202022-02-08%2015000.png) </br>
  Figure1 illustrates the proposed shallow CNN model and Table.1 tabulates the details. The proposed shallow network has 38,210 learnable parameters, which is very few in comparison to other deep models used for the same task, as shown in Table.1.</br>
![alttext]()
### Results
   In the first set of experiments, the original CT images are classified using the proposed shallow CNN model and the results are compared using various deep CNN models namely VGG16, Resnet50v2, InceptionV3, InceptionResnetV2, DenseNet121, and VGG19.  The performance comparisons are depicted in Table 2 and it is evident that the proposed architecture outperforms other models in terms of different output quality measures. This confirms the superiority of the proposed architecture to accurately predict the Covid 19 disease using CT images. Since the learnable parameters are very few for the proposed shallow CNN model, the proposed architecture can easily be used for the Covid 19 classification task.
 ![alttext]()
 The second set of experiments are performed to highlight the potential of the proposed DMD-based attention preprocessing stage for Covid 19 disease classification. The results are tabulated in Table 3 and by comparing with other deep CNN models it is clear that the proposed shallow CNN outperforms many of the existing  models. These evaluations also confirm the superiority of the DMD-based attention driven preprocessing stage. The proposed DMD stage is able to capture the inherent dynamics of the data and the extracted sparse dynamics matrix is fed as input to the classifier. The improved accuracy suggests that the extracted spatial dynamics captures the predominant features to distinguish the Covid 19 disease cases. 
 ![alttext]()
 From Table 2 and Table 3, it is clearly evident that the proposed Architecture was able to achieve comparable performance (in terms of accuracy) with minimal complexity compared to other state-of-the-art models which were shown in Table 4. </br>                        
Table 5: performance comparison of proposed shallow CNN models on state-of-the-art models of COVID detection from CT scan images </br>  
![alttext]()

