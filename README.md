# Images Creation For Seeker Experiment
Having problems with the downloaded Pharo Images? Build them yourself! (You will need both images: Control and Seeker)

## Update the VM
First, you'll need to update your Pharo 9.0 x64 VM doing this ([As shown in this image](https://drive.google.com/file/d/1x-UUSrTTKNmi_6Gbh39Et_TACUprj8sb/view?usp=sharing)):
1. In your Pharo Launcher, click the VMs button at the top right.
2. Select the VM for Pharo 9.0 x64.
3. Click the Update button in the toolbar.


## Control-Image
 1. Create a new **Pharo 9.0 64bits** image, name it **Control**. Launch it, open a Playground, copy & paste the following code and **Do it!**.
 ```Smalltalk
Metacello new
	baseline: 'SeekerXPImageCreation';
	repository: 'github://maxwills/SeekerXPOverrides:control';
	load.
#SeekerXPImageCreation asClass setupControlImage
```
 2. Wait a few moments. A notification will popup at the bottom left when the setup is complete. Save the image. The Control-Image is ready to start the experiment. Close it now. The Experiment's Instructions will tell when you should use this image. 

## Seeker-Image
1. Create a new **Pharo 9.0 64bits** image, name it **Seeker**. Launch it, open a Playground, copy & paste the following code and **Do it!**.
```Smalltalk
Metacello new
	baseline: 'SeekerXPImageCreation';
	repository: 'github://maxwills/SeekerXPOverrides:seeker';
	load.
#SeekerXPImageCreation asClass setupSeekerImage
```
 2. Wait a few moments. A notification will popup at the bottom left when the setup is complete. Save the image. The Seeker-Image is ready to start the experiment. 
Close it now. The Experiment's Instructions will tell when you should use this image. 

We recommend you to create a backup copy of these images before starting the experiment, in case anythying goes wrong.

Good luck!
