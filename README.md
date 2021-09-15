# RGB-based-Andorid-Malware-detection
 please follow the instructions to install and run the code. 
 
 **System Requirement and Installation: **

1.Install Ubuntu
2.	Install Anaconda, for  python


**Download Dataset, Pre processing and Training a Malware Detector**

1. Download the AndroZoo dataset, containing benign and malware APKs.
2. APKs can be downloaded from an API by providing an APK SHA256 hash by using the following script.(Downloading_APKs.ipynb) Both API and APK’s SHA256 are given by AndroZoo. 
3. Extracting androidmanfestfiles.xml and classes.dex file from an APK by using Androguard
4.	Converting an APK to an image (fileName:APK_to_images(Androguard_and_preDefined_Values)_Version_2.ipynb).
   a). Extract different properties from all these extracted files.
   b). Converting those properties to an integer values (predefined + calculation)
   c).	Can select custom APKs based on publishing date, number of vt_detection (detected by # of softwares in VirusTotal) etc.
   d). Place different properties on different channels.
   e). Interpolate all channels to a fixed size.
   f).	Merge all channels to make an image.
   
5. Training a Deep Learning Model
  a). 	Converting APKs images to .npy file for training a model.
  b). 	Load .npy file to train model
  c). 	Make labels, ‘0’ for benign and ‘1’ for malware.

**Implementing DroidDetector (P1)**

6.	DroidDetector based on binary vectors
  a). First extract different  properties from an APK to file using script
  b). Convert those properties to a binary vector (Preprocessing for DroidDetector). (APK2Vector)
  c).	Train DNN model on binary vector using following script

**Implementing Malware Detection Based on CNN  DeepClassifyDroid (P9)**

7.	Malware Detection Based on CNN
  a).	First extract different  properties from an APK to file using script
  b).	Pre processing 
  c).	Train a CNN model

**Generating Adversarial Examples**

8.	Generating Adversarial Examples with Pre defined benign properties (Attack1:-FileName: Generating_Random_benign)
  a).	Convert an APK to image.
  b).	Append benign properties.
  
9. **Generating bening APKs using GANs (Attack2)**
  a).	Generating benign APKs using DCGAN
  b).	Generating benign APKs using WGAN
  c).	Generating benign APKs using LSGAN

**Attacks on Models**

10.	Attacks on own model, P1 and P9 Detectors

○	Attack via Attack1
■	Own Detector
■	P1
■	P9
○	Attack via Attack2
■	Own Detector
■	P1
■	P9
![image](https://user-images.githubusercontent.com/29942534/133421921-b451f3e4-d0a2-4607-a9a7-c17bcb70eba4.png)
