# Cross-Platform (Hybrid-Native) Mobile Applications
## [Native, React Native, Flutter &amp; More](https://www.droidcon.com/2019/11/15/native-react-native-flutter-and-more/?video=380953234)

In this post, I go over the main points in each framework and the process I use to decide which one to use on which project.

My choice of the framework is similar to how I would choose a basketball game to watch. I am a West Coast person, Angeleno-biased, I’d go to watch the Lakers game any time. Sometimes the Lakers are not on their best streak, but the Clippers are still hanging in there. So, I’d end up watching the Clippers instead of the Lakers in this particular season's playoffs. Or if the Clippers are out, or on the bottom of the NBA West rankings, my next best choices in the Pacific division are the Golden State Warriors or Sacramento Kings. 

I approach the choice of platforms in a similar fashion. There are people who love React Native. When you talk to them, they say you shouldn’t use anything else but React Native, ‘it’s the best tool out there’. Same thing with Flutter, people get so excited. Or Native - ‘you should only write your apps in Native!’. I have a personal opinion of what I prefer to use on my personal projects. I’ll keep my opinion private. This post is not about that. It’s really about how you find what’s right for each of your projects.

When I was first put on a mobile testing team, everything was new - Android, iOS, etc. My devs were figuring how to build out a platform. They wanted to know whether to go the Native route or not. At the time, the options were PhoneGap, Unity, C++, C. 

As the platform continued to mature, things like Xamarin, React Native, Kotlin Native, Flutter, Swift, Web became available. There was so much one could do, and it was challenging to know what to do with all these things. At the time, for most devs, building mobile apps was new. So, we had to decide if we were going to learn Objective C and Java, or jump into something like PhoneGap. It was a hard decision for us, we didn’t know where to start digging in. 

Once I got to the point of ‘this is how I’m building/testing mobile apps’, I’d be able to reuse it for each project that came along. I started working on a new project last year, and encountered the same problem again. Questions such as ‘How are we going to build and test this app?’ and ‘What’s the right solution for us?’

Overtime, I’ve come up with my own way to decide.
I’ll cover each of these platforms a little: React Native, Flutter, Native. Some of the pros and cons of each. Then I’m going to dig into the way I make decisions for each platform, because each one has its own set of goals, just like the NBA example I’ve brought up before. It’s the Los Angeles Lakers, except I'd root for the Clippers sometimes, maybe😏

<img src="https://user-images.githubusercontent.com/70295997/216801662-34b80680-9c0a-4b0e-a51a-ea4e9df13212.png" width=40> ***React Native***

**Pros:**
* Easy to learn
* Lots of resources - if you know JS, there’s a plethora of resources out there.
* Lots of libraries - perhaps too many if you ever look in the node modules folder.
* Reusable components - that you can quickly drop into different screens.
* Hot Reloading - as you are writing your code, it just shows up on your device, it’s really fast, and pretty awesome overall.

**Cons:**
* JS is not type-safe without additional tools - it’s really easy to get into a project quickly and say ‘I’m just going to add TypeScript later’. And before you know it, you have code that is just a mess and is not scalable.
* There are a lot of flavors - there are many ways to do it. If you do a quick Google search, you’ll find that’s true.
* Performance - there can be some performance issues.
* Bridging can be challenging - bridging on React Native for Android can be a big challenge, even worse than iOS for me personally.
* Debugging - if you’ve done React Native, you’ve seen the [red screen of death](https://stackoverflow.com/questions/36408309/react-native-run-android-red-screen-of-death) come up. And it [hardly gives any context](https://stackoverflow.com/questions/40903211/react-native-red-screen-error) as to what’s going on.

<img src="https://user-images.githubusercontent.com/70295997/216801791-dbcc4818-276f-4c89-96eb-64f4a0ece17b.png" width=40> [***Flutter***](https://www.altexsoft.com/blog/engineering/pros-and-cons-of-flutter-app-development/#flutter-2)

[**Pros:**](https://www.altexsoft.com/blog/engineering/pros-and-cons-of-flutter-app-development/#pros-of-flutter-development)
* Type-safe (Dart)
* Supported by Google
* Reusable components
* Fast layout [engine]
* Hot Reloading - just like React Native

[**Cons:**](https://www.altexsoft.com/blog/engineering/pros-and-cons-of-flutter-app-development/#cons-of-flutter-development)
* Young platform - many people I discussed Flutter with, question its stability. It’s the story of Flutter, it has a ton of potential, and given time, can become more stable.
* Not a lot of resources
* Need to bridge to native [platform]
* Not a lot of devs with experience - consider, as you’re building out a team

![](https://github.com/lana-20/native-reactnative-flutter/blob/main/native.png)

***Native***

**Pros:**
* Performance - benchmark of React Native and Flutter is as good as native. With Native, you get that out of the box. Assuming that you are conscious of it and writing your code well.
* Native feel - not always, but if you do it right, you get the native feel in your app.
* Support [by the Google and Apple platforms]
* Community Support
* Quickly add new OS features - as Apple or Google drops a new version of the OS, you can quickly jump in and add that in, without having to wait for a third party to add support for whatever that new library is.

**Cons:**
* Code sharing across platforms - not using any of the other platforms, sharing code across platforms - iOS to Android - can be challenging.
* Steep learning curve
* Expensive - having to hire two separate devs to build on each platform, unless you can find somebody who can do both. And if you do, they are most likely not cheap. If you are a small company, building Native may not be the right solution.


How do you decide which of these platforms is going to be the best?
Some of these seem fairly obvious, but for me it took a lot of time working through this over and over to really understand it. Hopefully, the following will help someone else out there who is trying to decide.

***HOW TO DECIDE***

* WRITE DOWN THE GOALS FOR YOUR APP
* RESEARCH
* PROTOTYPE AND MEASURE
* SEPARATE FACT FROM OPINION
* WRITE DOWN THE RESULTS

**WRITE DOWN THE GOALS FOR YOUR APP**

* What is it that you want your app to do?
  * Performance
  * Speed of development
  * Native feel
  * Code sharing - to get the devs up quickly
  * Etc.
  
Decide on what your goals for the platform are. Then, most importantly, write it down. It’s important because goals can change over time. But there’s something about writing it down that helps you solidify that this is what we want this platform to be. Sit down with your team, whoever ends up making the decision, whoever the stakeholders are, and write down the goals for your app.

**RESEARCH**

* Talk to the devs and QA who have used each platform - talk to the people who have actually done it. Eg, I know somebody at [AirBnB who did React Native and then pulled out](https://www.theimmigrantprogrammers.com/p/why-airbnb-dumped-react-native?s=r). I talked to them over lunch about that experience. I gained a lot from it. I took notes and wrote everything down, everything I learnt about every different platform and what they ran into. The more I did it, the more I started noticing the patterns throughout the conversations. Eg, mentioning they ran into a particular performance issue in a table list. As I started gathering these notes, stuff started to stick out. That becomes important as I make my decision.
* Read online articles - there’s a ton of info out there. You’ll find articles on why you should never use React Native and the articles saying that you should always use React Native. You’ll find that for each of the platforms.
* Research opinions from both sides - it’s important that you look at the articles stating each side of the argument, if you want to understand the whole picture. Try to understand why somebody would suggest you never use a platform. What are the real drawbacks at the core of that article? And the same thing for the reasons to use it.
* Don’t base your decision on the opinions; however, opinions help us understand experiences of other devs and QA.

**PROTOTYPE AND MEASURE**

There is an app written in both React and Flutter. The dev didn’t do Native. The app is super simple, it just pulls a list of images from Unsplash and displays them in a list. The point is you want to find a way to prototype something similar to what you are building.
If I were going to build an app that displays a list of photos, maybe a competitor to Instagram, then I want to prototype something simple, not going too deep. Something simple, but something that shows the core goals that I have for my project. And I prototype it in each of the languages. They are all fairly simple to get the project started in. So, it should be easy to jump in, find these resources and prototype.

Github Repo with React Native and Flutter Prototypes:  https://github.com/BarlowTucker/photos-example
*Note: Set up your own Unsplash key.*

This is the React Native code for the app. It’s a very simple version. It may not be the best in terms of code quality or optimization, but the point here is to have the code that can fit into one slide, that can do what’s prototyped.

![](https://github.com/lana-20/native-reactnative-flutter/blob/main/app_proto.png)

For React Native, you build the components. You have your PhotoItem and PhotoList - these are the components that can be reused on multiple screens, and you display it in a list. This little bit of code built the app. There’s also a bit of network code that is present in the repo. So it pulls the photos, it displays them in a list, you just scroll through them.

![](https://github.com/lana-20/native-reactnative-flutter/blob/main/app_reactnative.png)

The Flutter version is a little bit longer. In fact some stuff was cut out of the slide. There’s some boiler plate that you’ll need to get from the repo. This is the Flutter sample for the exact same app. And, again, it displays the same list of photos from Unsplash.

![](https://github.com/lana-20/native-reactnative-flutter/blob/main/app_flutter.png)

Some of the nice things are the built-in widgets that are very similar to the React Native components that are widgets that you can reuse across the components. It’s all built into these different structures/layouts that you can find on the [Flutter](https://flutter.dev/) website. It’s nice that you can build these components that are reusable in [Dart](https://dart.dev/).

**SEPARATE FACT FROM OPINION**

Once done with the prototype, you measure your prototype against the goals. It’s important, once you have your prototype, to run it through some instruments that you have to get measures of load time, how much memory you’re using, CPU usage. Some of things that might be important, that you wrote down in the goals for your app, you’ll want to measure your prototype against and see how it performs. Understand that this is just your prototype and it’s not going to be as complex as your app.

Now, you take all this info and separate facts from opinions.
* Beware of opinions dressed as facts
  * “Using [fill in a favorite platform] removes a whole class of bugs” - I hear this all the time. It sounds like a fact. The reason it’s an opinion is because the class of bugs it removes is better than the class of bugs that it introduces. Because every platform, every way you write your code, whatever styles and backgrounds, it all comes with its own baggage. If you’re going to say that you’ll use whatever platform and you’re not going to have bugs any more, that’s not entirely accurate. At least not in my experience.

Sit down and try to find a way to boil it down to the facts for each platform. Again, for me that comes from obtaining enough data. You start finding those streams that run through all the articles, the people you’ve talked to, the prototype - so that you can state that you feel confident that is something you can build your app on.

**WRITE DOWN THE RESULTS**

* Write down what you found.
* Focusing on the facts and how the results align with your goals [for the platform].
* Using spreadsheets helps organize the information - give a score/value to each of the goals,eg, performance on the scale of 1-10. Now you have a way to score each platform, and you give it a score and total it up at the end. At the end, you’re going to have a pretty clear picture of ‘this is the right thing for us, for this app, right now’. 
Just because the solution is good right now, doesn’t mean you have to stick with it. It may be the right solution for now because of where you are as a company. Maybe six months from now, it’s time to reevaluate. And you go through these steps again and see if the platform you chose still aligns with your project goals.
Share the results with others - write a quick blog post, share it with everybody. There may be other people who are going through the same thing and they want to know what you found in your prototyping/research. The more you do that, the more you help others find the right solution for their platform.
