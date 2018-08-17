# TASS Movidius Facenet Classifier

[![TASS Movidius Facenet Classifier](images/facenet.jpg)](https://github.com/iotJumpway/TASS-AI/tree/master/Facenet)

The **TASS Movidius Facenet Classifier** uses Siamese Neural Networks and Triplet Loss to classify known and unknown faces, basically this means it calculates the distance between an image it is presented and a folder of known faces. 

The project uses an **UP2 (Up Squared)** the **Intel Movidius** for inference and the [iotJumpWay](https://www.iotjumpway.tech "iotJumpWay") for IoT connectivity. 

![Intel® UP2 & Movidius](../images/UPSquared.jpg)

With previous versions of TASS built using Tensorflow, **TASS Movidius Inception V3 Classifier**, the model had issues with the [Openset Recognition Issue](https://www.wjscheirer.com/projects/openset-recognition/ "Openset Recognition Issue"). **TASS Movidius Facenet Classifier** uses a directory of known images and when presented with a new image, will loop through each image basically measuring the distance between the known image and the presented image, it seems to overcome the issue so far in small testing environments of one or more people. In a large scenario this method will not be scalable, but is fine for small home projects etc. 

Combining **TASS Movidius Inception V3 Classifier** (prone to open set recognition issues) and **TASS Movidius Facenet Classifier** will allow us to catch false positives and verify positive classifications using the name/ID of that prediction to quickly index into the images and make a single calculation to determine if Inception classified the person correctly or not using Facenet and making the project more scalable. The latest Inception version of the classifier will be uploaded to this repository soon.

## What Will We Do?

1. Install the [Intel® NCSDK](https://github.com/movidius/ncsdk "Intel® NCSDK") on a Linux development device.
2. Clone & set up the repo.
3. Install and download all requirements.
4. Prepare your known and testing faces datasets.
5. Test the **TASS Movidius Facenet Classifier** on the testing dataset.
6. Run **TASS Movidius Facenet Classifier** on a live webcam
7. Install the [Intel® NCSDK API](https://github.com/movidius/ncsdk "Intel® NCSDK API") on a Raspberry Pi 3 / UP 2.
8. Upload and run the program on an **UP2** or **Raspberry Pi 3**

**Acknowledgement:** Uses code from Intel® **movidius/ncsdk** ([movidius/ncsdk Github](https://github.com/movidius/ncsdk "movidius/ncsdk Github"))<br />
**Acknowledgement:** Uses code from Intel® **davidsandberg/facenet** ([davidsandberg/facenet Github](https://github.com/davidsandberg/facenet "davidsandberg/facenet"))

## Bugs/Issues

Please feel free to create issues for bugs and general issues you come across whilst using this or any any related iotJumpWay issues.

## Contributors

[![Adam Milton-Barker: BigFinte IoT Network Engineer & Intel® Software Innovator](../images/Intel-Software-Innovator.jpg)](https://github.com/AdamMiltonBarker)



