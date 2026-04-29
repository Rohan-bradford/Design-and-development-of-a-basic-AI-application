Coursework Description
Application of AI methods for multimodal
heart disease diagnostic
Background
Health applications are one of the fields in which artificial intelligence will play a major role. Not
only can monitoring patients’ health be studied, but also preventive actions aimed at the early
detection of diseases. Therefore, different types of data, including records of age, weight, blood
type and pressure, diet type, smoking, etc., can be used to detect the risk of developing illnesses,
such as cardiovascular diseases.
In addition, image processing applied to radiography can be used to detect certain anomalies, such
as heart anomalies. Therefore, both modalities, tabular data and X-ray images, can be processed
with artificial intelligence techniques to indicate the presence or the potential risk of developing
such diseases. However, this tool cannot replace medical knowledge and expertise and must be
limited to a decision-support role. Furthermore, the analysis of input data using AI techniques can
provide a better understanding of the role of each characteristic in the development of the
diagnosed disease(s).
Scope and tasks
Using two datasets, one for tabular data of patient health about cardiovascular diseases, and the
other for X-ray images about heart anomalies, we aim to develop artificial intelligence techniques
to detect the presence of each disease from the corresponding datasets.
Task1- heart disease severity classification using tabular data
Using Dataset1, concerning patient health records, the data are presented in tabular form. The aim
is to use the data present as features and labels, to train a model capable of detecting the presence
or the level of the illness (from 0: no illness to 4: severe illness). Therefore, our first aim is to build:
a) A binary-classification model, to detect the presence of a heart disease. In this case, any
label in the last column (level) above 0 is considered as illness.
b) A multi-class classification model, to detect the level of the heart illness, using a multi-
class classifier.
However, not all features (column 2:age) to (column 15: thal) could be equally useful. Therefore,
feature selection can be taken into consideration during the development of the models. Besides,
feature normalisation or standardisation, may be required to reduce the data sparsity.
2
Input features
The following list contains a description of the different features and their values:
 id: (Unique id for each patient)
 age: (Age of the patient in years)
 sex: (Male/Female)
 origin: (place of study)
 cp: chest pain type: 1. typical angina; 2. atypical angina; 3. non-anginal; 4. asymptomatic
 trestbps: resting blood pressure (resting blood pressure (in mm Hg on admission to the
hospital))
 chol: (serum cholesterol in mg/dl)
 fbs: (if fasting blood sugar > 120 mg/dl)
 restecg: (resting electrocardiographic results)
 Values: [normal, stt abnormality, lv hypertrophy]
 thalach: maximum heart rate achieved
 exang: exercise-induced angina (True/ False)
 oldpeak: ST depression induced by exercise relative to rest
 slope: the slope of the peak exercise ST segment
 ca: number of major vessels (0-3) colored by fluoroscopy
 thal: [normal; fixed defect; reversible defect]
Note! The first column (Id) is not considered as an input feature.
Output labels
The output label is:
 The last column “level” indicates the predicted attribute (0 shows no disease and 1, 2, 3
and 4 shows different level of disease)
 This label can used as it is for multiclass classification. However, for binary classification,
labels must be converted into two values (0/false: if the original label is 0, and 1/True: if
the original label is above 0).
Required AI techniques
To carry this project, it is required to follow these guidelines:
 Use more than one classification model, compare their performances for each classification
task (binary or multiclass).
 Classification models should firstly be implemented with the methods studied in this
module, namely Decision trees, naïve Bayesian, Random forests, linear classifiers, linear
SVM, Artificial Neural Networks and Deep Neural Networks.
 Other classification methods can be used (optionally), however only for comparison with
the studied methods.
 To improve the performance, you can use different architectures or settings for each
method.
 Performance must be assessed using standard evaluation metrics, such global accuracy, and
class-wise precision, recall and f1-score.
 Findings must be discussed and commented.
3
Task 2- Heart disease detection using X-ray images
Using Dataset 2, containing X-ray images of the chest, we aim to classify them into presenting
signs of heart disease or not.
The dataset comprises 17 folders of images, each containing images of the related disease, i.e.
{Abscess, Ards, Atelectasis, Atherosclerosis of the aorta, Cardiomegaly, Emphysema, Fracture,
Hydropneumothorax, Hydrothorax, Pneumonia, Pneumosclerosis, Post inflammatory changes,
Post traumatic ribs deformation, Sarcoidosis, Scoliosis, Tuberculosis and Venous congestion}.
However, only the following are directly related to heart anomalies:
 Atherosclerosis of the aorta
 Cardiomegaly
 Pneumonia
 Pneumosclerosis
 Post-inflammatory changes
 Post-traumatic ribs deformity
Therefore, we aim to implement a binary classifier to classify images into heart-related or non-
heart-related diseases, as explained above.
However, the input must be the raw image, without any prior feature extraction, and therefore the
most suitable AI technique must be selected, e.g. convolutional neural networks (CNN).
Task 3- Image reconstruction and denoising
Also using Dataset2 for X-ray images, it would be interesting to exploit generative models, such
as Simple or Variational Autoencoders (VAE) and/or Generative-Adversarial Networks (GAN)
to improve the quality of images by reconstruction from clean (original) images or from noisy
images (by adding an artificial noise). This can provide a model that helps to use low-quality
images by applying reconstruction/enhancement before classification.
Problem statement
Diagnosis of disease using multimodal data, i.e. medical records and/or radiographic images, can
be approached as a classification problem:
 Collect the datasets (see the AI_CW2_2025-2026_Material folder in Canvas/Learning
Material), and analyse the data contained in each one (tabular medical records in the
Dataset1 and radiographic images in Dataset2). The data need to be divided into training
and test sets. When necessary, carry out the necessary preprocessing steps, such as
normalisation, standardisation or cleaning.
 For Dataset1, about patient health data, develop several classification models as
mentioned above in Task1.
 For the X-ray image dataset, develop:
o A classification model in which the input is the raw image and the output is the
heart-related / non-heart-related disease label, (see the list of heart-related diseases
in the description of Task2)
4
o A generative model, in which the input is a low-quality or a noisy image and the
output is a clean image. In this case, noise can be artificially added to the images
in the dataset, as a random Gaussian noise (see description of Task3).
 The evaluation of developed models must be included as follows:
o For classification models (developed on each dataset), the confusion matrix and
underlying evaluation metrics such as overall accuracy and precision per class,
recall and F1 score. An interpretation of each measure must be provided.
o For the image reconstruction/enhancement model, assess the quality of denoising
by measuring the corresponding metrics, including the absolute and the relative
root mean square error.
 Implement a program that allows the user to enter the patient’s tabular data and/or
uploading an X-ray image, as input, to provides the detected disease(s) as output, using
the developed models. The program may also apply a reconstruction step to clean the
upload images, before performing classification.
 Discuss the results obtained, making recommendations for further investigation and better
implementation.
 Show how the developed models can have an impact on accelerating the health
monitoring process and the precautions to be taken to avoid misuse of patient data or any
other ethical issues related to the application of AI in the healthcare sector.
 Write a report of 1000 (at minimum) to 1500 (at maximum) words to present your
work and the results obtained
 Present your code as a python notebook (.ipynb file).
