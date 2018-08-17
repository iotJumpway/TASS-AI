# TASS Movidius Facenet Classifier

[![TASS Movidius Facenet Classifier](images/facenet.jpg)](https://github.com/iotJumpway/TASS-AI/tree/master/Facenet)

The **TASS Movidius Facenet Classifier** uses Siamese Neural Networks and Triplet Loss to classify known and unknown faces, basically this means it calculates the distance between an image it is presented and a folder of known faces. The project uses an UP2 the Intel Movidius and the [iotJumpWay](https://www.iotjumpway.tech "iotJumpWay") for IoT connectivity. 

With previous versions of TASS built using Tensorflow, the model had issues with the [Openset Recognition Issue](https://www.wjscheirer.com/projects/openset-recognition/ "Openset Recognition Issue"). **TASS Movidius Facenet Classifier** uses a directory of known images and when presented with a new image, will loop through each image basically measuring the distance between the known image and the presented image. In a large scenario this method will not be scalable, but is fine for small home projects etc. 

One way to build a more scalable version would be to use **TASS Movidius Inception V3 Classifier** (prone to open set recognition issues) and verify positive classifications using the name/ID of that prediction to quickly index into the images and make a single calculation to determine if Inception classified the person correctly or not.

**Acknowledgement:** Uses code from Intel® **movidius/ncsdk** ([movidius/ncsdk Github](https://github.com/movidius/ncsdk "movidius/ncsdk Github"))
**Acknowledgement:** Uses code from Intel® **davidsandberg/facenet** ([davidsandberg/facenet Github](https://github.com/davidsandberg/facenet "davidsandberg/facenet"))

## Bugs/Issues

Please feel free to create issues for bugs and general issues you come across whilst using this or any any related iotJumpWay issues.

## Contributors

[![Adam Milton-Barker: BigFinte IoT Network Engineer & Intel® Software Innovator](../images/Intel-Software-Innovator.jpg)](https://github.com/AdamMiltonBarker)



