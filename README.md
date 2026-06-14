## What I built:
I built a CNN-based image classification model to classify three objects: phone, pen and bottle. 
Instead of using an existing dataset, I created my own dataset by taking pictures of these objects from different angles and lighting conditions.

## Experiments Performed:
1. Baseline CNN Model
- Optimizer: Adam
- Learning Rate: 0.001
- Batch Size: 8
- Dropout: 0.5
- Epochs: 15
2. Increased Dropout from 0.5 to 0.65
3. Added L2 Regularization
4. Reduced Epochs from 15 to 10
5. Reduced Batch Size from 8 to 7
6. Changed Learning Rate
7. Added Batch Normalization

## Observations:
  1.The baseline model achieved the highest validation accuracy but i noticed from the graph that validation loss kept on increasing 
  and also the difference btw training and validation accuracy showed me that the model was overfitting.
  
  2.I increased the dropout value thinking that it would reduce overfitting, but the results were opposite to what I expected
  The validation accuracy dropped, which showed me that increasing dropout too much can make the model lose important information during training.
  
  3.Since increasing dropout didnt work ,i decided to add L2 Regularization
  I expected L2 regularization to reduce overfitting and improve the model's performance on unseen data but 
  the validation accuracy was lower than the baseline model, and the validation loss also increased.
  This showed me that L2 regularization was not effective fro my dataset.
  
  4.I reduced the number of epochs from 15 to 10 because I wanted to reduce overfitting.
  The validation loss became more stable, but the validation accuracy was lower than the baseline model.
  
  5.I reduced the no of epochs from 15 to 10 expecting the model to overfit less and yeah it worked ,
  The validation loss became stable and gap btw training & validation accuracy also reduced.
  
  6.Further i reduced the batch size keeping everything same as previous experiment thinking that some randomness will be introduced & validation accuracy will improve
  and guess what As I expected validation accuracy increased and also confusion matrix showed better classification of images.
  Although it didnt achieve the highest accuarcy,it showed less overfitting,less validation loss and still maintained a decent validation accuracy.
  For me this was the best overall result.
  
  7.Since I got a good balance of everything in previous experiment, I kept the same settings and reduced the learning rate from 0.001 to 0.0005
  hoping that the model would learn more carefully and improve validation accuracy 
  but the validation accuracy decreased and the change did not improve the overall performance.
  
  8.Since the previous experiment did not improve validation accuracy, I tried adding batch normalization while keeping the other settings the same as exp 5
  cause i learned it is generally used to stabilize the training 
  but the validation accuracy dropped cloase to random guessing and validation loss also increased to a very high value
  This turned out to be the wrost performing experminet among all the experiments i condeucted.

## What Changed and Why:
1.I increased the dropout value because I wanted to reduce overfitting and improve generalization.

2.Since increasing dropout did not work as expected, I added L2 regularization to see if it could reduce overfitting.

3.As L2 regularization also did not work as I expected,so i Reduced epochs from 15 to 10 because 
I felt the model was learning the training dataset too muchh, I wanted to see if training for fewer epochs would help reduce overfitting.

4.Since reducing epochs gave a result i expected ,keeping the epochs same as 10 i reduced the batch size from 8 to 7 
because I thought the additional randomness during training might help the model generalize better and improve validation accuracy.

5.Since the batch size experiment gave the most balanced overall result, 
I reduced the learning rate from 0.001 to 0.0005 hoping that the model would learn more carefully and improve validation accuracy.

6.As changing the learning rate did not improve the results, 
I added Batch Normalization because it is commonly used to stabilize training and improve model performance

## Things That Failed / Confused Me:
1.I expected increasing dropout to reduce overfitting and improve validation performance, but it actually reduced the validation accuracy.

2.I was surprised that L2 regularization also did not improve the model even though it is commonly used to reduce overfitting.

3.The Batch Normalization experiment confused me the most. I expected it to improve training stability and performance, 
but it turned out to be the worst-performing experiment with a large increase in validation loss and a significant drop in validation accuracy.

4.One thing that confused me was that some techniques which are generally considered useful did not work well on my small custom dataset.

## Insights / Questions I Discovered:
1.I learned that improving a model is not as simple as adding more techniques. A change that helps one model may not help another
And also educing overfitting and improving validation accuracy are not always the same thing.
2.I was surprised to see how much impact a small change like batch size could have on the model's performance.
3.These experiments showed me the importance of testing ideas instead of assuming they will work.

One question I still have is why Batch Normalization performed so poorly on my dataset even though it is commonly used in CNN models???
