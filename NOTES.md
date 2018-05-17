# Talk

## Intro to micro:bit

micro:bit is a microcontroller platform designed to teach programming and basic electronics. It has some sensors built-in and some basic input and output (I/O) mechanisms that allow you to start sketching and see results immediately. 

The micro:bit educational foundation developed the micro:bit platform in a partnership with many companies and foundations, it is designed as a platform to get people started in programming. The British Broadcasting Corporation (BBC) supported the initiative and provided a micro:bit unit for free to every child in seventh grade (11/12 year olds) in the UK, that's about a million devices. 

The micro:bit is equipped with a matrix of 5x5 LEDs, two programmable buttons, a JST battery connector that will allow you to run your project without USB power, a powerful microcontroller (processor), an accelerometer that measures the unit's motion with respect to the vector of gravity, a compass and a bluetooth module that allows it to talk to other units and back to your computer wirelessly. It's tiny but it does pack a punch of possibilities. So you will not run out the full range of its possibilities in just a few weeks. This is a pretty nice gadget that has not yet been exploited to its full potential.

You can read more about it in the [wikipedia page covering the micro:bit](https://en.wikipedia.org/wiki/Micro_Bit).

## Wait a minute! did you say the BBC?

Yes! The venerable BBC is one of the parties behind the development of this board. It might be interesting for you to know that this is not the BBC's first foray into computing. In 1981 the BBC released the BBC Micro, a series of microcomputers for the home market, developed by the Acorn corporation, that many people in the UK grew up with and still have in their attics.

![BBC Micro Model B](http://gallery.nen.gov.uk/assets/0802/0000/0127/ict_equipment33_mid.jpg)

You can read more about it at [the wikipedia page covering the BBC Micro](https://en.wikipedia.org/wiki/Micro_Bit). 

## Why micro:bit?

Hey! I have used Arduino before, but I have never heard of this micro:bit thing, will I be able to use this knowledge? Well, if the goal is to acquire knowledge about programming and computational thinking then yes, both platforms will get you there if you put some effort into learning how to work with them. 

With micro:bit you can do many of the things that you can do with Arduino. The micro:bit is a more immediate platform as well, by immediate I mean that the gap that exists between working on something and seeing the results of your work is much much tighter in micro:bit. With Arduino you need to learn how to wire every sensor, learn about inputs and outputs and write substantial code before you can start to see some unimpressive serial output, more impressive results take a few weeks of arduous practice, so the learning curve is a little steeper at the very beginning. Both are excellent platforms and it is not my intention to favour one over the other, I just find that they suit different stages of the learning process.

Arduino is programmed primarily in a languange called C++ and there are not many alternatives, it's either C++ or hack-your-own. The micro:bit is a bit more forgiving to the learner and supports a variety of languages, we can use Blocks, which is a visual representation of code and when we feel more confident we can move onto Javascrip and Python. So it is more versatile for a person that is in the process of learning.

Another advantage to the micro:bit is that because the whole of the UK has adopted it in primary school as the platform of choice to teach technical basics nationwide, the user base is quite large for a relatively new platform. So there's plenty of educational material to get you started and the base keeps growing. 

That is why we chose micro:bit for the first half of the Tech Basics course. We understand that learning programming is hard, it involves shaping your thoughts in a way that suits computational processes and can sometimes be demanding, frustrating and non-intuitive. Hang on in there! It was like that for us too! It gets easier with practice. 

There's nothing "natural" about what computers do, they are an alien species that is taking over Earth and we will be better prepared for this reality if we learn to speak to them. Just like learning to ride a bike it takes time and practice, think of the micro:bit as learning wheels for your bike.

Once you get the hang of it, we can move onto Arduino and the knowledge you have gained by learning the micro:bit will still be useful to you. 

#### Is this for kids? I suspect I might be above this level of comprehension

You might. I know that you are all adult University students, some of you with credit cards and perhaps a love life, and that you are probably more mature than the average 12 year old. But when it comes to learning programming, you are getting started and at this stage you can benefit from this approach too. In fact one could argue that you are at a disadvantage with respect to a 12 year old as your mind is probably more cluttered with preconceptions, busy schedules and knowledge about the world that makes learning new ways of thinking a tad more difficult.

If you find the educational material a little too cartoonish for your taste, sink your teeth into the bits that are useful and ignore the rest.

### What is Blocks?

Blocks is a visual way of representing common programming structures as coloured shapes that snap onto each other in univocal ways. It helps with the burden that some early-stage learners have with the strict syntax rules and the formal grammars of programming languages. Blocks still conform to these rules but have a different way of enforcing them upon the learner that is closer to human intuition. This specific way of programming was pioneered by a programming environment for children called [Scratch](https://en.wikipedia.org/wiki/Scratch_(programming_language)) that is the result of research carried out by Mitchel Resnick's team at the Lifelong Kindergarden Group in MIT. Scratch is more than just Scratch itself, as a piece of software, it is an influential paradigm about how to approach early-stage learning into computer programming.

If you are into TED talks [you can watch this one by Mitch Resnick](https://www.ted.com/talks/mitch_resnick_let_s_teach_kids_to_code?language=en).


# Coding in micro:bit

You can start right away without installing anything at all. Just visit this site and that will start a web-based programming environment:  (note: some features do not work in Safari)

https://makecode.microbit.org/

If you want to learn a bit more about each Block and examples on how to use them, you can visit the reference: https://makecode.microbit.org/reference

## Live demo
- Live-code the spinner example using Blocks
```
on start {
    set delay = 2000
}

forever {
    show leds => {
        0 0 1 0 0
        0 0 1 0 0
        0 0 1 0 0
        0 0 1 0 0
        0 0 1 0 0
    }
    wait for "delay"
    show leds => {
        0 0 0 0 1
        0 0 0 1 0
        0 0 1 0 0
        0 1 0 0 0
        1 0 0 0 0
    }
    wait for "delay"
    show leds => {
        0 0 0 0 0
        0 0 0 0 0
        1 1 1 1 1
        0 0 0 0 0
        0 0 0 0 0
    }
}
```
- Show how to download a binary from the programming environment
- Show how to run the program on the physical board
- Do the spinner example with a variable to regulate frame speed
- Show how to make co-dependant parameters using a variable
- Show how to switch between Blocks representation and Javascript
- Backing up your project: (the option I currently use is a bit cumbersome but seems to work) 
    - switch to Javascript
    - copy the Javascript and paste it into a text editor
    - save file with a `.js` extension
    - use github to track that file and your progress

# Exercises

Let's use the simulator for these until you have your own board.

#### One -  animate
Create a program using Blocks that displays five preconfigured icons in the microbit and waits
for a set amount of time between each of them. Make sure that we can configure the time between each icon in a single place in your program.

#### Two - interact
Create a program that draws a pixel on the LED array and that lets you move that pixel using the built-in A and B buttons to move the pixel left and right and the P0 and P1 input pins for up and down.

#### Three - inventing your own syntax for Blocks
Have a goot look at the program that you just created using the visual blocks. What do these blocks represent? What do they mean? Would there be another way of representing the meaning of these blocks? 

Try to write the program you just made using Blocks, in a language that you invent yourself, this language must make sense to you. The only limitation is that your language must be in plain-text, so you should be able to write an equivalent program using the Atom text editor (or whatever plain-text editor you like best).

# Reading

Read this interactive essay by Bret Victor "Learnable Programming"
http://worrydream.com/LearnableProgramming/

