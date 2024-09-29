# Smart-RGB-Lighting-Control-with-Hand-Gesture-Recognition
This project enables control of RGB lighting through intuitive hand gestures, utilizing OpenCV for gesture recognition and Firebase for cloud connectivity. Users can seamlessly adjust the color of lights, selecting from 32 unique RGB combinations (2^5) for a customizable and interactive lighting experience. 
# AIM 
To Interface OPEN CV With Firebase and communicate with Esp 32 
# Procedure 
## Steps to follow 
1. Here we are using the PyCharm For coding
   * Download the PyCharm Community Edition ----> https://www.jetbrains.com/pycharm/download/?section=windows
2. IF you dont have python interpreter download
3. Create new project With attaching the python interpreter
4. open the new project ----> File ----> setting ---->[Name of the New project] ----> Python interpreter install librarys
5. opencv-python
6. mediapipe
7. firebase-admin
8. OR Install using command prompt
9. Librarys --->
   *  pip install opencv-python
   *  pip install mediapipe
   *  pip install firebase-admin
   ### requirements.txt: List of Python dependencies. You can include:
     ```
     opencv-python
     mediapipe
     firebase-admin
     threading
     ```
# Error
* installing on mediapipe library
* If it causes issues, delete the MediaPipe library, create a new project, and install it through PyCharm.
* If it doesn't solve the issue, copy the error message and Google it to identify the cause. If needed, try redoing the above process. The errors may vary by computer, and in some cases, turning off Windows protection can help.
# Esp 32 
 ## Aim 
 To interface Neo pixel led with Esp 32 & and communicate with firebase 
# Components
 * Neo Pixel Led
 * Esp 32
 * ![neo](https://github.com/user-attachments/assets/72435451-81f4-4ab4-8b95-6d8050998a6e)
# Procedure
 * Create a ESP 32 Project On Visual Studio Code With Arduino FrameWork
 * Interface ESP 32 microcontroller with Neo Pixel Led and do an Example code .
    *  Library ---> lib_deps = adafruit/Adafruit NeoPixel@^1.12.3
 * Create a Firebase Project For Read the RealTime Data
 * Collect The network credentials, URL database, and project API key ,Email ,Password
 * Install the Firebase-ESP-Client Library.Then, program the ESP 32 to Interface with Firebase
    * Library ---> lib_deps = mobizt/Firebase Arduino Client Library for ESP8266 and ESP32@^4.4.14
 * Insert your network credentials To the project work.
# Code 
```
#include <Adafruit_NeoPixel.h>
#ifdef __AVR__
  #include <avr/power.h>
#endif
#define PIN        13
#define NUMPIXELS  10

Adafruit_NeoPixel pixels(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);
#define DELAYVAL 200

void setup()
{
  pixels.begin();
}

void loop()
{
  pixels.clear();

  for(int i=0; i<NUMPIXELS; i++)
  {
    pixels.setPixelColor(i, pixels.Color(0, 150, 0));
    pixels.show();
    delay(DELAYVAL);
  }
}
``` 
# Output
![VideoCapture_20240929-125836](https://github.com/user-attachments/assets/e15ad220-0128-44cb-859b-c2df5fce689d)
![VideoCapture_20240929-125756](https://github.com/user-attachments/assets/fb54dc84-94ea-43e9-9d4f-e3c87d88a72c)
![VideoCapture_20240929-132754](https://github.com/user-attachments/assets/caf94cc3-65d9-4546-86f8-fc940a4d01dc)





 
