### Preface
This is intended to be a joke-ish general quiz for a certain someone to study up on DSA/OOP main points. Therefore, any scenarios with correlations to what actually happened/will happen is not intended (Please do not stab me thanks). As these questions are made intentionally as a storyline, some questions may correlate to each other, however answers do not have any correlations whatsoever. All questions may have multiple valid answers, each question may have subquestions, bonus points if you manage to find sub-answers/what group each answer is in. **All sections in a code block will not contribute to your answer, you should ignore them while figuring out your answer.**  To make you actually go study and not guess everything, there will be no MCQs. Mizuki will hold the intended solutions and/or explanations if necessary.

### Scenario
```
The day has arrived, and both Mizuki and Hoshino, your friends have arrived at the airport. They would be staying here for a few days, to see through your graduation thesis. However, for you, this is the first time in quite a few years that you've seen Hoshino, your girlfriend, again. You know she's very physical and straightforward, so maybe there is some silver lining for you to expect?
```

### Question 1:
#### Problem statement: 
```
Although not much happened upon their arrival, things start to kick off fast in the morning, as Hoshino decides to ask you out on a date, and you agreed. And so off you went with her for some work, and quite a bit of fun in between. However, unknowingly in the background, consequences of doing things half-heartedly strikes fast as the slides you sent to your supervisor on review is sent back to you with a lot of comments. Mizuki, who's staying at home knowing that it's impossible to work on this on her own, while feeling reluctant to call you when you are out, decided to call in a favor from a friend (who shall now be called Friend M) to solve this problem.
```

"What the f-", M exclaimed as he's reading through your reviewed slides. The slides are filled to the brim with remarks of your own errors, however he's analyzed through the comments and broken down to 3 big problems, tackling them one by one and breaking each problem down further as he goes:
- Missing meaningful title 
- Pictures with no context or overflowed
- Words in slides that give no meaning to the presentation
The list of problems is sorted by importance, and he's solving each one from the most crucial to the least crucial, only going to the next problem after he's absolutely sure he's finished with the previous one, considering them final for shipping.

#### Questions:
a. (DSA) What's the algorithm Friend M decided to use to tackle your slides problem?
b. (PM) What's the software development model Friend M used as he's working through your slides?
c. (DSA) What's the data structure of the list of problems?

### Question 2:

#### Problem statement:
While slowly working through the first problem, Friend M realizes that most of titles of the "Demo" section of your presentation is in the format "\<Section> Demo", and the contents of these slides are only the one image. As changing each title and formatting each image of a new slide is time consuming, he decides that it'd be much faster and easier to just create a general slide with "\<Section\> Demo" in the title, throw a stock image with the size of the whole body section of the slides. He then makes as many clones of these slides as needed, replacing "\<Section>" and the image to fit with the narrative.

As he goes through each slide, he has to find the right image in his folder of possible images to replace into the slides. To do so, he opens up the first image in the folder, and scroll through each one until he finds the right picture, adding it in and going back to the first image. However, the ANPR Demo part is too long to be written out fully in the title and contains 2 pictures instead of 1, so he deletes the word Demo from the title, and make room to add the second picture.

As he finishes up quicker than expected, Mizuki, asked for how her friend did it, only to be met with "You don't need to know that" and refused to answer.
#### Questions:
a. (OOP) Determine the Object-oriented programming pillar(s) used to solve the problem. 
Bonus points: Determine the sub-type of the pillar(s) used.
b. (DSA) What's the searching algorithm friend M used to find the right image to replace?
c. (DSA) Determine the time-complexity of his image switching algorithm.


### Question 5:
#### Part A:
Going back to your POV, as you are walking you saw a street food store, and having decided that it'd be nice to have something to chew on while you guys walk, you asked Hoshino to wait while you go grab some. However, the crowd around you is too large, and as you turn around, Hoshino's nowhere to be seen. There's a silver lining to this though: You've instructed Hoshino to go wait the first convenience store she sees if she's ever lost and unable to contact you.

As you scramble to pull up Google Maps, and taking in consideration her normal walking pace, you pointed out all the places where she could possibly be and drew up this graph:

```
A - B - C - D
|   |   |   |
|   +---E---+
|       |
+-- F --+  
|       |
+-- G --H


You are at A.
```


(DSA) Using BFS as your preferred way of traversal, what's the traversal order you have to take to reach all convenience stores?

#### Part B:
Unfortunately, even though most roads in this stupid fucking city has the same amount of sidewalk space, the amount of people on each sidewalk is not. As you've travelled through this area many times already, you know *roughly* how long it would take to travel to each convenience store from the ones connected to it. Adding said travel time to the graph, you get:
```
A -1- B -2- C -4- D
|     1     2     4
3     |     |     |
|     +-----E-----+
|           1
|           |
+---- F ----+
      |
1---- + ----2
|           |
+---- G -2--H

You are at A.
```

a. (DSA) What algorithm should you use to find out the time you'd take to reach each convenience store?
b. (DSA) Determine the fastest route and the amount of time it'd take to reach convenience store H, D and E respectively.

### Question 6:

As you su

