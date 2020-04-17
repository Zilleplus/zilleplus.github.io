---
title: project computer vision
permalink: /projects/computervision
---
# Project computer vision
This project was realized for the class [Computer vision](https://onderwijsaanbod.kuleuven.be/syllabi/e/H02A5AE.htm#activetab=doelstellingen_idp29371552) related to the Master Mathematical engineering.



## The problem
A bunch of x-ray pictures where provided(Figure1 right). Some of the pictures had landmarks that show the border of the 4 frontal teeth.(see Figure1 left) The algorithm should determine the borders of the 4 frontal teeth for the pictures without landmarks.
<center>
    <div>
        <a href="url"><img src="./img/computerVisionLandmarks.png" align="center" height="200" width="300" ></a>
        <a href="url"><img src="./img/computerVision_teeth_pic.png" align="center" height="200" width="300" ></a>
    </div>
    Figure1: left Landmarks on teeth, right full picture
</center>

## Final algorithm
### Active shape models
These models use PCA analysis to find principles components of a teeth. These components can then be used to build a new teeth. First 10 principle components are illustrated in Figure2 after the average teeth. The average teeth is obtained by adding together all the principle components each multiplied by there corresponding eigenvalues.

<center>
    <div>
        <a href="url"><img src="./img/computerVisionPCA_models.png" align="center" height="200" width="300" ></a>
    </div>
    Figure2: PCA components
</center>

### Step direction fitting algorithm
After determining a model with PCA analysis. The shape of a average teeth can be approximated by the model, displayed in Figure3. The normal on each following pair of data points is also printed out. This will be the search direction.
<center>
    <div>
        <a href="url"><img src="./img/computerVision_normals.png" align="center" height="200" width="300" ></a>
    </div>
    Figure3: Landmarks on teeth
</center>

### Fitting algorithm levels
After reading an interesting paper on these active shape models, it seems a multi level approach is the best option. Figure4 illustrates the resulting shapes after each level.
<center>
    <div>
        <a href="url"><img src="./img/level0_fitting.png" align="center" height="200" width="170" ></a>
        <a href="url"><img src="./img/level1_fitting.png" align="center" height="200" width="170" ></a>
        <a href="url"><img src="./img/level2_fitting.png" align="center" height="200" width="170" ></a>
    </div>
    Figure4: The same white shape in all 3 figures is the starting position of algorithm. The left figure has in grey the shape after level0 fitting, the center level1 fitting and the right level2 fitting
</center>

### Final remark
Although it's not included in the class it's possible to use system identification here. The landmarks here always had the same amount of points. Ths obviously will not always be the case. The landmarks could be represented by for example an ARMAX model instead of fixed points.

View project on [Github](https://github.com/Zilleplus/Project_computer_vision)
