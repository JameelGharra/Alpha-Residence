# Alpha Residence Initiative

## The Really Short Story Behind :boom:

A year ago, a friend of mine shared with us an idea he has been trying to do, making every house in our village smarter; add to that self-awareness, and scalability and all other good stuff in the picture, managing your home anywhere, anytime and determine who exactly can/can't do so with you; We decided to go on and do this as friends, getting this bigger and maybe get some money out of it later on.

My friend is an electrical engineer that works at Nvidia, so he was in-charge of the hardware part of the project, and I handled anything software related. A third friend was in-charge of marketting.

## What did this turn to after some months software-wise? :office_worker:
A mobile application that lets you control devices inside houses/workplaces, no matter what their type is or how many modes the device have, all in real-time, and you can manage who can/can't do so.

* ***A pool***? It is your home/workplace, each pool has its' own devices, its' own members.
+ ***Pool Members***? each pool have at least one member, each member has a rank (***Guest/Admin/Owner***), the higher rank you are, the more privilleges you get in the pool, for example an admin can invite/remove members.
- An ***app user***? each user has his own credentials (email and password), the email has to be verified before using the app, a user sees only the pools he is a pool member in.
* ***A pool device***? For e.g. an air conditioner that has a hidden camera has two modes, mode 1 is conditioning (includes data about temperature, fan level, heat/cold so on) and the second mode is camera (focus, resolution and so on) and both modes can be controlled inside the dashboard on the app, a device can have endless amount of modes.

## How things work? :factory_worker:	

### > Device Building Process

![Device Building Process drawio](https://user-images.githubusercontent.com/26360846/235238391-8d4124b7-3c0f-4f5b-a538-44042f0c4f0b.png)

 *In the diagram, the raw data for Device ID 1 that is with the type Y was read from the cloud, a safe object that **inherits** from Device was created*
 
 
