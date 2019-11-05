# assert js

## Invest in improvements
### Scaling R&D without dedicated QA (Adam Archer - Shopify)
When things are hard or going wrong, **invest.** Create projects to improve.
(my takeaway) create a learning culture and organization

## Testing
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

- variable font = single font file that behaves like multiple fonts
  key css features
  - css custom props/variables
  - calculations
  - variable fonts
  - ^ using them together

- accessibility (dark mode, high-contrast, line spacing, word spacing)
  - dyslexia -- increase line space can increase their reading retention by 50%

## lighthouse
everyone is responsible for performance
- lighthouse
  - "opportunities" tab contains useful suggestions for fixes
  - chrome extension + CLI tools

## Developing & Scaling Design Systems
- material UI
- why? consistency

the ultimate goal is making something that is intuitive, users can transfer context from one area of the app to another

design and conversations around design are never done

a design system only truly exists when others can use it independently of its creators

### document
1. there's too much to capture
1. we didn't figure it all out
1. we don't agree on everything

the more effort you put into making something "done", the more you resist change.

# Built With ❤️: Why Developer Experience Matters
lots of companies investing in user experience, why not dev experience, too?

1. money
2. mental energy / decision energy
3. morale

"experience lifecycle"
- getting started
- making first changes/use
- day-to-day
- retirement

experience using a tool
experience working with other developers

## working with other devs
### getting started
friendly readmes
automate workstation setup

### first commit
templates to guide user through what we want

### day to day
more important to stay consistent than use latest and greatest
keep a changelog, major changes happening to project

### retirement
retiring a project - add clear deprecation in readme
leave project in a finished, clean, buildable state (in case  revisited in future)

## experience workign tools
  start w cli first
  well-factored code might make it easy for others to contribute

### getting started
"how do I install this?"
- friendly readme
- one line installer
- if not easy to install, put package in docker file/container w shell script

### first contact
have init experience for migrations

### day to day
meaningful error messages
git ad . >> did you mean add?

### retirement
clear migration path to other tools
automated migration