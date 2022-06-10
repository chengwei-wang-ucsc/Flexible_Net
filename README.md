# Flexible_Net
This is an example of throughly connecting optuna's hyper-parameter tuning options with as many PyTorch neural net aspects as possible.

# Implementation's Tunable Parameters:
1, Number of hidden layers.<br>
2, Each layer's hidden size.<br>
3, The dropout rate of each layer.<br>
4, Which activation function to use between each layer and last layer.<br>
5, Turn on the bidirectional option or not.<br>

While Pytorch's API, such torch. nn.LSTM(), has a "n_layers" blank to fill in how many hidden layers to initiate and include in the structure, I found that having a dropout layer between each hidden layer is more likely to produce better results than only having one dropout layer at the end. There is a "dropout" option in Pytorch's API to dropout a specified portion of neurons of each layer; however, when "n_layers" is nmore than 1, dropout is performed after each layer or only dropout once is unclear. Therefore, I found this implementation very useful in terms of bring-in certainty into our neural network structure during definition.
Furthermore, I have also managed to allow optuna to fine tune the defined neural network's activation function out of all the avaliable Pytorch activation fuctions.
