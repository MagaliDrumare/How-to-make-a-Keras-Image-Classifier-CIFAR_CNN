
# Réseau de neurones à convolution (CNN) 

```
# Initialisation du modèle. 
model = Sequential()

# Conv2D>MaxPooling>Dropout
model.add(Conv2D(32, (3, 3), padding='same',
input_shape=(IMG_ROWS, IMG_COLS, IMG_CHANNELS)))
model.add(Activation('relu'))
model.add(MaxPooling2D(pool_size=(2, 2)))
model.add(Dropout(0.25))

# Flatten>Connected>Activation>Dropout
model.add(Flatten())
model.add(Dense(512))
model.add(Activation('relu'))
model.add(Dropout(0.5))

# Output layer 
model.add(Dense(NB_CLASSES))
model.add(Activation('softmax'))
model.summary()
```



