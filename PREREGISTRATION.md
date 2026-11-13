# PREREGISTRATION – SPEC 9901 - Applied Deep Learning

Bernardo Vieira de Castro - TU060 - a00048457

Academic year: 2026/2027

## Age Estimation Investigation

The aim of this assignment is to investigate different Deep Learning approaches to facial age estimation using CNNs. I will develop models capable of estimating a person's numerical age (regression) and predicting their age category (classification), comparing different network architectures, kernel sizes, image formats and activation functions to understand how each affects model performance.

### Comparisons and Predictions

I will initially create a baseline model using three hidden layers, 3×3 kernel sizes, color images (RGB) and ReLU activation functions. This model will serve as a reference point for all the other experiments, allowing me to compare the effects of changing individual aspects of the architecture and dataset. I am not suggesting that this is necessarily the best or worst combination of parameters, but rather a starting point that will give me a general idea of what performance to expect from my models.

As this is my first assignment of this kind, I am initially aiming for approximately 85% classification accuracy. However, given my limited experience, I would not be too surprised if I fall short of this target.

### Metrics to be used in all models:

* Regression: Mean Absolute Error (MAE) and Root Mean Squared Error (RMSE)
* Classification: Accuracy and F1-Score for classification, along with a confusion matrix
<br>
<br>

**Comparison 1: CNN kernel variations** (3x3 vs 7x7)

**Prediction**: I believe that the results from both kernel sizes will be relatively similar. However, because the dataset contains images covering a very wide age range (from 1 to over 100 years old), I predict that the 7×7 kernel will perform slightly better overall for age classification. Its larger receptive field may allow the network to capture broader facial features and patterns that help distinguish between different age categories.

On the other hand, I predict that the 3×3 kernel may perform better for regression. Its ability to capture finer facial details, such as wrinkles, skin texture and small changes around the eyes and mouth, could help the model distinguish between individuals who are close in age. I expect approximately 1–3% higher classification accuracy with the 7×7 kernel and a reduction of around 1–2 year in regression MAE comparatively with the 3×3 kernel.

**Potential Surprises**: I would be surprised if one kernel size significantly outperformed the other in both classification and regression. I would also be surprised if the 7×7 kernel performed better at regression.
<br>
<br>

**Comparison 2: Network variations** (Shallower vs Deep networks - 3 vs 5 hidden layers)

**Prediction**: I predict that deeper networks will perform better than shallower networks because having additional layers allows the model to learn more complex patterns. I expect approximately 4–6% higher classification accuracy and a reduction of around 2–5 years in regression MAE. However, deeper networks will take longer to train and require more computational resources.

**Potential Surprises**: I would be very surprised if the shallower network performed better than the deeper one.
<br>
<br>

**Comparison 3: Dataset variations** (Color vs Greyscale)

**Prediction**: I predict that color images will generally perform better than greyscale images because they contain additional visual information, including skin tone, complexion and other characteristics that may be associated with ageing. However, I believe greyscale images could perform better in certain situations, for example, inconsistent color balancing, lighting conditions or image quality could make someone appear to have a different skin tone than they naturally would. This could mislead the model, particularly if certain skin tones are underrepresented in the dataset. Greyscale images remove some of these color-related variations and allow the model to focus more on facial structure, wrinkles and texture.

Overall, I expect color images to achieve approximately 3–5% higher classification accuracy and around 2–3 year in regression MAE.

**Potential Surprises**: I would be surprised if greyscale images consistently outperformed color images across both regression and classification. This could suggest that color information introduces more noise than useful information into the dataset.
<br>
<br>

**Comparison 4: Different Activation Functions** (ReLU vs Tanh)

**Prediction**: I currently expect ReLU to perform better than Tanh, although this is more of an initial assumption based on my limited understanding of the two activation functions rather than a prediction I can confidently justify. I expect ReLU to achieve approximately 1–3% higher classification accuracy and a reduction of around 0.5–1 year in regression MAE. However, I am not particularly confident in this prediction and intend to investigate activation functions further throughout the assignment to develop a better understanding of their differences and effects on model performance. 

I am particularly curious to investigate how activation functions with different output ranges affect the learning process, especially the differences between functions with bounded outputs and those with unbounded outputs, as well as functions that allow negative values compared to those that restrict their outputs to non-negative values.

**Potential Surprises**: I would be surprised if both activation functions produced almost identical results across regression and classification. This could suggest that the choice of activation function has relatively little influence on this particular task.
<br>
<br>


