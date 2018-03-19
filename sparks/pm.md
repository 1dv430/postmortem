# Sparks

*Molly Arhammar 2017-06-01*  

## Abstract
*This report concerns the development process and techniques used to make a web-application within 200 hours over ten weeks. It discusses the vision, the finished project and the workflow and techniques used to get there. The report identifies three key points to a successful project as an iterative and incremental workflow, good planing and an element of social control, and two key points to avoid as confusion around testing and being too much of a perfectionist.*

## Project background and overview

### Finished product

Spark is a service to match volunteer-based organizations with people who want to help. The app allows you to register as a volunteer, let the app know how often you want to help and what kind of skills and interest you have, and get a list with needs matching your profile where you can apply with a single click. You can also register as an organization, fill out your needs, and get an email with contact info when someone shows interest. There is a pipeline for continuous delivery with a CI-server in place with automatic testing and deployment and the code is well commented and structured.

### Vision and Goal

The goal for the project was to build a small but stable and scalable application, with automated testing and a plan for continuous delivery and deployment. It set out to be be mobile first, offline first, and accessible. The aim was to set up a development process that is test-driven, predictable and automated, the keywords for the project being *simple*, *modern*, *accessible*, *updated*. The core functionality of the application aimed to match volunteers with volunteer opportunities.

In realizing this vision technical skills would be combined with development and project-focus skills to, hopefully, be able to finish a fully functional app on time and with a reasonable amount of effort and documentation.

### Workflow

The project has had an iterative workflow, which means that it is carried out in small increments, each increment building on top of the last, expanding it. In the context of this project that meant to have a deployed and working and tested version of the app every Monday, with more and more features being added on each week. The iterations have, on top of this, been grouped into sections in accordance with the [OpenUP](http://www.eclipse.org/epf/general/OpenUP.pdf) project lifecycle: *Inception*, *Elaboration*, *Construction*, and *Transition*. Within each of these sections there have been a specific focus to the iterations, to make sure that the project is on track and can be completed in time.

Notable to mention in relation to my personal workflow is that I made it a part of the project to set up a CI-pipeline, a plan for continuous integration. This means that I connected a CI service - in my case Travis - to act as a gatekeeper between my source-code on Github and my deployed server on Heroku. On every push with updated code to Github, Travis ran the tests I had told Travis to run, and if the code passed the tests, automatically deployed the code to a staging server. On that staging server manual tests could be run, and when those were passed satisfactory, the staging app were manually promoted to a production app accessible to the public. This workflow ensured that the app visible to the public were always updated to the latest working version, and that I never had to deal with a situation where something on the production server didn't work as expected, since it had already been tested on an identical staging server.

### Techniques used

*Client-side*

- Vanilla Javascript
- React
- Material UI
- CSS
- HTML

*Server-side*

- NodeJS
- Express
- MongoDB

*Testing*

- ESLint
- Mocha and Mocha-steps with Chai and Chai-as-promised
- Enzyme
- React Test Utils
- Sinon
- Karma

*External API:s*

- Facebook
- SendGrid

*CI and deployment*

- Webpack
- Github
- Travis
- Heroku
- MLab
- PaperTrail

The client-side of the app is written in React with a few instances of vanilla javascript for external functionality. The design is done using Material UI and CSS. The server is written as an expess-node-server, connecting with a MongoDB database. The app connects to facebook through their API to authenicate the user, and to SendGrid for help with sending emails. The client is compiled in webpack before deployment, version-controled on Github, then push via CI-control on Travis to be hosted on Heroku, where it uses PaperTrail for logging and MLab for hosting the MongoDB database. App is linted with ESLint, testing on the client is done with Enzyme for testing React specifically, as well as sinon, mocha and React-test-utils. The tests are then run through Karma, which compiles and transforms them. Tests on the server are written with mocha and chai-as-promised, and run with mocha-webpack.  

## Take-aways

### Positive

The first positive is the workflow - the iterations, the risk list, and the constant deployment. The iterative workflow has been splendid - to make sure that everything works to deploy and test instantly, every week, means that there is never a sudden surprise of something that doesn't work and a huge amount of code that needs to be rewritten. It discourages to put things off, which keeps the application small but solid - what you have works, and is deployed, rathen than having a huge code-base of half finished things and then make everything work at once. There is never an element of total crisis, which facilitates a sense of comfort in one's own abilities. Connected to this is the OpenUP project lifecycle, which dictates that the app first be planned out and structured, then all major risks identified, and then other features added when those risks have been eliminated. This approach proved a huge success for me. It kept me focused on the right things, and made sure I had a working app deployed the first week and an app with no risks for core functionality not working when there was five weeks left in the project. Fortunately it is very easy to move this sucessful approach to any other project I take on - the key point is to identify key features during the first two weeks, find what risks there are to those key features not working, and then solve those risks one by one. The approach is about the same as one takes to coding in general - figure out what needs to be done and why it isn't working, and then logically implement method after method until it does. It is a problem-focused approach rathen than a solution-focused one - if you understand the problem, then you understand why there is a problem, and then the solution becomes obvious. Just spend enough time focusing on understanding the problem, both when coding and planning a project.

The second huge positive thing is my own ability to plan. I'm very happy with it, both with managing to keep the requirements down to a sensible amount when I planned out the whole project to begin with, to identify key requirements and put the rest on a waiting list, I estimated quite correctly how many new techniques I would be able to learn within the set time - and my planning in each iteration - my estimated time was never completely off, I planned with slack, and I exited the project having implemented all requirements under step one only running 4.5 hours over time in total. I knew that I'd be travelling for the last three weeks of May, which meant I planned to have worked extra hours before then to make up for lost time in advance, which gave me a sense of control and motivation. Thanks to this my finished app is very close to my original vision, both in scope, functional and quality requirements, and implementation details. 

The third positive is the element of social control. To have to answer to someone else every monday and in effect having to present the product live to a 'customer' had me continiously tying up loose ends and testing what I had done. To do test reports functioned as an element of social control over myself as well - every week I had to sit down, look at my code, and actually ask myself what I had done and what tests I had written that did not exist the week before. To have to have it in writing made it very obvious what wasn't done, and made it impossible for me to save the testing for last.

### Negative

The first negative is confusion around testing. Wanting to test both client functionality and design, as well as both unit and integration tests on the server, made it necessary to use two different tests runners, neither of which I had used before. I had never tested React. I had never even used React. On top of this I had to make the tests run automatically on a CI-server on push to Github, where they ran differently than on my local machine, and write mocks for tests against the database that also had to work on the CI-server. This is, whitout doubt, the hardest thing I did in the project, and I could have spent three times as much time on it without feeling like I was finished. To not know how to use either the testing tools or the testing frameworks or the CI server or the test runner made for a huge confusing mess that had nothing to do with actually writing good tests that tested if my app worked correctly. I am very happy that I forced myself to push to production through the tests on Travis, because that made me actually have to deal with the mess rather than put it off. I couldn't have done much differently, wanting to do all the tests I did, but it was still a huge stress-factor that I have to avoid in the future. A step in this direction has been taken already with me now having learned a lot about many different frameworks, which means in the future I can let 'what do I know how to test properly' weigh in on my desicion on what languages and frameworks to use for my code. Still, I will have to take every opportunity to learn more about testing as soon as possible, because I do not leave this project feeling that it is my area of expertise in any way.

The second negative is my own perfectionism. I became frustrated with myself for not being able to do everything at once when I had it all planned out in my head. I got stuck on things becuse I kept thinking about how I could make them better - which is really not a bad thing, in moderation, but it is very hard not to get stuck on a certain thing and not let it go until I find it perfect (which, spoiler, is never), and by virtue of this risk working huge amounts of overtime. Having to stay within 200 hours as well as sticking to my plan was very good for keeping this at bay, and is also how I will try to avoid it in the future - to have a mantra of 'this is not about what I can do, it is about what I can do *in 200 hours*'. I have to have faith in myself and trust that I am not stupid, and then dispose my time after that. I have to accept that perfection does not exist and move on. A good way to avoid this is also by keeping requirements specific and small and then expanding.

## Conclusion

In conclusion, I am very happy both with myself, what I've learned, how I used the skills I already had, and the project as a whole. The actual application could have had more functionality, but that was also the point - to not just make an app, but a sustainable project with a sustainable work flow that I can expand on. The whole project as such with the CI, the iterative workflow, the external APIs that I've incorporated, how I've figured out how to use documentation to actually help myself, the well structured and well commented code and the working application implementing all the core requirements, have been a success.  

To see the development potential for the project is easy, since my product backlog contains both a step 2 and a step 3 with features I'd like to implement, like a profile for the organization, custom emails and an on-site inbox. Given more time I would mostly start with trying to get a complete test-coverage, since I think this is a enourmously valuable skill to have, would teach me many new techniques, and would better the applications performance.  

Development potential with myself ties in to this and is as easy to identify - I shall work on the two negative experiences and how to not have them happen again, which means 1) to learn more about testing frameworks, to try to adapt a test-driven approach, and to make even more time for testing in the total scheme of a project, and 2) to work with my perfectionism and frustration with myself by setting tangible goals for when things are done - even small things, like a class, a requirement or a test suite and not just the big things - and force myself to let them be by that point. To strive for a sense of 'good enough' and move on, as well as trying to get a feel for how much it is good to push myself, and set up a clear amount of time I am allowed to spend on something.
