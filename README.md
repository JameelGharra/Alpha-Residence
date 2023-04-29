# Alpha Residence Initiative

## Index
* [App Showcase](https://github.com/JameelGharra/Alpha-Residence#showcase-cinema)
+ [How some things work?](https://github.com/JameelGharra/Alpha-Residence#how-some-things-work-factory_worker)
  - [Device Building Process]()
  - [Example of listening to pool member changes: an admin kick a member whose online](https://github.com/JameelGharra/Alpha-Residence#-an-example-of-listening-to-poolmember-changes-an-admin-kicking-a-member-whose-online-controlling-devices-in-that-pool)
  - [State Management for Authentication: BloC pattern](https://github.com/JameelGharra/Alpha-Residence#-state-management-for-authentication-bloc-pattern)
* [The Really Short Story Behind](https://github.com/JameelGharra/Alpha-Residence#the-really-short-story-behind-boom)
* [What did this turn to in some months?](https://github.com/JameelGharra/Alpha-Residence#what-did-this-turn-to-after-some-months-software-wise-office_worker)

## The Really Short Story Behind :boom:

A year ago, a friend of mine shared with us an idea he has been trying to do, making every house in our village smarter; add to that self-awareness, and scalability and all other good stuff in the picture, managing your home anywhere, anytime and determine who exactly can/can't do so with you; We decided to go on and do this as friends, getting this bigger and maybe get some money out of it later on.

My friend is an electrical engineer that works at Nvidia, so he was in-charge of the hardware part of the project, and I handled anything software related. A third friend was in-charge of marketting.

## What did this turn to after some months software-wise? :office_worker:
A mobile application, for iOS & Android, that lets you control devices inside houses/workplaces, no matter what their type is or how many modes the device have, all in real-time, and you can manage who can/can't do so.

* ***A pool***? It is your home/workplace, each pool has its' own devices, its' own members.
+ ***Pool Members***? each pool have at least one member, each member has a rank (***Guest/Admin/Owner***), the higher rank you are, the more privilleges you get in the pool, for example an admin can invite/remove members.
- An ***app user***? each user has his own credentials (email and password), the email has to be verified before using the app, a user sees only the pools he is a pool member in.
* ***A pool device***? For e.g. an air conditioner that has a hidden camera has two modes, mode 1 is conditioning (includes data about temperature, fan level, heat/cold so on) and the second mode is camera (focus, resolution and so on) and both modes can be controlled inside the dashboard on the app, a device can have endless amount of modes.


## How some things work? :factory_worker:	

### > Device Building Process

![Device Building Process drawio](https://user-images.githubusercontent.com/26360846/235238391-8d4124b7-3c0f-4f5b-a538-44042f0c4f0b.png)

 *In the diagram, the raw data for Device ID 1 that is with the type Y was read from the cloud, a safe object that **inherits** from Device was created*
 
### > An Example of Listening to PoolMember Changes: an admin kicking a member whose online controlling devices in that pool

![PoolMember kicked Listener Example drawio](https://user-images.githubusercontent.com/26360846/235309463-74fd90c6-3e79-4866-8fe3-d4ad648c7f9b.png)

 *In the diagram, the user happened to be viewing the pool he got kicked from by an admin, so he was forced to view the pool browsing page again and removed that pool from the locally cached pools*

### > State Management for authentication: BloC pattern

![Authentication BloC drawio](https://user-images.githubusercontent.com/26360846/235311292-e5f77280-6f64-473f-bc31-947a2ed2337c.png)
*Navigation is using the BloC design pattern, seperating the business logic from presentation, facilitating testability and reusability.
if a BloC listener is a root of some sub-tree in the widget tree it will recieve any updated state, a BloC consumer is a BloC builder and a 
BloC listener, a bloC builder returns a widget depending on the new state emitted.*

## Showcase :cinema:

*The screen the user gets if he is not logged-in when he launches the application (if he was logged in and logs out he won't get this screen, he would be back to the authentication page)*\
![Intro_AdobeExpress](https://user-images.githubusercontent.com/26360846/235312183-f554a023-5293-4f61-ba60-72030336557d.gif)\
*An actual user perform a login in the app, his email was verified.*\
![Logging_In_AdobeExpress](https://user-images.githubusercontent.com/26360846/235312525-fcc623d9-50c7-4964-8e33-0724cff500b1.gif)\
*In the left a web app version of the application, with a user with an email of (vancehitch@gmail.com), on the right an Android version of the app with a user with the email of (jameelgharra@gmail.com), both users are pool members inside "Jameel's Beach Mansion", this showcases how quickly the data changed in real-time.*


https://user-images.githubusercontent.com/26360846/235316161-ffaa07f0-22e6-40d0-b49e-8eb4fc234d58.mp4\




*The user with the email of (jameelgharra@gmail.com) has the authority to invite in the pool of "Jameel's Beach Mansion", the invitation is to a user with an email of (vancehitch@gmail.com), gets invited and the pool shows in real-time, members list was checked, after a few seconds, some other user changed (vancehitch@gmail.com)'s rank to admin (two red stars).*\


https://user-images.githubusercontent.com/26360846/235316282-1f338a11-1d49-4daf-aecc-7f4ed97eadcf.mp4



