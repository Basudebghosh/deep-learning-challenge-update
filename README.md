Module 21 Challenge :
deep-learning-challenge :

Links for the COLAB Einviormnet :

AlphabetSoupCarity : https://colab.research.google.com/drive/1B4x1I9RwKOgIXKzUgBW98JCOTLY8BnEO#scrollTo=9eg-BxYoVMZ4

AlphabetSoupCharity_Optimisation :  https://colab.research.google.com/drive/1BHRbaZaUyvEgfuBAOTTQkG-jHs70XTE1#scrollTo=9eg-BxYoVMZ4

Overview : Purpose of this analysis : 
Overall purpose of the neural model analysis is to harness the power of Machine Learning, especially Neural Network, to provide insights, predictions, and guidance for charity organization  to improve the effectiveness and success of their fundraising campaigns. By levering historical data and sophisticated modelling techniques, this analysis empowers charity organizations to make data-based decisions that drive positive social impact and foster philanthropic efforts.	
CLASSIFICATION and APPLICATION_TYPE are the target variables.	
EIN, NAME, AFFILATION, ORGANIZATION, STATUS, INCOME_ATM, SPECIAL CONSIDERATIONS, ASK_ATM and USE_CASE are the features variables.
STATUS column has a constant vale for all entries, it would not contribute model’s learning and can be dropped.
SPECIAL CONSIDERATIONS could be dropped as it does not have influence for the success prediction of the model.
ORGANIZATION could be dropped if it does not provide significant information related to the success of the campaign.
Three layers :1. First hidden layer, 2. Second hidden layer and, 3. Output layer has been used.
Used activation functions for the normal model are : 1.  ‘LeRU’ and 2. ‘Sigmoid’.
Reasons behind the usage of the these activation functions : Basically, activation functions introduce non-linearity to the network, enabling it to learn complex relationship between inputs and outputs.
Generally, the activation function “ReLU’ (Rectified Linear Unit), is used for the hidden layers and “Sigmoid” for the output layers. The Sigmoid function provides result is term of Probability where values lie between 0 to 1. Means that the model provides accuracy from 0% to 100% (e.g., 0.0, 0.5 and 1.0 provide the accuracy for the model 0%, 50% and 100% respectively) and it is easily understandable for the model’s accuracy/performance from the values between 0 to 1. 
Reasons behind used different layers : The number of layers determines the depth of the neural network. Deeper layers (more layers) can capture more complex features and will provides better accuracy of the model.
The accuracy of the original model is 62.2%. To improve the accuracy of the model following steps has been taken:
1.	Have dropped another features “SATUS” and “SECIAL_CONSIDERTION” reduction of bins of top 8 categories.
2.	Increased First hidden layer from 80 units to 100 units.
3.	Increased both first hidden layer by 20 units and second hidden layer by 10 units.
4.	Replaced activation function in second layer “LeRu” by “Tanh”
5.	Increased the Epoch from 80 to 100.

Summary: The accuracy ofthe orinial model is 62.3%. This accuracy is not great, but this model can support the faund raising for the Charitable organization is some extent.

Even though different steps has been taken to optimize model’s accuracy/performance, but it does not improve overall  performance from the original model. The improvement of the performance is very minimal. Droping more features and binning top eight featues just improve 0.8% accuracy. All other alternatiove combinations does not imprve accuracy from the Original model's accuracy 62.3 %.

Recommendation: To improve the accuracy of the model, we can consider exploring different models and techniques. One of the potential alternative models to consider is Random Forest. The Random Forest Classifier is an ensemble learning method that builds multiple decision trees and combines their predictions to make final decisions. It has proven to be effective for various classification tasks and can be particularly useful when dealing with complex and high dimensional data like this use case Charity Classification problem.

Random Forest is capable of capturing non-linear relationship between features and target variables. Unlike neural network, it does not require explicit features scaling and can handle a mix of categorical and numerical features with ease.
Random Forest provides a measure of feature importance that allowing us to identify which features are most influential in making prediction.
By combining multiple decision trees, the Random Forest can reduce Overfitting and improve generalization. It averages out biases and errors from individual trees, leading to more robust predictions.
Random Forest can interoperate in ease and gains insights into mole’s decision-making process in compared to the deep neural network.
Random Forest generally requires less training time in compared to the neural network.

Conclusion: We can conclude that the Random Forest classifier can be viable alternative to the deep neural network for the charity classification problem, offering better interpretability, handling non-linearity effectively, and potentially achieving improved accuracy.
















											

