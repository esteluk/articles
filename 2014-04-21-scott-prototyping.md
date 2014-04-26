# Some Thoughts On Prototyping

About seven years ago I started studying graphic design. At the time I managed to get a few freelance gigs making posters, logos, and various other print projects, however more and more I would get asked to design websites. Usually I approached these the exact same way that I would approach any other print project. I would design a series of static mockups, make a ton of variations and explorations, and once I was satisfied with the visual design, I would either code it myself, or work together with a developer to bring the project to life. I always separated the design and coding process, and to be honest, always saw coding as a nuisance. However, as I didn't really know many developers at the time, more often than not I was forced to code my own designs. And so, as one would in 2007, I got pretty decent at Action Script 2 + MC Tween. I hadn’t really learnt any HTML or CSS until about 2009, therefore I coded all of my websites in AS2, which admittedly, at least gave me the chance to care about how elements, sorry, ”movie clips”, could behave. I always saw this phase as a time where I could “play” with my designs...spending tons of time finessing animation curves of how objects would slide, fade, scale, or bounce in and out. Things one couldn't really do in HTML, CSS, JS just yet. Sometimes interesting things would happen, and sometimes I’d have to go back to the drawing board. I never saw this as prototyping, but it indeed was. The problem with my entire process however, was that I separated design from coding. This meant that at some point I would realize the way I had originally imagined something working was flawed. The flow was broken or maybe the behavior I thought would work, didn’t. I don’t know why I separated these two, no one ever told me I should or should’t, but both tasks definitely demanded a different mindset. In my mind, one was distinctly design, and the other distinctly coding. 

Skip ahead a few years and this whole field of work has evolved. Web technology has improved tenfold, responsive web design is nearly a standard best practice, and most importantly we now design for a huge array of touch devices which make our interfaces inherently gestural. Consequently this greatly increases the complexity of designing an interface. Not only do we now have to account for a hundreds of different screen sizes, resolutions, device / OS fragmentation, and Operating System conventions, the way elements elements behave on a screen actually matters more than ever. In my previous anecdote about designing Flash websites, none of the animations were really necessary to the interface beyond adding a level of polish and delight. However, in gestural interfaces they can greatly improve the way we understand how an object will behave, as well as how we can interact with it. An example of this I’ve always appreciated is the way tapping on a photo in the Facebook iOS app scales it up from the bottom while the background darkens and scales down. This subtle animation indicates that you could swipe the photo down to dismiss it instead of tapping the “Done” button. Because of this one could question whether or not the button is even necessary, however I’m sure it is a good failsafe nonetheless. In fact, I’ve become so used to this pattern that I unsuccessfully try to dismiss every photo on my phone with this gesture. The important thing to recognize here is that interaction and animation can directly influence the visual design of what we’re working. This makes a strong argument for not separating these two tasks but rather trying and strive for a place where designers can work on the visual design and prototype interactions in a combined process. Additionally, as designers it’s not uncommon for us to have tons of layout variations for a screen before we settle on one, however typically it seems as though we don’t explore nearly as much — if at all — with interaction and animation.


So how do we change this? Well, for starters we need to use new tools. Luckily there are quite a few tools which are available to the public which have popped up in the last few years to help us. There are basically three tiers of tools which each have their own pros and cons. In tier #1 are the “click-through“ tools such as Composite (http://www.getcomposite.com/), Fluid UI (https://www.fluidui.com), Flinto (https://www.flinto.com/), Proto.io (http://proto.io/), and Marvel (https://marvelapp.com/). These all enable you to get to some high fidelity prototype which allows you to click through the screens of your application and animate between views with replicated native behavior. They're usually pretty quick to make and can be valuable if you want to present a “basic” prototype to a client. However, creating prototypes with these tools always feels like something you do to present a finished design in a semi-working state, rather than to iteratively work on the design and interaction of you project. Personally I find tier #1 tools to be a little uninteresting. They don’t enable one to come up with new or interesting interaction patterns, and still separate the process of designing and prototyping. In tier #2 would be video programs such as After Effects. You would use tools in this tier to make videos showing the behavior you’d would like to achieve. Typically this takes a lot of time and effort, and in the end you can’t actually interact with it. An obvious benefit however is that you can typically create whatever type of animations your heart desires. As a result I still find it to be a more interesting option as opposed to the tools in tier #1. Lastly there is tier #3 — which as you might have guessed is the tier I most prefer. Here there are two tools — Framer.js and Quartz Composer / Origami — which enable you to create rich, high fidelity, intractable prototypes, all while integrating very seamlessly into your design process. 

## Framer.js
Framer.js works by creating an HTML document of your design. It takes the layer groups in your Photoshop / Sketch file, creates images out of them, takes those images and wraps them in divs with name attributes that match the layer groups in your design file, and lastly positions them with CSS 3D transforms. Any time you make changes in your design file and re-run Framer, it updates the HTML file. It’s pretty magical. For those of us who are used to working with web technology, this whole set up feels super familiar. Once you have your project set up, all you you have to do is open up the app.js file in your favorite text editor and start writing Javascript to define how these elements should behave. From here it’s very easy to simultaneously explore visual design and animation / interaction behavior.

What I love about using Framer is that it uses web technology. This means that anytime something isn’t working the way you want, or you can’t figure out how to get an animation working exactly as you in-vision, you’re only ever a StackOverflow article away from a solution. On top of that, the library itself is very well documented and has a lot of helpers which make preforming common animations quick to write and easy to understand. Additionally, sharing your prototypes is incredibly simple as any modern browser can run them. Browsers such as Clear Browser (www.aliceturtle.com/clear-browser) even allow you to view your iOS prototypes on your device—sans chrome. There’s one obviously elephant in the room which I’ve yet to address, and that is that you need to know Javascript in order for Framer to fit into your workflow. This is an understandably large barrier to overcome when you want to get up and running quickly however I would encourage anyone who is in this position to make use of resources such as Code School (https://www.codeschool.com/) or Treehouse (http://teamtreehouse.com/) to learn Javascript and other web technologies. It is knowledge that will come in hand many times again outside of just prototyping. Additionally for those who are already savvy in these areas and eager to dive in, the Framer.js Facebook Group (https://www.facebook.com/groups/framerjs/) is a great resource for asking questions, sharing prototypes, and getting updates on the tool. As one last resource, this article (https://medium.com/building-potluck/2e405d50b600) written by Cemre Güngör is incredibly helpful for creating more advanced swipe and drag gestures.

## Quartz Composer / Origami
So that’s Framer, what about Quartz Composer? Well, Quartz Composer is a little harder to explain, but I'll give it a shot. It is a Visual Programming application from Apple which is free as a part of Xcode. Basically you can imagine it as this thing which creates individual abstractions of code that each preform certain tasks. The application was originally used for creating screen savers and doing crazy graphic manipulation, but at some point along the way, people started using it for Interaction Design. 

As a side note, I’d like to break up my paragraph here for a moment to acknowledge the awkward vagueness that is Quartz Composer. I don’t entirely know how to explain it to people, but my best advice would be to simply embrace it. The fact that you don’t need to understand every detail of what’s going on is actually what makes it such a powerful tool.

Back to it then. The UI comes with quite a few concepts to grasp. You have the Editor which has “Patches” and “Noodles” that connect together to create different behavior. And you have the Viewer, which renders whatever is defined in the Editor. All of these Patches basically run contained bits of code so you don’t have to do any of the hard work. This could be things like generating a wave value, setting a timer, rendering images, videos, text, or graphical shapes like squares and circles. Some of that sounds reasonable, however as an Interaction Designer you might be looking for patches that would for example: detect interaction events on an object, preform animations, group objects together,  or render your composition into a Phone or Tablet. This is where Origami (http://facebook.github.io/origami/) comes in. Origami is a free prototyping toolkit for Quartz Composer from Facebook. Without it, I don’t imagine anyone would see much value in using Quartz Composer as a prototyping tool, however with it, you can create highly gestural prototypes, arguably much quicker and easier than in Framer. One of the biggest benefits in using Quartz Composer is that you don’t necessarily need to know what kind of animation you want to have before you make it—you can imagine how this is mostly the opposite when writing your animations in Javascript. By dragging the noodles and experimenting with different patches you often arrive at outcomes that you didn’t initially imagine. Additionally since it has the ability to render in text, images and graphical shapes, you can start to use it more and more for visual design, thus making the process of iterating on design and interaction happen in the same place, at the same time. Once you become more advanced with Quartz Composer you can even start to do things like at video, and audio to your prototypes, or even access web cam on your computer. You can imagine how this starts to make your prototypes feel more and more real. There is however one draw back to Quartz Composer. That is, the community using it is still rather small, and when you can’t figure something out, it is sometimes next to impossible to find the answer anywhere online. Luckily the Origami kit has some great example files to get you off the ground. In addition to this there are two very active communities on Facebook where people are sharing knowledge and answering questions: Origami Community (https://www.facebook.com/groups/origami.community/) and Quartz Composer (https://www.facebook.com/groups/quartzcomposercommunity/). 

In my opinion, Quartz Composer is currently the most powerful tool that exists for prototyping. While a lot of the coding aspect is abstracted, you still need to understand some core concepts of how animation works, and how states are handled. However, once you get beyond these points you’ll be able to show your prototypes to Engineers and explain what is happening in a pseudo-code like manor. This is much more valuable for both parties involved and in my opinion should be done in place of showing static mockups and hoping other people’s imagination is as inventive as yours. I also believe that using Quartz Composer brings us as Interaction Designers to a solid level of technical understanding and empowerment without clouding our focus from actually creating good design. If we go too far down the path of coding our own applications, we won’t be focused enough on the visual design and it becomes very cumbersome to do multiple animation and interaction explorations. I think we can create the most interesting work when design and prototyping converge into one process and we can whip out prototypes as fast as we design different layout explorations.