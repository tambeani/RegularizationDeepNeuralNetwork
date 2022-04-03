# RegularizationDeepNeuralNetwork

## To implement dropout in Deep Neural Networks

The motivation behind implementing regularization is to prevent overfitting. This can be done in 2 ways

1. Putting constraints on parameters of ML model
2. Prevent neurons being overdependent on any variable
3. Batch normalization

For this implementation we would focus on 2nd point. For example, if a CNN is fed train image of the number 5, out of which certain images have swirls at the end of the handwritten 5. To prevent the model from overfitting on the "swirl" feature we randomly drop certain neurons. 

To achieve this we randomly delete some of the activations from the matrix of parameters. By doing so, we eliminate certain codependencies from certain parts of the data - swirls of different styles of writing 5. This ensures that your model is immune to these codependencies.

In practice, this deactivation of activation function can be defined via the dropout rate - 0.2 to 0.8. Since the dropout leaves behind "holes" in parameter, we impute these values by average of parameter for that layer. This makes the NN more robust & extrapolative. 

MIT License

Copyright (c) 2022 Aniruddha Tambe

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.