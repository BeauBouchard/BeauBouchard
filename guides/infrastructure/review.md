# Architecture Review is just another Peer Review

Architecture Review is at times I found a contentious meeting at times. There are many reasons for that which can be different for every meeting and company. There is but one thing that is a solid overlap from these meetings, which is normally a root misunderstanding.

One of the more famous quotes about architecture meetings. 
> The Architecture Review Process is a crucible. In it we burn away irrelevancies until we are left with a pure product, the truth for all time. 
> (Jean-Luc Picard Star Trek: The Next Generation, ‘The Measure of a Man’) (Yes, go watch the episode, he actually said that)

 I really like Architecture, and sometimes I am too shy or caffinated to talk about it effectively. Empathetically I know other people with broad sets of experiences have varying good and bad days which contribute to hteir own ability to be tactical and effective in a tedious meeting.

Sometimes, a Colleague will want to use the meeting to re-inforce their biases, at times appearing uninterested in changing them, staying fearful to what they dont understand. Too much time in this world has been wasted by men sharing their opinions about Kubernettes or serverless, or terraform before anyone in the room used it, and too many leaders are incapable of considering alturnative to what they already understand. New things sometimes can be scary and architecture can increase in complexity, but the leaders should maintain a flexible view that is shared through broad collaboration. 

I thought a little bit about a previous architecture review I had else where in life, where it was really informative, meaningful and helped me write a good document. The thing is it was mostly in confluence, and it was all in a few comments and a side conversation to make sure i was understanding the consideration. I enjoyed it because they got to take time to explain their nuanced view in a calm even keel manor like we all often do in a PR code review. Complex systems sometimes have simple answers with nuanced consequences, and those are really really hard to eloquently talk about on the fly in a guild meeting. 
Sometimes documents are shy or unfinished and don't need comments yet which is totally valid and fine. But I always suggest architecture committees should have a normalization of receiving compassionate feedback and responding to that feedback both sides taking into consideration your colleauges come with good intentions. 



## How do I make my Architecture Review Meetings more like Peer Review? 


The real purpose of the Architecture review meeting is actually something imporant that shouldn't be trivially wasted. Arguably depending how you are conducting your architecture and who the stakeholders are there are imporant responsibilities and considerations that should exist in your architecture documents. 
Rooting important questions that exist in other standards, but not fully adopting other more rigid standards helps focus deliberate conversations in the documents. 
These are normally how I like to format some sections, which I recommend using in most Architecture document review processes, and it helps reviewers and stakeholders to be more tactical and focused on their considerate comments and questions when reviewing. 


## Introduction Paragraph 



### Problem Statement / Objective Statement 

Communicating the rationale of your architectural change is excelently summed up in the introduction area at the start of any document. This can be in the form of a Problem statement, as if you are trying to solve a problem, or presenting a better alturnative. 
You should be using this introduction to root the document explaining throughoughly "why".


### Goals / non-goals

What you are trying to solve is sometimes as important as listing the things you are not interested in solving. 

Its especially imporant for effectively and clearly communicating to stakeholders the enumerated objectives that are setout to be accomplished possibly with some criteria. Non-goals being powerful in accomidating considerations you have no interested in, but could be comingled or related. 
My goal is to add a CI-Process to xyz project, my non-goal are things I do not want to do. I do not want to update the CI-Process, I do not want to change the CI-Process, as the CI-Process is in ABC repo, CI-Process will be implimented in XYZ repo...  is a small scale example. 

### Diagrams

The vision you are trying to explain is accomplished through a number of different ways, one way, litterally illistrating a high level diagram to cover the system you are architecting.  
I recommend using color-blind-safe colors to highlight changes, and taking time to make a reusable diagram that will last the lifecycle of the change, possibly incorperated into the primary architecture documentation to contribute to its broader context. 


### Impact Statement 

* What at your company is changing)
* Clarify and assess the need for a change
* Assess non-functional requirements and constraints

### Methodology 

This is your meat, this is where you lay out how you plan to execute your thingy. 

### Considerations / Risks / Mitigation

* Identify trade offs with pros and cons between scenarios 
* Identify potential opportunities of reuse and risks
* Reduce the likelihood of late rework and issues due to poor design

#### Alturnatives

Its polite to conceed that you could be wrong, and consider generating alternative scenarios that solves the problem. But recognize this isn't a document about those alturnatives, its a document stating your intent to go with your current choice. You can outline briefly why you didn't consider another option, but you don't need to think of it as discrediting that solution, mearly expressing your open preference is sufficient. The nuance here is the working solution is the best solution at most companies, but you can always leave room for that conversation about alturnatives open throughout the document process. Its not your job to solicite the alturnative solution's adoption, only your own. Their alturnatives can be considered, but their alturnatives have their own merits that should be taken serious. But you don't need to without being prompted to spend a very long time on alturnive ways to do something. 

### Reflection

* Discover or reinforce the need of platform foundations
* Ensure decisions are taken favoring shared standards
* Align stakeholders among requests for changes in the landscape.






