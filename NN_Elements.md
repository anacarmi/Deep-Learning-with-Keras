# Introduction to Neural Networks


### Steps or elements:
- Type of NN 
  - Sequential
  - Funtional
- Adding the neurons
  - Dense (add hidden layers)
    - Input neurons
    - activation
  - Add the last neuron
- Model.Summary()
- Compile
- Fit
- Evaluate
- Predict

----------

A basic code for a neural network is this one:
`````````````````
from Keras import Sequential
from Keras import Dense

model = Sequential()

# Add a hidden layer of 64 neurons and a 20 neuron's input
model.add(Dense(64, input_shape=(20,), activation='relu'))

# Add an output layer of 3 neurons with sigmoid activation
model.add(Dense(3, activation='sigmoid'))

# Compile your model with adam and binary crossentropy loss
model.compile(optimizer='adam',
           loss='binary_crossentropy',
           metrics=['accuracy'])

model.summary()

`````````````````
