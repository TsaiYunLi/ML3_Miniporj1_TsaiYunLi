# ML3_Miniporj1_TsaiYunLi
This is a Kaggle competition project just for the purpose of practicing deep learning algorithms, since it has ended years ago. The competition name is "Histopathologic Cancer Detection," which raised a binary class image classification problem where we need to "identify metastatic cancer in small image patches taken from larger digital pathology scans", quoting the original words on the Kaggle platform. Please see the reference section for the Kaggle competition link. <br>

To solve this problem, I will built two hybrid models: <br>
ImageNet_ANN_full_model = ImageNet_CNN + ANN_classifier <br>
ImageNet_SVM_full_model = ImageNet_CNN + SVM_classifier

The ImageNet_SVM_full_model, with a training subset AUC of 0.9137, and a validation subset AUC of 0.8073, performs much better than the ImageNet_ANN_full_model. Thus, I used ImageNet_SVM_full_model to predict the test images' labels, which turns out to have a test dataset AUC of 0.7804, a score for the Kaggle leaderboard position of about 1068. This score is not bad but also not ideal. This might be caused by the fact that, due to limited computer resources, I did not feed the entire, very large training dataset but 800 randomly sampled training images and 200 validation images in the model during its training phase, potentially causing some overfitting and inaccuracy in the models' prediction power. Also because of the limitation on computer resource, when predicting labels for the entire 57458 test images , it took a long time to run on the Kaggle notebook environment. It ran 1796 iterations with 2s/step and 2897s in total, which is a crazy long time. 

If I were to redo this project, instead of using Kaggle notebook with limited computer resource, I would try to figure out how to input the Kaggle datasets from a local environment of a computer with many GPUs or a cloud environment for unlimited computation power. When the computation resource limitation is lifted, my models would probably make better predictions and score higher.

Please point out what else I need to adjust to improve my model's prediction power. Your suggestions and advice are very welcomed!

Please do not use my code or text without proper citation, thank you!
