# assert js

## Invest in improvements
### Scaling R&D without dedicated QA (Adam Archer - Shopify)
When things are hard or going wrong, **invest.** Create projects to improve.
(my takeaway) create a learning culture and organization

## TDD
### jim shore
- TDD is less about testing and more about having control and understanding of your code.
- Experiment, get feedback, learn, and adapt.

### How to build the TDD habit in your team - Ryan Marsh
- emotional and habitual, not based on logical choices
  - basal ganglia - where habits are stored
- cue > routine > reward
  - conway's game of life exercise
  - delete your code! (remove the reward)
  - bell throughout the day, then 3 minute TDD cycle
- the key to running a successful TDD workshop is to not tell them it's a TDD workshop

### Component-driven design & viz test coverage - Michael Shilman (chroma)
- ui states are combinatorial
- break down designs into components
- catalog relevant states for each component as a story
- build out components __in isolation__
- recompose components into screens
- ^ this is actually testing

### other things
- gobal day of code retreat (coderetreat.org)
- practice TDD as a community


## Test maintenance
### old solutions to new problems - josh justice (big nerd ranch)
The problem now is test maintainability. Let's talk in patterns, and take advantage of our rich testing history.

"xUnit test patterns (refactoring test code)" by Gerard Meszaros

5 warning signs
- using conditionals in tests
- mystery guests (setup abstracted away)
- irrelevant information
- interacting tests
- production logic in tests

### tests > types - Colin Ihrig (Joyent)
there are tradeoffs for types that most devs and project managers don't consider
- types add verbosity & complexity
- a language is a big dependency, their bugs are now your bugs
- "The TypeScript Tax"
- can still provide a type declaration file (.d.ts)

### Integration testing w Cypress - Nancy Du (rangle.io)
- integration tests can be hard for stakeholders to understand
- mocks become difficult to setup + maintain

suggestions
- write based on AC of user stories
- auto-record real responses to test APIs to make managing mocks easier to maintain

### test flakiness - jason palmer (spotify)
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


# web unleashed

## oops I guess we're full stack - chris coiyer
"care about users and deal with the browsers, users, and devices"
the great divide, specializing is okay

## Dynamic Typographic Systems, Modern CSS, and Variable Fonts - Jason Pamental
most common interface w user is *words*

type is the voice of our words, how we 'hear' what we read

key css features
- css custom props/variables
- calculations
- variable fonts
- ^ using them together

### "design can reduce friction"
- variable font = single font file that behaves like multiple fonts
- accessibility (dark mode, high-contrast, line spacing, word spacing)
  - dyslexia -- increase line space can increase their reading retention by 50%

### transfer friction: intentional tension
Misconception that if users presented with slightest challenge, they are gone. Sometimes typography needs to be challenging, force you to stop and figure it out. "Design is communication" 

get away from one-layout solutions
- all content in medium/facebook/ny times looks the same
- multiple templates per site (standard, editorial layout #1/#2)


## Slashing Bad User Experience Using DevTools - Henri Helvetica
everyone is responsible for performance

tools
- FF beta: inactive CSS
- network panel
  - filter can take conditions. e.g. >10kb
  - gear > use large request rows
    - can see if resource being compressed (gzip/brotli)
  - filmstrip with timestamp and page view changes
- lighthouse
  - "opportunities" tab contains useful suggestions for fixes
  - chrome extension + CLI tools

## Developing & Scaling Design Systems
- material UI
- why?
  - consistency

the ultimate goal is making something that is intuitive, users can transfer context from one area of the app to another

design and conversations around design are never done

document decisions! take the system out of the heads of the people who designed it

a design system only truly exists when others can use it independently of its creators

communication breakdowns - if it's not written down, it didn't happen

communication, especially in a way that messages 
  1. how systems change as scale incr
  2. tools for managing the dev and design of system at scale

## tools for managing the dev and design of system at scale
1. develop
1. document
1. deploy

### develop
ideas can be abstract
went deep with mockups, even interactions
"the pressure test"
  when applying to many screens, seeing where it breaks
worked w partners on redesigns of apps (calendar, inbox)
made sure it works for things like typography, color
studies on material.io spec

### document
1. there's too much to capture
1. we didn't figure it all out
1. we don't agree on everything

forces people to work through the gaps and make sure the system is strong and robust

limitations of examples
"glerb" 
pairing an example with a counter-example is good
examples are necessary but are not sufficient (sometimes we miss the subtle patterns)

great design principles are a shortcut to fluency (vocabulary)
design principles emerge from doing the design work
principles don't come at beginning, should describe how the system actually works, not how you think it should

e.g. MIO prin #4 one adaptive 
e.g. #9 motion provides meaning
material is the metaphor

### deploy
turning makers into educators
will have people not familiar w ux or new to field
what + why
if can explain fundamentals, they can take them forward and teach others
support multiple learning styles
deep docs, live talks, podcasts, videos
the artifact trap (perfectly organized spec)
  runs the risk of creating false boundaries and 

the more effort you put into making something "done", the more you resist change.

can also impose false boundaries on your users
key artifacts can mask the system's goals


## design systems as communication
talk to your audience, figure out what is and isn't working

modes at google
- newsletters
- team check ins
- design office hours
- launch reviews
- triage

number of users of system can be challenging and overwhelming, but start small, take first step of writing something down

systems don't "succeed or fail". it is not a binary. it will work some of the time. design is never done.

the impact of a design system scales with the effort you put in.