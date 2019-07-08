[Ben and Jennifer's issue](https://github.com/nodejs/mentorship/issues/87)

#[Mentorship Diary] Ben & Jennifer
(Mentorship Round 1) Ben will be mentoring Jennifer on Node.js Testing and coverage.

#Kickoff meeting (6 August 2018)
---
[YouTube kickoff meeting recording](https://youtu.be/RDemyxxM3Ts)

#Scope Introduction
---
Benjamin will be mentoring Jennifer about the process of testing NodeJS and writing tests.

> The Node.js Testing Working Group's purpose is to extend and improve testing of the Node.js source code.

#Goals & Expectations
---
- Learn about the current test code coverage report
- Learn Best Practices in writing tests
- Start contributing to NodeJS by writing tests for code that is not currently covered
- Prepare Jennifer to become a future Mentor in the program
- Use this Beta program to help define the mentorship program going forward

#Availablility
---
Benjamin and Jennifer agreed to have meetings once a week during the month long Beta program. Each meeting will last between 30-60 minutes. Benjamin and Jennifer will coordinate the time for the meetings using Slack. Meetings will be held on Zoom. Meetings will be recorded and placed on YouTube for anyone to watch.

#Privacy & CoC
---
We are both comfortable recording sessions and will record sessions and link to them on github. All videos will be made available in this [playlist](https://youtu.be/ig5Yx4OSNGo) on YouTube.

#Meeting [#1](https://github.com/nodejs/mentorship/pull/1) With Mentor (12 August 2018)
---
[Video of meeting is here](https://youtu.be/6CeYO56DPwQ)

On Sunday August 12, 2018, I had my first meeting with my mentor Benjamin. Prior to the meeting I had dowloaded the NodeJS binaries from Node's website and followed the instructions to build them. I also followed the instructions on how to run the tests to verify the build. At this point I was ready to make code changes and was ready for my initial meeting with my mentor Benjamin.

##Our First Meeting
---
Benjamin and I met via zoom and the meeting was recorded. (See above for a link to the video on YouTube. All our meetings will be in my playlist on YouTube). I showed him what I had done to prepare for the meeting. One of the expectations of the Mentorship program is that mentee's take initiative during the program. Only challenge was that I needed to redo all of my work in downloading and building the code because of one small mistake. The goal of the program is to contribute to the NodeJS code base and contributions are made via PR (pull requests). By downloading the binaries from NodeJS website I did not have an upstream master to the NodeJS repo. DUH. So in our initial meeting I started the steps to fork the repo into my personal GitHub account and the clone it down to my laptop. From there I could follow the steps that I had done initially. In the video you will see my jumping over to my terminal several times to check status because the build can easily take 15+ minutes to complete.

##Code Coverage
---
While the build was completing, Benjamin showed me the nightly code coverage reports from the tests. You can check out the [nightly code coverage reports here](https://coverage.nodejs.org/). Since I am a JavaScript developer I looked at the JavaScript code coverage. The core of NodeJS is written in C++ and there are tests for it too.

Here is what the code coverage looks like:
![Image](https://camo.githubusercontent.com/0ad2016cad4110ed1db9ec005627fe0afb7c2682/68747470733a2f2f6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f636f6465436f7665726167652e706e67)

From there Benjamin showed how you can drill down into any section to get to the actual NodeJS code. When you look at a file, any line(s) of the code that is not covered by a test will be highlighted in red like this:
![Image](https://camo.githubusercontent.com/4133fec482031a6d11552d84fe32e719cd34113c/68747470733a2f2f6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f6e6f6e436f7665726564436f64652e706e67)

Now that we know which code is not covered by tests, we then started looking at the code in my IDE. I use IntelliJ as my IDE but any IDE like Visual Studio Code, Sublime Text, Atom, Vim, etc would work just as well.

##Layout of Test Files
---
The first test we looked at was test/parallel/test-fs-mkdir.js. If you have ever written tests then you will be very familiar with what the tests look like. This file has about 10 different tests in it.

Anything that is used in the tests are 'required' at the top of the file. After that any variables that will be used in tests are defined.

The actual tests are seperated by enclosing each test in {}.

##Best Practices
---
Benjamin has started to create some "Best Practices" for all the tests. One thing he has been doing it to put a short comment at the start of every test explaining what that test does. This will make it easier for the next person that comes in to look at the test code because they will have a clear understand of what the test is doing exactly.

##My First Pull Request
---
After our first meeting, my goal was to review what I learned from the first meeting. After absorbing my new knowledge, I am expected to go in and start making contributions to the tests. My initial PR will be simply to start adding comments to the existing tests. In my next post I will share the process of creating my first PR.

#Building NodeJS
---
In order to contribute to the NodeJS open source code, you must first download the binaries and build the software. Now that may sound like a daunting task but let me ensure you that it is not. In fact, I created a short 6-minute video that shows you the exact steps that you need to follow to do this. You can [watch the video here](https://youtu.be/jNY499yMwaE).

#Steps to Build
---
1. The first step that you need to take is to fork the NodeJS souce code from the Node repo on GitHub into your personal GitHub repo. You can find the [Node repo here](https://github.com/nodejs/node). In the top right there is a "Fork" button. 
![Image](https://camo.githubusercontent.com/57caf0566a84dbaf550350825e82724f9cc67111/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f666f726b2e706e67)
Just click on that button. You will be asked what repo you want to fork the code to. You should select your personal GitHub repo. The process will take a minute or two to complete.

2. Go to your personal repo and open the repo. Click on the green "clone or download" button.
![Image](https://camo.githubusercontent.com/82a1abaa3ef1fdc632b235f5294927a780d6ed27/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f636c6f6e65427574746f6e2e706e67)

3. Click on the copy icon to copy the url of the repo to your clipboard. 
![Image](https://camo.githubusercontent.com/ca6c7f73ff5321faf39b463a0b6c074fbdcf19d7/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f636c6f6e652e706e67)

4. Open your terminal and the clone your repo to your computer.
![Image](https://camo.githubusercontent.com/17f0cfb74c563edc1830a94a02cd6afe111dbae7/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f636c6f6e657465726d696e616c2e706e67)

5. Next step is to build the code. Follow the instructions in the image below.
![Image](https://camo.githubusercontent.com/2e896106ef370da5c6930bd412ae5e1608643c8f/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f6275696c64636f64652e706e67)
The build process can easily take 20+ minutes to complete.

6. The last step is to verify your build by running the command in the image below. 
![Image](https://camo.githubusercontent.com/50aa5a4caab47e2bdab6ca8da7be661856171e14/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f766572696679746573742e706e67)

#Meeting [#2](https://github.com/nodejs/mentorship/issues/2) with Mentor (20 August 2018)
---
[Video of meeting is here](https://youtu.be/f8jpnfVNNco)

@bcoe and I had our second meeting on Monday, August 20th. We met for an hour. During this meeting, we went over my first PR (pull request). As part of the best practices, Benjamin is trying to implement with the tests in Node, he wants to add a comment for every test. My first PR was to add a comment to an existing test file.

##My First PR (ALMOST)!
---
![Image](https://camo.githubusercontent.com/d61db60f584724a5da54a212d37b18c2234f16e1/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f77656c636f6d6550522e706e67)

In our first meeting, we reviewed the test/parallel/test-fs-mkdir.js file. In this file, there are tests for the mkdirSync and mkdir commands which are part of fs (file system). fs is an integrated part of NodeJS.

The test-fs-mkdir.js file consists of 11 tests. The tests are grouped in individual scopes since the tests are surrounded by {}. Of those 11 tests, 7 had comments explaining what the test accomplished. These comments help out anyone that is looking at the file to determine what is exactly going on.

As part of my first PR, I added comments to the 4 tests without any comments. The process was very simple to complete. Once I completed adding the tests, I worked with Benjamin to commit my changes and submit the PR to the NodeJS repo.

I made an initial comment on my changes. During this meeting, Ben showed me the format that comments should take. We verified that my comment started with the area that is being addressed in the PR. In this case, it was "test". The comment should not exceed 80 characters. We had to change the wording in the comment to make sure we stayed under this limit. Once everything was completed, I pushed my commit to my local repo. Then I went to the NodeJS repo and submitted a PR.

Submitting a PR automatically results in tests being run on your code. It will also make sure there are no conflicts with your code. After this process completes, the PR is accepted. All PRs are reviewed by other members of the team. If they approve your PR then it is merged into master. At this point, you have contributed to open source software.

##My First PR Was Rejected
---
![Image](https://camo.githubusercontent.com/9fb1d380179217ad647e56a7535d256dc9ee9293/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f666565646261636b312e706e67)

Just when I thought I had made your first PR, I woke up the next morning to an email that one of the reviewers had requested that I make a change. I had made an initial commit and then when working with Benjamin during our meeting, I made a second commit. The NodeJS Committee prefers to have all commit squashed into a single commit. My PR had 2 commits on it so they wanted them to be squashed into a single commit.

This was not a big challenge to complete. Anybody with knowledge of git will know how to squash commits. So I started out to make this change. During this timeframe, I got another email from a second reviewer who requested a different change. His request was that I add a period to the end of my commit sentence. Seriously I just had to laugh at that one.

I squashed my two commits into one. Then I created a new commit message. I made sure that I added a period to the end of the sentence. I have my new commit ready to be submitted and will do that during my next meeting with my mentor. As part of the Beta program, we want people to see the process so I will submit it during our meeting which is recorded so people will see the process first hand.

##My First PR Gets Closed
---
![Image](https://camo.githubusercontent.com/dcd78b25c678954b37e56c60920e7d3dac143f8d/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f666565646261636b322e706e67)

After doing my first PR, I got feedback from 2 reviewers. While they are waiting for a new PR to be submitted with the requested changes, they closed my initial PR. The changes were not merged but it was a good experience to get a feel for the process. Next time I will be better prepared when submitting my PR.

#Meeting [#3](https://github.com/nodejs/mentorship/issues/3) With Mentor (04 September 2018)
---
[Video of meeting is here](https://www.youtube.com/watch?v=5voK2tbwzoQ)

Tonight I had my third meeting with my mentor Benjamin. I was all prepared to go through and resubmit my PR from our last meeting. Just as a recap, my first PR was rejected (or at least I thought it was).

When you submit a PR, it is reviewed by one or more members of the team. I had gotten feedback from one contributor asking that I squash my commits so there is only a single commit. Another contributor sent feedback that I needed to put a period at end of my commit message.

I fully thought my PR was rejected but after talking to Benjamin at the start of the meeting I learned that it was officially accepted. I am so excited that this happened. Another contributor actually went in and made the changes and then approved my PR. [Here is a link to my PR](https://github.com/nodejs/node/pull/22424/files)

##Writing About My Experience
---
I have been very fortunate to be part of the NodeJS Mentorship program while it is in Beta. I want others to be able to see what the experience has been like and I have written two articles that were published on Medium.com.

The first article was published in the NodeJS Collection publication. This is the official NodeJS channel. They have a format for articles that they write when they talk about somebody committing to the NodeJS project. The article titled [How I Got Into #Node: Jennifer Bland can be read here](https://medium.com/the-node-js-collection/how-i-got-into-node-jennifer-bland-3060d02654b3).

The second article was published in FreeCodeCamp's medium publication. FreeCodeCamp provides free training to teach people how to code. Since FreeCodeCamp has over a million users worldwide, this publication would provide a great introduction to contributing to Open Source Software. The article titled "Contributing to Open Source isn't that hard: my journey to contributing to the Node.js project" can be [read here](https://medium.freecodecamp.org/contributing-to-open-source-is-not-hard-here-is-my-journey-to-contributing-to-nodejs-d10760e31194).

Both articles have generated quite a bit of response. I have had multiple emails from users that have signed up to be a mentee in the program after reading these articles. Plus I had an email from one person that signed up to be a mentor.

As of September 23, 2018 the article in FreeCodeCamp had been viewed 16k times. The article in NodeJS collection has been viewed 831 times.
![Image](https://camo.githubusercontent.com/328038b747471b39dc266b6e3766dbc610756491/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f61727469636c6572656164732e706e67)

##Writing My First Test
---
Tonight we went through the first test that I wrote. The FS section of NodeJS has a section that allows calls that use promises. This API is currently at a Stability: 1-Experimental level. This means the feature is still under active development and subject to non-backward compatible changes or removal in any future version. use of the feature is not recommended in production environments.
![Image](https://camo.githubusercontent.com/e51c129edbcc899395668f439c4a7765af360875/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f667350726f6d697365732e706e67)

FS Promises is experiemental currently but eventually it will be included in the code. So my first test covered this new functionality. If you read from a buffer and indicate that you want to read zero bytes then the read should return zero bytes. My mission was to write a test for this scenario.

During the meeting I showed Benjamin what I had written for him to review my code. We ran the tests to see if it covered the code or not. We went through several iterations of my initial test to verify the test covered the code.

At the end of the hour I was able to submit a PR for my first test. [Here is my PR](https://github.com/nodejs/node/pull/22800)

#Meeting [#4](https://github.com/nodejs/mentorship/pull/4) With Mentor (10 September 2018)
---
[video of meeting is here](https://www.youtube.com/watch?v=fF2kBhaRMB8)

Tonight I had my fourth meeting with my mentor Benjamin. Benjamin has been working on some really cool improvements on running tests. If you ran tests, it could take 15 minutes or more for them to complete. Bejamin has been working on creating a tool similar to [nyc](https://github.com/istanbuljs/nyc) that will allow you to run tests quicker and provide formatted output of the results. The result is the creation of [c8](https://github.com/bcoe/c8).

##C8 Testing Library
---
Benjamin spent time showing me how to utilize his library for testing. It took a few attempts before we were able to get the code up and running properly. Benjamin had just finished the code a few days before and needed to make one change for it to work properly on my machine. During out meeeting he actually made the change, pushed it to GitHub and then I pulled the change down so I could get it runing locally.
![Image](https://camo.githubusercontent.com/3fd94af92d2726e1c516783fd8c98357e44d2ea2/68747470733a2f2f7777772e6a656e6e69666572626c616e642e636f6d2f6e6f64652d6d656e746f72736869702f63382e706e67)

We were able to spend time running my test that I had written last week using the new c8 library. It was able to determine whether or not my test covered the code. Based on the inital results, we went back in and changed the code in my test and re-ran the test. We did this process multiple times as we verified the test covered the code.

If you are interested in learning more about the c8 library that Benajamin created, you are in luck. Benjamin wrote an article on it for the NodeJS collection on medium.com. His article is titled [Rethinking JavaScript Test Coverage](https://medium.com/the-node-js-collection/rethinking-javascript-test-coverage-5726fb272949). This articles provides an interesting perspective of testing Node V8.

The library greatly improves testing for Node. The speed improvements in running tests is incredibly faster. When you run tests, it will show you if the code is covered or not. The fact that we were able to make multiple changes to my test and then run the code, get the results, change the test and repeat multiple times in less than 30 minutes on the meeting shows how fast it is.

##My Second PR
---
At the end of our meeting last week, I submitted a PR for my first test. Benjamin started running the tests on my PR. The process can take up to an hour to complete. So at the end of the meeting the tests were running.

The next morning I woke up to find out that my test actually resulted in breaking another test that was in the same JavaScript file. Since I was using an empty buffer, that was being used in the test after mine. As a result it caused that test to fail.

As team members reviewed by PR, they provided feedback on my test and why it cause the test after mine to fail. Based on that feedback, Benjamin reached out to me about us getting together again to finalize the PR. We will be meeting next Monday.

##Reflections on the NodeJS Mentorship Program
---
I am fortunate to be a member of the BETA program for the NodeJS mentorship program. The BETA program has only four members. We were all assigned to a mentor for a one month trial of the mentorship program. Our feedback will shape the final version of the program before it is rolled out officially.

For me personally, I have greatly enjoyed being a part of the BETA version of the mentorship program. I have learned how easy it can be to contribute to Open Source Software. I think all developers regardless of their skill level should be actively involved with contributing to Open Source Software.

I will be taking my newly learned knowledge of tests and expanding upon it going forward. In the future you will see me submitting more PRs to NodeJS as I help to expand the test coverage for the code base.




