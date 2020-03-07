# ![identify the image : Neuros_Network](https://colab.research.google.com/drive/1URhMOssSEy-yaRI_AGxYh8Ppykl8GETW)


*The first line creates a Sequential model. This is the simplest kind of Keras
model for neural networks that are just composed of a single stack of layers connected
sequentially. This is called the Sequential API.
* Next, I build the first layer and add it to the model. It is a Flatten layer whose
role is to convert each input image into a 1D array: if it receives input data X, it
computes X.reshape(-1, 1). This layer does not have any parameters; it is just
there to do some simple preprocessing. Since it is the first layer in the model, you
should specify the input_shape, which doesn’t include the batch size, only the
shape of the instances. Alternatively, you could add a keras.layers.InputLayer
as the first layer, setting input_shape=[28,28].
#Next I add a Dense hidden layer with 300 neurons. It will use the ReLU activation
function. Each Dense layer manages its own weight matrix, containing all the
connection weights between the neurons and their inputs. It also manages a vector
of bias terms (one per neuron). When it receives some input data, it computes
Equation 10-2.
* Then I add a second Dense hidden layer with 100 neurons, also using the ReLU
activation function.
* Finally, I add a Dense output layer with 10 neurons (one per class), using the
softmax activation function (because the classes are exclusive).
so the model looks like this:

I trained the model 30 times, so the accuracy achieved 88.9%


55000/55000 [=========] - 5s 100us/sample - loss: 0.2252 - accuracy: 0.9192 - val_loss: 0.2978 - val_accuracy: 0.8892.

this is the input images for this model, 
![model](https://github.com/LadyWinterD/Neuros_Network/blob/master/model.PNG?raw=true)


this is the output for this model,

![inputdata](https://github.com/LadyWinterD/Neuros_Network/blob/master/MNIST.PNG?raw=true)


you can see:
for the first image it estimates that the probability of
class 9 (ankle boot) is 96%, the probability of class 5 (sandal) is 3%, the probability of
class 7 (sneaker) is 1%, and the probabilities of the other classes are negligible.
![output](https://github.com/LadyWinterD/Neuros_Network/blob/master/OUTPUT.PNG?raw=true)


