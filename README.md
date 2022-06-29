No need to mount google drive if running on jupyter notebook



MODEL STRUCTURE
'''
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 resizing_13 (Resizing)      (None, 128, 128, 3)       0         
                                                                 
 rescaling_13 (Rescaling)    (None, 128, 128, 3)       0         
                                                                 
 cropping2d_13 (Cropping2D)  (None, 98, 98, 3)         0         
                                                                 
 conv2d_57 (Conv2D)          (None, 98, 98, 16)        448       
                                                                 
 max_pooling2d_57 (MaxPoolin  (None, 49, 49, 16)       0         
 g2D)                                                            
                                                                 
 batch_normalization_57 (Bat  (None, 49, 49, 16)       64        
 chNormalization)                                                
                                                                 
 dropout_26 (Dropout)        (None, 49, 49, 16)        0         
                                                                 
 conv2d_58 (Conv2D)          (None, 49, 49, 32)        4640      
                                                                 
 max_pooling2d_58 (MaxPoolin  (None, 24, 24, 32)       0         
 g2D)                                                            
                                                                 
 batch_normalization_58 (Bat  (None, 24, 24, 32)       128       
 chNormalization)                                                
                                                                 
 conv2d_59 (Conv2D)          (None, 24, 24, 64)        18496     
                                                                 
 max_pooling2d_59 (MaxPoolin  (None, 12, 12, 64)       0         
 g2D)                                                            
                                                                 
 batch_normalization_59 (Bat  (None, 12, 12, 64)       256       
 chNormalization)                                                
                                                                 
 conv2d_60 (Conv2D)          (None, 12, 12, 64)        36928     
                                                                 
 max_pooling2d_60 (MaxPoolin  (None, 6, 6, 64)         0         
 g2D)                                                            
                                                                 
 batch_normalization_60 (Bat  (None, 6, 6, 64)         256       
 chNormalization)                                                
                                                                 
 conv2d_61 (Conv2D)          (None, 6, 6, 64)          36928     
                                                                 
 max_pooling2d_61 (MaxPoolin  (None, 3, 3, 64)         0         
 g2D)                                                            
                                                                 
 batch_normalization_61 (Bat  (None, 3, 3, 64)         256       
 chNormalization)                                                
                                                                 
 dropout_27 (Dropout)        (None, 3, 3, 64)          0         
                                                                 
 flatten_13 (Flatten)        (None, 576)               0         
                                                                 
 dense_26 (Dense)            (None, 64)                36928     
                                                                 
 dense_27 (Dense)            (None, 8)                 520       
                                                                 
=================================================================
Total params: 135,848
Trainable params: 135,368
Non-trainable params: 480
_________________________________________________________________

'''
