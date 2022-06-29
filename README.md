1. Train Accuracy := 87.17%
2. Validation accuracy := 60.94% , highest = 82.81%
3. Test Accuracy := 64.29%


MODEL STRUCTURE

_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 resizing (Resizing)      (None, 128, 128, 3)       0         
                                                                 
 rescaling (Rescaling)    (None, 128, 128, 3)       0         
                                                                 
 cropping2d (Cropping2D)  (None, 98, 98, 3)         0         
                                                                 
 conv2d (Conv2D)          (None, 98, 98, 16)        448       
                                                                 
 max_pooling2d (MaxPoolin  (None, 49, 49, 16)       0         
 g2D)                                                            
                                                                 
 batch_normalization (Bat  (None, 49, 49, 16)       64        
 chNormalization)                                                
                                                                 
 dropout (Dropout)        (None, 49, 49, 16)        0         
                                                                 
 conv2d (Conv2D)          (None, 49, 49, 32)        4640      
                                                                 
 max_pooling2d (MaxPoolin  (None, 24, 24, 32)       0         
 g2D)                                                            
                                                                 
 batch_normalization (Bat  (None, 24, 24, 32)       128       
 chNormalization)                                                
                                                                 
 conv2d (Conv2D)          (None, 24, 24, 64)        18496     
                                                                 
 max_pooling2d (MaxPoolin  (None, 12, 12, 64)       0         
 g2D)                                                            
                                                                 
 batch_normalization (Bat  (None, 12, 12, 64)       256       
 chNormalization)                                                
                                                                 
 conv2d (Conv2D)          (None, 12, 12, 64)        36928     
                                                                 
 max_pooling2d (MaxPoolin  (None, 6, 6, 64)         0         
 g2D)                                                            
                                                                 
 batch_normalization (Bat  (None, 6, 6, 64)         256       
 chNormalization)                                                
                                                                 
 conv2d (Conv2D)          (None, 6, 6, 64)          36928     
                                                                 
 max_pooling2d (MaxPoolin  (None, 3, 3, 64)         0         
 g2D)                                                            
                                                                 
 batch_normalization (Bat  (None, 3, 3, 64)         256       
 chNormalization)                                                
                                                                 
 dropout (Dropout)        (None, 3, 3, 64)          0         
                                                                 
 flatten (Flatten)        (None, 576)               0         
                                                                 
 dense (Dense)            (None, 64)                36928     
                                                                 
 dense (Dense)            (None, 8)                 520       
                                                                 
=================================================================
Total params: 135,848
Trainable params: 135,368
Non-trainable params: 480
_________________________________________________________________

