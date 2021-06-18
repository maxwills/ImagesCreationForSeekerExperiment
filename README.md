# Images Creation For Seeker Experiment
Having problems with the downloaded Pharo Images? Build them yourself! (You will need both images: Control and Seeker)

Using an ***updated Pharo Launcher*** (latest version) with ***latest VMs***:

## Control-Image
 1. Create a new **Pharo 9.0 64bits** image, name it **Control**. Launch it, open a Playground, copy & paste the following code and **Do it!**.
 ```Smalltalk
Metacello new
	baseline: 'SeekerXPImageCreation';
	repository: 'github://maxwills/SeekerXPOverrides:control';
	load.
#SeekerXPImageCreation asClass setupControlImage
```
 2. Wait a few moments. A notification will popup at the bottom left when the setup is complete. Save the image. The Control-Image is ready to start the experiment. 

## Seeker-Image
1. Create a new **Pharo 9.0 64bits** image, name it **Seeker**. Launch it, open a Playground, copy & paste the following code and **Do it!**.
```Smalltalk
Metacello new
	baseline: 'SeekerXPImageCreation';
	repository: 'github://maxwills/SeekerXPOverrides:seeker';
	load.
#SeekerXPImageCreation asClass setupSeekerImage
```
 2. Wait a few moments. A notification will popup at the bottom left when the setup is complete. Save the image. The Control-Image is ready to start the experiment. 

We recommend you to create a backup copy of these images before starting the experiment, in case anythying goes wrong.

Good luck!
