# Brainhack Today I Leanrt(TIL) AI Camp 2019 Write-up
This is a write-up of my experience at brainhack TIL AI Camp 2019 hosted by DSTA.  
The source code to what I did as well as the team's final code is in this respository.  
For some explaination of how to use the code and what is going on, read the README.md file of the respective python note books. If there is no README file, there will be some sort of explaination in the python notebook itself.
## Short Version/TL:DR
This was my first experience at a hackathon/coding competition, and was also the first time I was exposed to Artifical Intelligence(AI) and deep learning. Through the camp, we were introduced to the fundementals of deep learning and CNNs for image classification. The challenge was to make a model to classify images into 15 different poses. We managed to get 5th place and won an Amazon Fire 7 tablet for everyone on the team.

## Quick Links
* DSTA
* Brainhack TIL 2019
* Additional Materials

## 1. Intoduction
Note: Before I starting talking about anything, I'd like to point out some things.
* This write-up is based on my experience at the camp, as such it may not fully reflect the views of my teammates/or anyone else for that matter.(If they do make their own write-ups I'll be sure to link them above :D)
* All credit goes to the respective authors of the github repos and downloaded models used in the notebooks.
* When I refer to the AI camp, I am refering to the whole event.
* The competition refers to the time period after the workshop until the 2 days at the EXPO, where the event was held.
* Competition days refer to the 2 days at the EXPO.  

### About the AI camp 2019  

**Information about the camp in general**
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
![Picture of timeline](Content_for_readme/Timeline_of_camp.png 'Picture of timeline')  

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
### About the Team  

The team, .NEET comprised of(In order of the picture, left to right):
* Jes
* David ([Github Profile](https://github.com/David-The-Programmer 'David's GIthub Profile'))
* Me, Chuan Hao
* and Sheen Hern

Here's a picture of us together :D.  
![Picture of the team](Content_for_readme/Picture_of_whole_team.png 'Picture of the team')  

We formed a team together as we mainly knew each other from either secondary or primary school and all had some interest in AI.

My main role was to deal with the technical parts of the project, such as programming and explaining how the model works. With Jes coming up with the idea and first iteration of our final model's architecture.

## 2. My Experience  

This section will mainly be going over my thoughts and experiences I had during certain time periods in the camp. A final summary of my thoughts and reflection on the camp can be found in the next section.

### Workshop/Breiefing

This was pretty exciting to me as I only had a background in python and machine learning before coming to the workshop. Through the workshop, I managed to learn the fundamental basics of deep learning and the common libraries used to implement Convolutional Neural Networks(CNN). Working with classic datasets such as the MNST and CIFAR-10 datasets.  
Furthermore, I managed to get to talk to the mentors that were teaching us, more questions, such as different techniques to improve our model's architecture, as well as what to do later on to prepare for the competition. In addition, I got an insight into how the AI industry is currently developing, such as how AI is implemented into everyday devices and the future of AI as a whole.  
All in all, I was mainly focused on trying to learn as much as I could in these 2 days about AI and deep learning, asking as many questions as I could to the mentors.

### Prep to the competition  

After discussing with the team, we decided to try out 4 separate approaches to the problem.  
1. Re-train an existing well-known model's architecture
2. Do transfer-learning on pre-trained models in keras
3. Implement object detection to crop out the humans doing the poses in order to train a CNN to just classify the humans.
4. Some combination of the above(?)

I was mainly trying the last 3 approaches in order to create a model with the best accuracy. So, for the next week, I created the benchmark models notebook and the object detection notebook you can see in the repo. (albeit I had to clean up a lot of the messy code)  
Through the whole process, I ended up learning how to better work with the keras functional API and the OpenCV library to process images in python. I also worked by looking at other Github repositories to see how they implemented the model for their use case. As a whole, I got a better understanding of how to implement any ideas I had for both the pipeline and model architectures in python.  

The best results I got were 66% validation accuracy by using transfer learning on a pre-trained Xception model on imageNet, with the last 14 layers being trainable.(The last layer was a dense 11 layer, for the 11 classes at the time)

(Sadly I have no pictures of this time period)

### Competition day itself

**Day 1**
I would say this was the most exciting part of the whole camp for me. The experience of being with my teammates, coding together, sharing ideas and helping one another out to try and create the best model we could, was an experience unlike any other.(Looking back it almost seems magical) I would also like to preface the rest of what happened that day with this,
* We were in our first year, first semester in SP
* This was our first experience at a hackathon for everyone on the team
* Everyone did not have much experience in AI before the camp
* We were not expecting to win anything, heck we were just glad to be there in the first place(The jacket was pretty cool.)

At 10AM(I think) was the first time a new test set was released for us to benchmark our model against. This would also be the first time  we would be comparing our model against other teams models. To the shock of everyone on our team, we managed a stagering 79% accuracy on the first test set. This was using Jes's first iteration of the re-trained VGG16 model. We even managed to get on the leaderboards with that score :D. This gave everyone hope that we might actually be able to get some sort of placing. This also showed that maybe, just maybe we could compete witht the university teams. 
Here's a picture:(Sorry for the bad quality)  
![Picture of us on the leaderboard with test set 1](Content_for_readme/Leaderboard_testset_1.png '')  

After this we continued to discus on ways we could try and get more accuracy out of our model, as well as what kind of curveball challenge we would get later on. After lunch, DSTA released test_set_2, alongside with the new train and test set with 4 new classes.  

Who could have thought, 4 new classes and 3 1/2 hours to adapt our model to the new dataset. It took us a few minutes to wrap our head around what we were supposed to do, or rather what we could do. As we did not expect this kind of challenge as a curveball, we had no clue what was the proper way to adapt models to new data and we did not have time to research on that. As such, our team agreed to go with the simplest of solutions, and that was to treat the dataset as a completely new dataset and work from scratch. Looking back, this was probably the riskest course of action we could have taken. We did not know if our model could retrain in time and may not even have a model to submit in the end. We should have tried splitting the team up, with some researching on what we should do and others trying whatever came to mind to atleast have a model to show at the end.  

However, our risky plan worked, to some extent. By treating the dataset as a completely new dataset, we just retrained the whole VGG16 model on the new dataset and hoped it would be as good as before.(We did this on Jes's Laptop) At the same time, I retrained my previous Xception model with the new dataset as well. We did this as I knew from previous experience, my Xception model would only take 1 to 2 hours to retrain from scratch, compared to Jes estimation of around 3 hours for his. We were still hoping for Jes VGG16 model to train in time as we expected his model to have a higher accuracy. Therefore my model acted as a safety net for us if Jes model did not train in time. In the meantime as the model trained, me and Jes worked on cleaning up some of his code for submission. I also got ready the code for submission of our model. 

3 hours and 15 minutes passed, it seems as though Jes model has reached the highest accuracy it would ever reach. It managed to get an impressive 73% validation accuracy. We all agreed this was probably the best accuracy it would get and then submitted that model along with its source code to DSTA. We then began to turn our attention to making slides for pitching/presenting the next day.  

At this point, we once again had no idea what to expect, as on the submission test_set, we got 74.9% accuracy. Thinking nothing of it, we just had fun designing the slides to the best of our abilities as only the top 5 teams with the best accuracy would be preseting. We focused on showing what we did and our process rather then trying to win the competition at this point.  

**Day 2**

As day 2 began, we came back to EXPO not knowing what to expect. On one hand, we really were not expecting to get any sort of placing in the top 5. On the other hand, we really hoped that we did well enough to get top 5. To our surprise again,(I think I'm starting to see a pattern here) we got 5th place in our category and would preseting later on in the day!  
Here the pciture:  
![We managed to get 5th place](Content_for_readme/Top_5_leaderboards.png 'Picture of us in 5th on the final leaderboard')

We bagan cheering among ourseleves and patting each other on the back. We actually did it! As first years in SP and in our first hackathon we actually managed to get something.(Top 5 were guaranteed something) After calming down, we then began thinking on how we would be presenting our slides later on in the day.  

Well as you can expect, we came in 5th in the end after the [presentation](https://drive.google.com/drive/folders/1MCkEaMff1PRF3aO44LmIlMR4ayXcWy1M?usp=sharing 'Link To Google drive with the other resources'):D.  
Photo of us presenting:  
![Photo of us preseting, Credit to DSTA for the photo](Content_for_readme/Presentation.png 'Photo of us presenting')
In the end we won an Amazon Fire 7 tablet for everyone on the team.(Will add picture later on)
Afterwards, we went around to check out the tech showcase being held by DSTA and some people from the industry at EXPO.

Well this concludes my experience in Brainhack TIL 2019 AI camp. I would like to extend my thanks to the people who helped out in the event, DSTA for hosting the event and my teammates for this wonderful experience.

## 3. Conlusion
All in all, the camp not only introduced me to deep learning and AI but also built up my interest in the field as a whole. After talking with some of the people in working in AI in DSTA as well as in the industry, I realised there is still a lot more I can research on and do with AI. The camp also showed me that even now, I can start to look more into AI or any field in IT for that matter.  
I guess the learning point is that age does not really limit what you can do in IT. As long as you go at your own pace, you can achieve great things regards of your age. I am now definitely looking forward to joining more hackathons in the future to not only put my skills ot the test but to also learn more about the vast field of IT.  I am also looking forward to joining the next Brainhack TIL camp next year!  
![Final Image](Content_for_readme/Final_img.png)

(temp)
This is for me to organise this write up
1. Short Version/TL:DR
2. Quick Links
3. Introduction
   + About the competition
   + About the team
4. My experience
   + Workshop/Breif
   + Prep to competition
   + Competition
5. My thoughts as a whole
6. More on the code
