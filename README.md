# Brainhack Today I Leanrt(TIL) AI Camp 2019 Write-up
This is a write-up of my experience at brainhack TIL AI Camp 2019 hosted by DSTA.  
The source code to what I did as well as the team's final code is in this respository.  
For some explaination of how to use the code and what is going on, read the README.md file of the respective python note books. If there is no README file, there will be some sort of explaination in the python notebook itself.
## Short Version/TL:DR
This was my first experience at a hackathon/coding competition, and was also the first time I was exposed to Artifical Intelligence(AI) and deep learning.  

## Quick Links

## 1. Intoduction
Note: Before I starting talking about anything, I'd like to point out some things.
* This write-up is based on my experience at the camp, as such it may not fully reflect the views of my teammates/or anyone else for that matter.(If they do make their own write-ups I'll be sure to link them above :D)
* All credit goes to the respective authors of the github repos and downloaded models used in the notebooks.
* When I refer to the AI camp, I am refering to the whole event.
* The competition refers to the time period after the workshop until the 2 days at the EXPO, where the event was held.
* Competition days refer to the 2 days at the EXPO.
### About the AI camp 2019
This camp was hosted by the Defence Science and Technology Agency ([DSTA](https://www.dsta.gov.sg/home 'DSTA Homepage')) as part of their larger event, Brainhack, held every year.(I think)  
The homepage of the camp can be found here.([Brainhack Today I Learnt 2019(TIL)](https://dsta.gov.sg/til 'TIL Homepage'))  
The github profile for the camp(and hopefully future camps) can be found [here](https://github.com/brainhack-dsta 'DSTA brainhack-til github profile') 

The camp was meant as both a workshop and competition for people who were interested in AI.  
The camp however focused on the more specific section of computer vision and using deep learning models to do image analytics.  
The competition's objective was to build a model to classify the pose of the human in an image into their respective classes. 
The training, validation and test dataset was provided by DSTA themseleves.

This camp was held for students from Junior Colleges(JC/IP), Polytechnics(Poly), Institute of Technical Education(ITE) and Universities(Unis) in Singapore.  
The students are then split into 2 seperate categories, Poly/Uni and JC/IP/ITE.  

The timeline of the event was split into as such:  
![Picture of timeline](https://github.com/chuanhao01/Brainhack_TIL_2019-write-up/blob/markdown/Content%20for%20readme/Timeline%20of%20camp.png 'Picture of timeline')  

**Workshop**  
The camp was structured such that we had a workshop before the competition started so as to give everyone some knowledge on how to create deep learning CNN models for image classification.(4/6/2019)  
The workshop used the classic MNST and CIFAR-10 datasets to teach us the basic of deep learning CNNs.  
**Breifing**  
We then had a breifing 2 days later, where the training and validation datasets were realsed to us. We then had a week to build our models for the competition.  
The original dataset released to us had 11 classes and a total of around 1000 images for both the training and validation dataset.

The workshop and breifing were held at DSTA offices.  

**Competition**  
The competition was held at the EXPO max atria.(Level 2) On the day itself 3 test datasets and a new training and validation dataset were released.  
This was due to a curveball challenge given to us on the afternoon of the first competition day. They gave us around 3 1/2 hours to adapt our models to 4 new classes.

The day was structured as follows:  

For the First day.
| Time    |                     Activity                     | Remarks                                                                                                    |
| :------ | :----------------------------------------------: | ---------------------------------------------------------------------------------------------------------- |
| 10.00AM |            Release of the test_set_1             | This test set was based on the train and validation set given at the start of the competition (11 classes) |
| 1.30PM  |        Release of the curveball challenge        | New train and validation datasets were released. (4 new classes)                                           |
| 5.00PM  |             New test_set_2 released              | This allowed us to benchmark our model against a test set we have not seen                                 |
| 5.30PM  |     Release of the final_submission_test_set     | We were only allowed one submission for the final test set                                                 |
| 6.00PM  | Deadline of submission for source code and model | Slides were due the next day 8.00AM                                                                        |

For the Second Day.(Not to sure about the accuracy of the timing)
| Time    |               Activity               | Remarks                                                                                                 |
| :------ | :----------------------------------: | ------------------------------------------------------------------------------------------------------- |
| 10.30AM | Pitching/Presentation of top 5 teams | This was when the team's with the top 5 accuracy in the final submission had to present on their models |
| 3.00PM  |          Release of results          | Nuff Said                                                                                               |
### About Myself


(temp)
This is for me to organise this write up
1. Short Version/TL:DR
2. Quick Links
3. Introduction
   + About the competition
   + About me
   + About the team
4. My experience
   + Workshop/Breif
   + Prep to competition
   + Competition
5. My thoughts as a whole
6. More on the code
