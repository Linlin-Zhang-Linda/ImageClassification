# ImageClassification

## Overview

* This is an image classifier for TensorFlow Lite on iOS. It use Image classification to classify what it sees from the device's back camera, using a pre-trained model. The application must be run on device.

## Data collection
download some images to local or Google Cloud Storage
* [Stanford Dogs Dataset](http://vision.stanford.edu/aditya86/ImageNetDogs/)
* Google(collect cats images)

## Train the data->get the model
1.upload your image files

2.use AutoML(GCP) to train the data

3.Use the model(clik TF Lite)

4.download the files: dict.txt; model.tflite

## Deploy the model to iOS
 [reference](https://github.com/tensorflow/examples/tree/master/lite/examples/image_classification/ios)
* install Xcode command-line tools `xcode-select --install`
* install CocoaPods `bash sudo gem install cocoapods`

Note: The demo app requires a camera and must be executed on a real iOS device. You can build it and run with the iPhone Simulator, but the app will raise a `Camera not found`exception

* `bash git clone https://github.com/tensorflow/examples.git`
* `bash cd examples/lite/examples/image_classification/ios pod install` 

Note: If you have installed this pod before and that command doesn't work, try `pod update`

* `bash open ImageClassification.xcworkspace`

Note:Xcode 10.0 or above
* open the `ImageClassification` project

Note:open the xcworkspace and don't open the xcodeproj directly
* add the model and .txt in it
* click **Signing&Capabilities** ->choose the **Team**
->add your initials and a number to the end of the string in **Bundle Identifier**
* connect your device(with iOS 12.0 or above)
* run it!

## result
![alt text](https://drive.google.com/uc?id=1RfW-DqqNtTJcsldZGBuvyJsfeK-QRvbd)
![alt text](https://drive.google.com/uc?id=1SL_0Mce4ihOxhL-HiHoqSg0ueSkOD9Mg)
