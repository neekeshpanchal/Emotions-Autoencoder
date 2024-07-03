# Emotions-Autoencoder
Applying an autoencoder and sequential neural network towards predicting human emotion in a video. Implemented using keras, sklearn, matplotlib, and cv2.


![image](https://github.com/neekeshpanchal/Emotions-Autoencoder/assets/80868396/046f0cc2-20f2-4091-9e67-8b00e6f90aad)


Encoder Layer:
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 input_1 (InputLayer)        [(None, 64, 64, 3)]       0

 conv2d (Conv2D)             (None, 64, 64, 32)        896       

 max_pooling2d (MaxPooling2D  (None, 32, 32, 32)       0
 )

 conv2d_1 (Conv2D)           (None, 32, 32, 16)        4624      

 max_pooling2d_1 (MaxPooling  (None, 16, 16, 16)       0
 2D)

 conv2d_2 (Conv2D)           (None, 16, 16, 8)         1160

 max_pooling2d_2 (MaxPooling  (None, 8, 8, 8)          0
 2D)

 conv2d_3 (Conv2D)           (None, 8, 8, 8)           584

 up_sampling2d (UpSampling2D  (None, 16, 16, 8)        0
 )

 conv2d_4 (Conv2D)           (None, 16, 16, 16)        1168

 up_sampling2d_1 (UpSampling  (None, 32, 32, 16)       0
 2D)

 conv2d_5 (Conv2D)           (None, 32, 32, 32)        4640

 up_sampling2d_2 (UpSampling  (None, 64, 64, 32)       0
 2D)

 conv2d_6 (Conv2D)           (None, 64, 64, 3)         867

 Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #
=================================================================
 flatten (Flatten)           (None, 12288)             0

 dense (Dense)               (None, 128)               1572992

 dense_1 (Dense)             (None, 64)                8256

 dense_2 (Dense)             (None, 3)                 195

=================================================================
Total params: 1,581,443
Trainable params: 1,581,443
Non-trainable params: 0
_________________________________________________________________

=================================================================
Total params: 13,939
Trainable params: 13,939
Non-trainable params: 0
_________________________________________________________________
