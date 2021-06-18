# Images Creation For Seeker Experiment
You have been directed here because you have experienced problems with the downloaded images: 
- You were unable to launch the Downloaded Pharo Images for the Seeker Experiment. 
- Your images presented a FileSystem writing permission issues.
- Other possibly related issue.
   
Fear not! For you will succeed by following these simple 7 steps:

1. Open your Pharo Launcher, and create two new Pharo 9.0 64bits images. 
   Name them: **Control-Image** and **Seeker-Image** respectively.
2. Launch the **Control-Image**.
3. Open a Playground. Copy and paste the following code. Select it all, and Do It!
```Smalltalk
Metacello new
	baseline: 'SeekerXPImageCreation';
	repository: 'github://maxwills/SeekerXPOverrides:control';
	load.
#SeekerXPImageCreation asClass setupControlImage
```
4. Wait a few moments until there are no more ProgressBars. If there are no errors, close the playground, ***Save and Exit*** the **Control-Image**.
5. Now launch the **Seeker-Image**.
6. Open a Playground. Copy and paste the following code. Select it all, and Do It!
```Smalltalk
Metacello new
	baseline: 'SeekerXPImageCreation';
	repository: 'github://maxwills/SeekerXPOverrides:seeker';
	load.
#SeekerXPImageCreation asClass setupSeekerImage
```
7. Wait a few moments until there are no more ProgressBars. If there are no errors, close the playground, ***Save and Exit*** the **Seeker-Image**.

You are ready to start!. 

We recommend you to create a backup copy of these images before starting the experiment, in case anythying goes wrong.

Good luck!
