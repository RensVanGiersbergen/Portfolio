# What is the best way to code review in a group project?
<br>
<div align="center">
    <img src="https://image.spreadshirtmedia.net/image-server/v1/mp/compositions/T773A1MPA1611PT10X15Y7D153480745FS1605/views/3,width=550,height=550,appearanceId=1,backgroundColor=FFFFFF,noPt=true/wtf-per-minute-developer-code-java-c-gift-travel-mug.jpg">
</div>

## Table of contents
- [Introduction](#introduction)
- [What is code review?](#what-is-code-review)
  - [Manually](#manually)
  - [Automated](#automated)
- [Why is code review important?](#why-is-code-review-important)
- [What code review strategies are there?](#what-code-review-strategies-are-there)
  - [(Fagan) Inspection](#fagan-inspection)
  - [Pair Programming](#pair-programming)
  - [Over-the-shoulder](#over-the-shoulder)
  - [Tool-Assisted](#tool-assisted)
- [How do experience software engineers use code reviewing?](#how-do-experienced-software-engineers-use-code-reviewing)
- [Conclusion](#conclusion)
- [Sources](#sources)

## Introduction
In this research my goal is to find out the best way to review my groupmembers their code. We got a request from our stakeholder (Bert) in our group project to review
each others code so this is the perfect opportunity to start a research to achieve my goal. Code reviewing will ensure the quality of your software, makes it easier to understand different approaches of other developers and will hopefully make you think about those different approaches and how you could benefit from these. All in all, if you're working in a software team. This research is going to help you out!

## What is code review?
Code review is a process where one gets their code reviewed by other developers or external applications. As a developer you want to get your code reviewed as soon as possible to get a second opinion on your code. Later on we will talk about what you can do with this second opinion. Thus there are multiple ways of reviewing code. Automated and manually. 

### Manually
The code review process done manually goes as follows, one or multiple developers take a look at the source code of a developer. At least one of the developers reviewing the code must not be the code's author. This will enforce the code reviewing to be done very critically. If the author of the code were to review it themselves they would be less critical about it, because in their eyes they always made the right choice when it comes to programming. The reviewers will look at the code and ponder if this approach can be optimalized. At the same time they will see bugs or errors the writer of the code made or notice security issues.

### Automated
Automated code reviewing is very different from manual code reviewing. There are many automated services like Sonarcloud, Resharper, CodeScan etc. They will scan your code and let you know about possible errors you made, security issues, typos you make while coding and much more. This improves your quality of code, but it has one major downside. These services all check your code based on if it is wrong or right. If u make a mistake while coding or added more lines then needed in a specific part of code they will notice it, it doesn't only matter if the code is written right. Even more important would be why you programmed it this way or if your architecture is okay. These question cannot be answered by the previously mentioned services.

## Why is code review important?
Code reviewing is part of the quality assurance of your code. The second opinion of the reviewer(s) are critical. These opinion(s) are important because listening to them increases the code quality. Think about: maintainability, readability, understandability. Furthermore it helps finding defects in the software. Think about bugs, security vulnerabilities, performance issues and in the worst case injected malware.

On the other side, code reviewing is also very educational. You get to learn from mistakes you make and get to transfer knowledge with each other. Both parties, the code author and the reviewing team benefit from each other.

When working in a developer team, code reviewing each other gives you yet another cool benefit. You get to understand someone's way of thinking. This makes you understand them better when they explain something, because you have a good understanding in what way somebody thinks and works. This allows you to grow closer as a developer team, as you start to work better coöperatively.

## What code review strategies are there?
Here I will include the most common strategies to review code.

### (Fagan/Formal) Inspection
This approach requires a serie of meetings and a group of engineers. They will go over the code line by line. Usually with copies of the material. This is a very good method but it very time and people consuming which makes it very hard to use in small businesses.

### Pair Programming
This approach lets two developers work on the same code. This makes sure the developers check each others code as they go. With this method you don't need to review code at the end of the process which is very nice, but in the end the time it takes to deliver increases and requires more teamwork.

### Over-the-shoulder
This is a lightweight method which is arguably code reviewing. It is considered way more comfortable compared to the previous method (Pair Programming). Once you're done coding you simply ask a developer to come take a look. You quickly explain what you made, what it does and how you made it. This method is not made for reviewing large quantities of code. In an ideal situation you have implemented a small feature and get that reviewed.

### Tool-Assisted
This last method is considered the most favorite way of code reviewing by developers. It requires no extra developers to review your code. Previously we talked about the difference between automated and manual code reviewing so keep that in mind. Nonetheless this method costs the least time and developers needed for reviewing. Another advantage of using this method is that it is very quick compared to the other methods. This process can be automated using GitHub Actions, and many of the services talked about [above](#automated) are included in IDE's, for example ReSharper. All those reasons add up to this being the most loved method.

## How do experienced software engineers use code reviewing?
I asked a couple of experienced software engineers about how and when they use code reviewing.

Starting with Bert from Isaac (becoming IO). Bert works at a software developing company. That's why code reviewing is very important. They never publish anything without having it checked out at least once, preferably twice. According to Bert the key of a succesful code review is to keep the SOLID principles in mind at all times.

## Conclusion:
After getting to know many ways of code reviewing and hearing opinions from experts. My conclusion is that the best way for us in the group project to code review is with the over-the-shoulder tactic and we will code review after a new feature is ready. At the end of the sprint we will do a formal inspection. With these 2 tactics combined everyone keeps track of all parts of the project. And finishing every sprint with reviewing new code with a formal inspection we make sure nothing is missed since over-the-shoulder alone is very lightweight.

## Sources:
- [Smartbear](https://smartbear.com/learn/code-review/what-is-code-review/)
- [Wikipedia](https://en.wikipedia.org/wiki/Code_review)
- [GitLab](https://about.gitlab.com/topics/version-control/what-is-code-review/)
- [Codegrip](https://www.codegrip.tech/productivity/best-practices-for-reviewing-code/)
