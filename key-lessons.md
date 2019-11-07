# TDD
- TDD is less about testing and more about having control and understanding of your code.
- Experiment, get feedback, learn, and adapt.
- emotional and habitual, not based on logical choices
  - basal ganglia - where habits are stored
- cue > routine > reward
  - conway's game of life exercise
  - delete your code! (remove the reward)
- gobal day of code retreat (coderetreat.org)
- practice TDD as a community

# test flakiness
- cost of flakiness
  - time & money (retriggering ci builds, local builds, etc)
  - loss of confidence (resort to manual verification)
- hard to "see" flakiness. it's not obvious by looking at the code
- measure flakiness, show devs their tests are flaky, how long it takes, how often they fail
  - start w data
  - choose a flakiness detection technique
    1. (most accurate) run each updated test 50-100 times in CI
    2. (the most Ok) record test results for every master commit
    3. (the most badass) run each changed test 3-5 times and calculate test coverage delta between each run

# Pushing Through Friction
- lies within the gaps between how things are and how they should be

## dev divide
- we're still browser people who are the shepherds of design, ux, perf, and a11y
- "care about users and deal with the browsers, users, and devices"
- the great divide (in the web community) - css tricks
  - specializing is okay
  - lots of tweets about what's wrong with the web
  - blame on both sides
  - we created the divide on the tech

## dev culture and experience
"if only we did this one 'obvious to me' thing, it'd be better"
"normalization of deviance"
friction mostly painful for mid-sized companies

pushing through this friciton is worth it, often people will leave to avoid these problems, but that means there is friction everywhere

push through with optimism and kindness

- doc sources of truth and keep them updated
- avoid single points of failure
- create culture of documentation (make this part of AC)
- ask new hires after starting - how could this be better, what's missing, what have you seen work better elsewhere?

there's often the correct path and the easy path. take the correct path because it will lead to to better outcomes

- ! stack is not technology, but people, process, and tech
- how to give people room to experiment/grow? ask for business cases, build prototypes
- friendly readmes, changelogs (even for projects), templates, automate setup
- more important to stay consistent than use latest and greatest
"you don't have to play with all the toys", maybe you don't need it
- don't over-engineer
- avoid the hype machine

When things are hard or going wrong, **invest.** Create projects to improve.
(my takeaway) create a learning culture and organization

# user empathy
1. insulate customer from complexity

can use variable fonts to create interesting and engaging designs, but also user choice
  - dyslexia -- increase line space can increase their reading retention by 50%

## a11y
common perception that you can do a11y by accident, this doesn't make sense
experience not considered in this case
fixing anything after the product was built (including a11y) is expensive

## give users choice
FOUC, death of progressive enhancement
FOUC
- FOIT (invisible text)
- FOUT (unstyled text)
- FUBC (unbehaviored content)

conflating what is good for the user is what is good developers?
we feel good about the stuff we create, at best our users **tolerate** what we create

https://www.youtube.com/watch?v=_cMLVqyYCzU&t=1209
"I can't watch this video, what's wrong with this picture?"

Is "No JS a relevant use case?" no >> "For your web experience, is there a reasonable and useful experience that does not require JS?"
  - no JS doesn't make sense for 3D shooter game

HTML design principles
"priority of constituancies"
https://www.w3.org/TR/html-design-principles/#priority-of-constituencies
> In case of conflict, consider users over authors over implementors over specifiers over theoretical purity. In other words costs or difficulties to the user should be given more weight than costs to authors; which in turn should be given more weight than costs to implementors; which should be given more weight than costs to authors of the spec itself, which should be given more weight than those proposing changes for theoretical reasons alone. Of course, it is preferred to make things better for multiple constituencies at once.

imprintable design
- user is imprinted on the experience, we need design focused on *each* person
- instead of building in layers of technology, build in degrees of fidelity

flaw: if the device can do it, the user wants it
  - showing webGL rendered map when low connectivity and 2% battery, no way to communicate my situation
  - how web content can affect power usage

flaw: people always want the most powerful experience

- features have weight and consequences (for user and planet)

> **start building in *options*, start exposing *choices***

can we fight for the user? put their concerns first?
we didn't ask to swap out old build for webpack, don't ask permission to make the web better


# we're all in this together