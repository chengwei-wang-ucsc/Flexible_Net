# Flexible_Net
This is an example of throughly connecting optuna's hyper-parameter tuning options with as many PyTorch neural net aspects as possible.

While Pytorch's API, such torch. nn.LSTM(), has a "n_layers" blank to fill in how many hidden layers to initiate and include in the structure, I found that having a dropout layer between each hidden layer is more likely to produce better results than only having one dropout layer at the end. There is a "dropout" option in Pytorch's API to add the dropout layer into the defined neural net layer, however, whether the dropout is performed after each layer or only dropout once at the end is unclear. Therefore, I found this implementation very useful in terms of bringing certainty into our neural network structure during definition.

Furthermore, I have also managed to allow optuna to fine tune the defined neural network's activation function out of all the avaliable Pytorch activation fuctions.
