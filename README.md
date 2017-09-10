# Benchmarking Script for Unity

## Status : Working (Windows-Linux-Android)

### Description
Use this script to see how your scene performs and shows on varius devices

### What's new
* Now works for multiple scenes.
* Image outputs now also use numbers for better sorting through quality presets.

### Usage
Note-1 : If you are benchmarking a Google VR scene, Add a GvrHead to the camera
of that scene and disable tracking for both rotation and position to keep the
camera still during benchmarking
Note-2 : If on android go to `Player settings-> Other settings` and change Write Permission to `external`

1. Add the script to an empty object of an empty scene
- Choose the name of the scene (or scenes) to test
- Choose a time offset to allow the scene to "settle" after loading
- Choose how long will the scene run for FPS counting
2. Deploy both scenes to the target device and run
3. The script will load the scene as many times as the quality presets and will
	- Count FPS
	- Take a screenshot
4. Wait for the app to close
5. Retrieve results from the appropriate folder
	- Windows : MyDocuments/UnityBench/
	- Linux   : /home/$USER/UnityBench/
	- Android : /sdcard/UnityBench/

### Contributions / Ideas
Feel free to contact me for these or other ideas you might have :
- You could make the script get the GvrHead component from Google VR camera and disable
it's tracking automaticaly. I am guessing this should be made with reflections method
though, otherwise it would not run on non-GVR projects
- Other Platforms support
- GI settings
- Camera animation
- More options

### Licence
This project is under the MIT licence, FPS counter is my improved version of the Google VR SDK GvrFPS
