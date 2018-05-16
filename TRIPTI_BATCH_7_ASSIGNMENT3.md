# Article 1

## Activation function:

###### Use of this function in the neural network is to predict if the result of a given set of input is activated or not by calculating its weighted sum using different functions.

+ **Sigmoid function:** The range of this function is (0,1) where input values can be in between  –inf to inf. This function is very active only for a small range of input dataset and beyond this range on both sides whether positive or negative, this function is not useful as it’s return value as 0 or 1. It is used in classification problems.

+ **ReLu (Rectified linear unit):**   *A(x) = max(0,x)*

    If the input value is negative, ReLu will throw away those values and return zero as output, otherwise, the value of output will be equal to the value of the input. Since it requires less mathematical operations, it is less expensive than other functions. 

+ **Leaky ReLu:** It is same as Relu but instead of zero, it will give ***0.01x*** as output when ***x (input value) is negative***. These functions will help neurons to not just die when they are negative as it still gives some value and stops dying ReLu problem. It will give an inclined line instead of a flat horizontal line.

+ **ELU (Exponential linear unit):**  *y = a(e^x – 1 ) when x < 0 else y = x*

    Unlike ReLu and Leaky Relu, it takes care of the vanishing gradient problem when an input value is negative and it smoothes down slowly.

+ **SELU (Scaled exponential linear units):**  *b(ELU)*

    Values of these two parameters (a and b) are derived from input data.

###### Out of all, SELU converges better on all input values but is more expensive than other functions as it requires more mathematical computations.


**********************



# Article 2

## Convolutions:

###### It is a method of extracting features from input data by applying various filters to get the type of output that we want.

+  **3 x 3:**  Convolution can be of any size and 3 x 3 is most commonly used as it requires less power and is used for feature extraction. It reduces dimensions of input by 2.

+  **1 x 1:**  It is used as ***feature merger, not a feature extractor*** as it maps one to one pixel from input to output and it helps to reduce dimensions.

+  **Cx1, 1xC Convolutions:**  If we first do a convolution of size  Cx1 on the input image and then if we again do a convolution of size 1xC on the output which we got from the first convolution will give same result as if we do a convolution of size CxC on the input image. Separable convolution is 7.2 times faster as it has fewer parameters with 0.3% loss in accuracy. 
 
+ **Grouped Convolution:** It is used to reduce the mathematical computation by dividing channels into separate groups and then merging the output layers to get the final output.

+ **Depthwise Separable Convolutions:**  It is a combination of Depthwise convolution and Pointwise convolution. Depthwise convolution applies to a single input channel at a time, unlike standard convolution which applies at all channels at a time. Pointwise convolution is of size 1x1 which applies to "N" channels at a time and because of fewer parameters, it is faster than standard convolution.

+ **MaxPooling:** It is used to reduce the receptive field. It scales down an image and is useful when we have extracted most of the features.

 ****************


# Article 3

## Regularization:

When we overfit a model, it performs poor on the test dataset. Regularization keeps all the features but reduces number of parameters.
This is one of the challenges we face in the Deep Learning where we have such a large number of layers with so many neurons.

**We regularize the model by using various techniques to prevent overfitting. Some of them are:**

+ **DropOut:**  As the name suggests, dropping out some neurons from a network to make a model simpler and remaining neurons are trained by those dropout neurons so that a model will not ignore any important feature.

+ **Label Smoothing:** Sometimes we overfit a model to get 100% correct output. To avoid overfitting of a model we relax threshold level.
*E.g.:* If we get output by 90% accuracy, we still accept it as we have relaxed threshold level by 10% and consider it as a final output.

*****************









