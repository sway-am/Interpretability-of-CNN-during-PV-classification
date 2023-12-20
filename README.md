# Interpretability of CNN during classification of PV

This project was undertaken during the period of research under Dr Zeeshan Ahmad. 

### Description

<pre>
The main objective of this study was to understand the interpretability of CNN models during classification by using different methodology.
  
# Three techniques were tested, 
  1. LIME
  2. SHAP
  3. Grad CAM
  
# Main Objectives
  1. Construct a CNN to perform surpervised classificaion on "ELPV" dataset, classifying the solar modules to mono-si or poly - si modules
  2. To show that while classifying the CNNs focused mainly in the corner of the images, as mono-si panels have triangular cut outs and 
  poly - si solar panels have no cuts, ie. they are a full square.

#The CNN model has the following architecture :-
  Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 120, 120, 16)      448       
                                                                 
 max_pooling2d (MaxPooling2  (None, 60, 60, 16)        0         
 D)                                                              
                                                                 
 conv2d_1 (Conv2D)           (None, 60, 60, 16)        2320      
                                                                 
 max_pooling2d_1 (MaxPoolin  (None, 30, 30, 16)        0         
 g2D)                                                            
                                                                 
 conv2d_2 (Conv2D)           (None, 30, 30, 32)        4640      
                                                                 
 max_pooling2d_2 (MaxPoolin  (None, 15, 15, 32)        0         
 g2D)                                                            
                                                                 
 flatten (Flatten)           (None, 7200)              0         
                                                                 
 dense (Dense)               (None, 16)                115216    
                                                                 
 dropout (Dropout)           (None, 16)                0         
                                                                 
 dense_1 (Dense)             (None, 1)                 17        
                                                                 
=================================================================
Total params: 122641 (479.07 KB)
Trainable params: 122641 (479.07 KB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________

# The result on the test data is :
    precision    recall  f1-score   support

        mono       1.00      1.00      1.00       216
        poly       1.00      1.00      1.00       309

    accuracy                           1.00       525
   macro avg       1.00      1.00      1.00       525
weighted avg       1.00      1.00      1.00       525

# Conclusion 
  According to the observation, the SHAP method had the best interpretability map. This method will be further applied to study the interpretibility
  of CNNs used in defect classification of solar cells, to verify their outcomes.
  
  
</pre>
