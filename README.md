# Interpretability of CNN during classification of PV

This project was undertaken during the period of research under Dr Zeeshan Ahmad. 

###  **EXPERIMENT 1 : DEFECT CLASSIFICATION OF SOLAR CELLS**

<pre>
The main objective of this study was to understand the interpretability of CNN models during defect classification by using LIME method.
  
# Main Objectives of EXPERIMENT 1:
  1. Construct a CNN to perform surpervised classificaion on "ELPV" dataset, classifying the solar modules to their respective defect types
  2. To study the LIME MASK and understand the focus of the model



#The CNN model has the following architecture :-
  Model: "sequential_2"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_12 (Conv2D)          (None, 40, 24, 32)        896       
                                                                 
 batch_normalization_6 (Bat  (None, 40, 24, 32)        128       
 chNormalization)                                                
                                                                 
 max_pooling2d_12 (MaxPooli  (None, 20, 12, 32)        0         
 ng2D)                                                           
                                                                 
 conv2d_13 (Conv2D)          (None, 20, 12, 32)        9248      
                                                                 
 batch_normalization_7 (Bat  (None, 20, 12, 32)        128       
 chNormalization)                                                
                                                                 
 max_pooling2d_13 (MaxPooli  (None, 10, 6, 32)         0         
 ng2D)                                                           
                                                                 
 conv2d_14 (Conv2D)          (None, 10, 6, 64)         18496     
                                                                 
 batch_normalization_8 (Bat  (None, 10, 6, 64)         256       
 chNormalization)                                                
                                                                 
 max_pooling2d_14 (MaxPooli  (None, 5, 3, 64)          0         
 ng2D)                                                           
                                                                 
 conv2d_15 (Conv2D)          (None, 5, 3, 128)         73856     
                                                                 
 batch_normalization_9 (Bat  (None, 5, 3, 128)         512       
 chNormalization)                                                
                                                                 
 max_pooling2d_15 (MaxPooli  (None, 3, 2, 128)         0         
 ng2D)                                                           
                                                                 
 conv2d_16 (Conv2D)          (None, 3, 2, 256)         295168    
                                                                 
 batch_normalization_10 (Ba  (None, 3, 2, 256)         1024      
 tchNormalization)                                               
                                                                 
 max_pooling2d_16 (MaxPooli  (None, 2, 1, 256)         0         
 ng2D)                                                           
                                                                 
 conv2d_17 (Conv2D)          (None, 2, 1, 512)         1180160   
                                                                 
 batch_normalization_11 (Ba  (None, 2, 1, 512)         2048      
 tchNormalization)                                               
                                                                 
 max_pooling2d_17 (MaxPooli  (None, 1, 1, 512)         0         
 ng2D)                                                           
                                                                 
 flatten_2 (Flatten)         (None, 512)               0         
                                                                 
 dense_6 (Dense)             (None, 256)               131328    
                                                                 
 dropout_4 (Dropout)         (None, 256)               0         
                                                                 
 dense_7 (Dense)             (None, 128)               32896     
                                                                 
 dropout_5 (Dropout)         (None, 128)               0         
                                                                 
 dense_8 (Dense)             (None, 10)                1290      
                                                                 
=================================================================
Total params: 1747434 (6.67 MB)
Trainable params: 1745386 (6.66 MB)
Non-trainable params: 2048 (8.00 KB)
_________________________________________________________________
  
# The result on the test data is :
Classification Report:
              precision    recall  f1-score   support

           0       0.59      0.51      0.55       356
           1       0.39      0.44      0.41       263
           2       0.59      0.61      0.60       182
           3       0.87      0.96      0.91       297
           4       0.88      0.88      0.88        34
           5       0.91      0.93      0.92      2023
           6       0.56      0.67      0.61       159
           7       0.66      0.65      0.66       211
           8       0.25      0.38      0.30        40
           9       0.68      0.43      0.52       336

   micro avg       0.77      0.77      0.77      3901
   macro avg       0.64      0.65      0.64      3901
weighted avg       0.77      0.77      0.77      3901
 samples avg       0.77      0.77      0.77      3901

# Conclusion 
  Using LIME we can clearly observe the focus of the model.
  
  
</pre>
