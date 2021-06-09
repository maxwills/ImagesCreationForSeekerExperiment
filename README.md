# Images Creation For Seeker Experiment
You have been directed here because you were unable to launch the Downloaded Pharo Images for the Seeker Experiment.  
Fear not! For you will succeed by following these simple 7 steps:

1. Open your Pharo Launcher, and create two new Pharo 9.0 images. 
   Name them: **Control-Image** and **Seeker-Image** respectively.
2. Launch the **Control-Image**.
3. Open a Playground. Copy and paste the following code. Select it all, and Do It!
```Smalltalk
Metacello new
    baseline: 'SeekerExperiment';
    repository: 'github://StevenCostiou/SeekerExperiment:single-task-list-from-files';
    load.

Metacello new
    baseline: 'SeekerXPOverrides';
    repository: 'github://maxwills/SeekerXPOverrides:control';
    load.

(IceRepository repositories select: [:r| r name='SeekerXPOverrides']) first discardChanges.

#SeekerExperiment asClass instrumentSystemForSeeker
```
4. Wait a few moments until there are no more ProgressBars. If there are no errors, close the playground, ***Save and Exit*** the **Control-Image**.
5. Now launch the **Seeker-Image**.
6. Open a Playground. Copy and paste the following code. Select it all, and Do It!
```Smalltalk
Metacello new
    baseline: 'SeekerExperiment';
    repository: 'github://StevenCostiou/SeekerExperiment:single-task-list-from-files';
    load.

#SeekerExperiment1 asClass controlOrSeeker: #seeker.

Metacello new
    baseline: 'Seeker';
    repository: 'github://maxwills/SeekerDebugger:seeker-xp';
    load.
    
#SeekerDebuggerPresenter asClass showInDebugger: true.

Metacello new
    baseline: 'SeekerXPOverrides';
    repository: 'github://maxwills/SeekerXPOverrides:seeker';
    load.

(IceRepository repositories select: [:r| r name='SeekerXPOverrides']) first discardChanges.

#SeekerExperiment asClass instrumentSystemForSeeker
```
7. Wait a few moments until there are no more ProgressBars. If there are no errors, close the playground, ***Save and Exit*** the **Seeker-Image**.

You are ready to start!. 

We recommend you to create a backup copy of these images before starting the experiment, in case anythying goes wrong.

Good luck!
