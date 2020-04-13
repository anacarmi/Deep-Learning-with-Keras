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
``````````
from Keras import Sequential
from Keras import Dense

model = Sequential()

model.add(Dense(64, input_shape=(20,), activation='relu'))

model.add(Dense(3, activation='sigmoid'))

model.compile(optimizer='adam',
           loss='binary_crossentropy',
           metrics=['accuracy'])

model.summary()

``````````

### Building the structure 

`Sequential()` it is the structure of how the NN has to be. Most of the cases it is always Sequential.

To add the layers, you have to write the `.add()` to the model you named and write `Dense()` which is a way to say you are building a layer. Inside Dense you have the number of neurons in that layer, and if it is the first or only hidden layer then add the `input_shape=()` which says how many neurons there are as input. Finally you add the `activation=` function which in this example we use `relu`.

After adding the hidden layers (within the input) you add the output with `Dense(1)`

#### Example:

For a NN with 3 inputs, one hidden layer of 2 neurons and an output of 1, we have:
```
model = Sequential()

model.add(Dense(2, input_shape=(3,), activation='relu')

model.add(Dense(1))
```

### Compilation
### Fitting
### Evaluation
### Prediction


-------

Other example:

````````````````
# Train for 100 epochs using a validation split of 0.2
model.fit(sensors_train,parcels_train, epochs = 100, validation_split = 0.2)

# Predict on sensors_test and round up the predictions
preds = model.predict(sensors_test)
preds_rounded = np.round(preds)

# Print rounded preds
print('Rounded Predictions: \n', preds_rounded)

# Evaluate your model's accuracy on the test data
accuracy = model.evaluate(sensors_test,parcels_test)[1]

# Print accuracy
print('Accuracy:', accuracy)
````````````````






