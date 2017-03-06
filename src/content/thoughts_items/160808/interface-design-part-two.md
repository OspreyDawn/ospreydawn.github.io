*This is Part 2 in the The Logo Design Process series. See the previous part [here.](#/thoughts/160804)*

## Part 2: How Sense & Language Come Together to Make An Elegant Interface.

*I'm going to focus on a hypothetical banking application of the seven stages of thinking. This will reference the work I did for Westpac New Zealand's internet banking app called 'Westpac One.’ I will focus specifically on the task flow for the lock screen.*

In banking apps, the foremost concern of the user is making sure that the app they are using is secure and deliberate. When dealing with a user's possession as prized as their wealth, there is a greater need for discrepancy between a user's intent and what is presented on screen. For a bank, they have their own processes in the background that each have clear purposes for ensuring a user's security. Banks want to equate the experience of doing business with them with integrity. For the user, they just want to make sure that whatever they're doing, wherever they are, is safe and secure.

This hypothetical app has unique feature that allows users to quickly check their balance without having to login. As soon as they want to do something that needs to be more secure, like making a payment, then they need to unlock their account. By unlocking their account, the app goes through a series of checks on the back end that the user doesn't necessarily need to know the specifics of. However, the *status* of these processes are important to know because the checks require time and a connection to the internet to execute. This means the app has three states: a quick access state, the unlocking state and a logged in state. Communicating these spaces and the transitions between them is incredibly important to ensure there is no discrepancy in expectations of behaviour for any given space a user inhabits.

*The concept of space is a topic worth the attention of its own article. Architect Christopher Alexander has a robust and transcendent definition of space that I will cover in relation to design at later date.*

First, transparency facilitates trust which is a key factor in any application. Transparency means clearly showing how an action a user does affects the state of the app clearly. Second, like a person's proprioception, we need to communicate how a user is moving through these spaces so that they don't feel lost. An interface without clear proprioception is like being in a sensory deprivation tank. We need to be able to let the user evaluate the world of the app for every action we let them enact on it. Third, the nature of popular mobile devices these days means we are restricted to only one sense: the visual through the use of the screen. Sound (speaker) and touch (vibration) could be considered but for the sake of consistent communication I will limit myself to visual demonstrations.

So how do we solve for transparency and proprioception using only the visual medium?

Because the user is transitioning to three different spaces over the course of this task flow, it is important to make clear visual distinctions between the spaces. However, they can't be too different otherwise users could become disorientated. The quick access state and logged in state both show the same information but have different restrictions on the actions you can do in each. Because they are so similar, making them look visually similar in layout provides familiarity but clearly defines a distinction between the two.

<div class="gallery vertical">
  <iron-image class="galleryItem" style="background-color: white" sizing="contain" preload fade src="/src/content/thoughts_items/160808/gallery/banquit-screens.jpg"></iron-image>
</div>

Key elements (the user accounts, the nav-bar items and their titles), are all in the same place when changing states. The differences are seen in the more subdued palette. The logged in state is removed of distractions, putting a focus on the serious nature of the tasks to be carried out in the logged in state. Contrast to this, the quick access state is more playful representing a more relaxed space to comfort users, reminding them they have access to their account but nothing is going to go wrong in this space. The state of these spaces is also represented by the state of the lock icon. In quick access, the lock is closed signifying the account is secured. Logged in, the lock is open meaning the user is now free to do what they choose with their accounts.

### Using Animations in Interfaces to Connect to the Physical

The pad-lock icon is an important element in communicating state and intention of the app's functions. This is where real life metaphors in interface design are at their most useful. A pad-lock in the real world is used to ensure that whatever it protects is kept secure. Only those who have the code to it can unlock it. This is the affordance the pad-lock icon provides. This sets expectations on the interface element and communicates intention using common knowledge of the real world. It is made distinct in the quick access interface with the use of bold colour to encourage users to focus on it (and touch it as is expected in touch interfaces nowadays).

When they do, an animation plays to show the change in the space:

<div class="gallery">
  <video-frame source="/src/content/thoughts_items/160808/gallery/banquit-lock.mp4"></video-frame>
</div>

Notice how when the user taps on the button, the button itself expands and changes shape to fill the entire screen and reveals a keypad. This shows how the user is transitioning from the quick access space to the unlocking space. With the use of the lock icon, we set the user's expectations for some sort of method of verification and revealing the keypad rewards this expectation.

Animations like this are incredibly useful in communicating a change in state of an interface. There is a clear logical progression that animations provide. They can give context, consistency and history to the elements of an interface. When you move from one room to another, you don't appear in the next room the moment you decide to travel. You stop what you were doing, you get up and walk, you might open a door and so on until you get to your destination. There is a clear number of steps you take after you execute on intention before you actually get there. It's not just practicality of it either, it provides context, it keeps you orientated and comfortable in the space you are in. In abstract spaces like digital interfaces, animations are a god send. They clearly show how you can move from one place to another not just to know where you are overall, but show how you got there and where you might go if you return to where you came from. Users need to be able to evaluate the result of their actions to know if their goals have been met. In the digital realm, animations are the simplest way to provide this feedback. See how when we tap on a key, the numbers on the padlock rotate.

Again we're referring back to the metaphor we used with the padlock. Now we are showing that the PIN keys are tied to the padlock and using them is acting on the padlock meaning we are in the process of unlocking it. There's also an indicator that changes state when we press a key to let the user know that the press was registered and infers how many more key presses we have to go. The key press is the execution, the pad-lock rotates, a key indicator is filled and now the user is able to evaluate their action. When all the keys are entered one of two results will happen:

<div class="gallery">
  <video-frame source="/src/content/thoughts_items/160808/gallery/banquit-error.mp4"></video-frame>
</div>

If the PIN is entered in wrong, the lock will shake and an error message will appear. Inspired by the way Apple animates an incorrect password on macOS, the shaking immediately catches the eye of the user. The animation is reminiscent of someone shaking their head or the jarring feedback you get when you go to open a locked door. Its sharp and intrusive, a stark contrast to the smoothness demonstrated by previous animations. We want to tell the user something went wrong and when things go wrong it’s usually sudden, unpleasant and unexpected. Shaking the padlock this way communicates this.

This is one of the few times where going against a user’s expectations makes sense. Here, we are trying to highlight this result is not the expected action. Humans, to the surprise of some, are not perfect beings. We have make sure our interfaces allow for failure and communicate it clearly. When people evaluate the execution of their goals, it is measured by success or failure.

<div class="gallery">
  <video-frame source="/src/content/thoughts_items/160808/gallery/banquit-success.mp4"></video-frame>
</div>

If the PIN is correct, the keypad disappears but that doesn't mean we're at the end. Banks have a myriad of security checks going on in the background but having the loading screens linger on a single animation can convey a sense of slowness. This can leave users thinking something has gone wrong when everything is perfectly fine. Having the feeling something has gone wrong when you're dealing with somebody's money is never a feeling you want to convey. So here we show some sort of progress or representation of something going on behind the scenes can give the user confidence in your app's ability to function.

Animations in general do a great job of showing how all the different parts of your app all connect together. They allow a way to see the different function and spaces relate to each other. They are the journey between landmarks that a traveller might take when abroad providing crucial orientation. The greatest feature of animations however has to be the amount of transparency they provide.

The use of the padlock in the app mockup is a good example of how being transparent about what your app is doing to the user. Being transparent helps the user to understand the interface you are putting them in. This creates expectation, making it predictable. The more predictable an interface and the more consistently it satisfies expectations, the more a user will trust an interface. The more trust there is, the less they will think about the specifics of their actions and the gulfs of execution and evaluation become incredibly narrow; the sign of an elegant interface.
