# Doodle-to-Actual-Image
This project's goal is turning a doodle into a real image. For further application, user can create a simple app or UX, UI just by a few sketches. This work is planned to follow the following steps:
- Create dataset 
- Build a classification model 
- Build an object detection model
- Replace doodle object into a real object

**Note:** Until now, this work has done step 1 and 2. Hence, the following content will describe only first two step. 

## Create a initial dataset 
The dataset was created by utilizing a provided [tool](http://draw.hasbrain.com/) from [hasBrain](http://www.hasbrain.com/). File **f0**  is the dataset which contains around 3800 images. <br>
**The dataset includes** *14 classes*

0. *Carousel* 197 images
1. *Description* 254 images
2. *Episode* 316 images
3. *Full* 234 images
4. *Grid-view* 282 images
5. *Header* 183 images
6. *Home-marquee* 194 images
7. *Onboarding* 166 images
8. *Portrait-photograph* 182 images
9. *Search-page* 181 images
10. *Sidebar* 178 images
11. *Signup* 278 images
12. *Video-thumbnail* 232 images
13. *Youtube* 301 images

## Build CNN model for classification 
You can find step-by-step I have gone through to build CNN from ipython file which named **_Doodle_Model.ipynb_**
This model achieved 96% f1-score without any data augmentation. In  my opinion, this result is acceptable at this early stage. There are more aspects which should be concerned rather than the accuracy. 

For instance, about the dataset, it is quite small in quantity. In addition, samples in the same class are not different from others too much. It leads to less variant in dataset. The reason is that the dataset was created by a group of about 12 members and at first, we agreed that each class will be drawn with the same form. Thus, if we could build a model which achieve 99% or 100% will not be meaningful much. The main point of this project is the user's experience. So we need to make it more divergent.        

## Demonstration
In this commit, I also made a simple demo which was followed and modified from [Syed Moinudeen](https://github.com/moinudeen/digit-recognizer-flask-cnn). <br>
To run the demo, you open the command promt and change the working place to the **_Demonstration_** folder. 
Then you set <code>set FLASK_APP=app1.py</code> and run <code>flask run</code>. It will return an ID for local web browser, you copy and paste it to chrome to enjoy the demonstration. <br>
Before running the demo, make sure that you installed all necessary libraries in the **_requirements.txt_**. 
