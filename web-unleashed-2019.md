# handles
- #WEBU
- #webu19
- @FITC

# oops I guess we're full stack - chris coiyer
"care about users and deal with the browsers, users, and devices"

the great divide - chris

front of the front & back of the front - brad frost

component-driven design

stacks
- LAMP
- MEAN
- Serverless
- STAR

11ty ssg

css-tricks/conferences

open source, user contributuions, jamstack hosting
- users can contribute fixes

used netlify + netlify CMS + cloudflare

no browser api to send email
- sparkpost 

"full-stack front end developer"

"fullstack" developer - @holtbt

# Dynamic Typographic Systems, Modern CSS, and Variable Fonts - Jason Pamental
most common interface w user is *words*

type is the voice of our words, how we 'hear' what we read

## design can reduce friction

key css features
- css custom props/variables
- calculations
- variable fonts
- ^ using them together

variable font = single font file that behaves like multiple fonts
- axes like slant, italicize, oblique, etc.
- axes also animatable

slant == just angle
italic == on/off (up to designer)

only accessible if type designer allows it

font weight, font stretch (width)

friction reduction - improcing readability

more about ratio/scale

"the role of the typographer has changed. we no longer decide; we make suggestions" - tim brown

media query to support dark mode (coming from OS) - newer to 
  prefers-color-scheme: dark
  add letter spacing to light text on dark background

accessibility
  crowding, older, high-contrast, line spacing

  dyslexia -- increase line space can increase their reading retention by 50%
    word-spacing

  "accessibility aids pop out"
  - dark mode
  - contrast
  - large text
  - spacing
  - ^ build it using css variables

## transfer friction: intentional tension
sometimes typography needs to be challenging, force you to stop and figure it out

"design is communication"

get away from one-layout solutions
- all content in medium/facebook/ny times looks the same

multiple templates per site (standard, editorial layout #1/#2)

"we're convinced that if users presented with slightest challenge, they are gone"

multi-layout example is all the same font, mostly same markup (plus one extra div)

first of type, first letter

word break

shorter hight & width columns are more engaging to read

"proxima nova" variable font

whitespace 1/3 on left, 2/3 on right

css shape to define polygon to contain text (scales w screen)

book layout mode example (use 100vw columns + swiping)

these ideas spreading, e.g. ada.georgia.gov

most modern browsers supported except ie11, use fallback

- "plex sans"
- monotype
- fonts.com
- google fonts api
- oswell?

faux-foundry.com
host the fallback font

progressive font enrichment
- serve you incremental patches to font files, not downloading all at once
- not as much problem for english, but japanese/korean = 20mb fonts

what the web wants
- adopt these features, learn how to do it well

optical sizing
font-variation-settings

persistence
participation
partnership


# Slashing Bad User Experience Using DevTools - Henri Helvetica
everyone is responsible for performance

90% of performance is front end

the front end is the most hostile development platform in the world

firebug was created to monitor http requests

## network panel
look for hints
long bars = resources taking long time to load
  == slow network, large resource, or both
filter can take conditions. e.g. >10kb
gear > use large request rows
  can see if resource being compressed (gzip/brotli)
filmstrip with timestamp and page view changes

## waterfalls

## throttling

## code coverage
FF beta: inactive CSS

## lighthouse
- median score is 40
- TSN score was 2
- "opportunities" tab contains useful suggestions for fixes
- chrome extension + CLI tools


# Developing & Scaling Design Systems
- building system / legos analogy
- material UI
- why?
  - consistency

the ultimate goal is making something that is intuitive, users can transfer context from one area of the app to another

communication, especially in a way that messages 

1. how systems change as scale incr
2. tools for managing the dev and design of system at scale

## how systems change as scale incr
starts w existing stuff - from existing sheets or other sites they love

hex code for color on a sticky note - way of codifying and remembering decisions

designer can't scale and can't tell every engineer or new designer what decisions have been made

design and conversations around design are never done

have to decide whether decisions apply to one or all products

can't scale if there is a single "oracle" designer that embodies the system

document decisions! take the system out of the heads of the people who designed it

a design system only truly exists when others can use it independently of its creators

communication breakdowns - if it's not written down, it didn't happen

having a central ux team > separated, needing n-1 channels of communication

creating a design system is fundamentally a design problem

design system is for the devs and designers, people building with it

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



# Built With ❤️: Why Developer Experience Matters
@amaltson
lots of companies investing in user experience, why not dev experience, too?

1. money
2. mental energy / decision energy
3. morale

2 weird errors, struggling to setup workspace

experience using a tool
experience working with other developers

"experience lifecycle"
- getting started
- making first changes/use
- day-to-day
- retirement

sympathy vs empathy
use an empathetic viewpoint

pair programming
pair up tool
in git, change author to 2 people
not sol for mobbing
Co-authored-by in trailing commit message (works in github)

mob up?

## working with other devs
### getting started
empty readme - rowan manning, post on writing a friendly readme

lightweight sequence diagrams, how does data flow through system
  plant UML

workstation setup
  tribal knowledge
  best to automate it

### first commit
green pipelines

github templates to guide user through what we want

### day to day
more important to stay consistent than use latest and greatest
- show small corner, if no buy in, then remove additions

keep a changelog, major changes happening to project

### retirement
retiring a project - add clear deprecation in readme
  - make sure all issues and PRs are closed
  
leave project in a finished, clean, buildable state (in case  revisited in future)

archive it
  - on github, doesn't allow people to submit new things

## experience workign w other devs

devs live day-to-day in IDE
GUI or CLI?
devs mostly live in cli
  start w cli first
  well-factored code might make it easy for others to contribute a web app, editor plugin, electron app, etc

### getting started
angry if empty readme
"how do I install this?"
provide packages that make it easy
  omnibus
  homebrew tap feature

put package in docker file/container w shell script
feels like a cli utility

friendly readme
one line installer
if not easy to install, use docker

### first contact
have init experience for migrations
e.g. config conversion from pair up to mob up
remove friction (go look up in user lookup)

migration from existing systems
do the work on user's behalf

### day to day
meaningful error messages
lint and shift feedback left

git ad . >> did you mean add?

levenshtein distance suggestions
  look for library
  if config setting not recognized, run against all known settings we're looking for

### retirement
clear migration path to other tools
automated migration


# Building Web Apps That Don’t Suck
@fharper
slides will be online

everyone: "coding is fucking hard"

business people: "coding is easy"

## architect

motivations
1. I'm microtasking
1. I'm local
1. I'm bored

"you don't have to play with all the toys", maybe you don't need it

don't reinvent the wheel

## design

mobile-first

fitt's law
> "the bigger and closer a target is, the easier it is to hit"

## optimize
- lighthouse
- cssnano

## http requests
- avoid or minimize 3xx redirects
- gzip encoding (htaccess, nginx.conf, web.config)
- image sprites
- use CDN
- cache the content
- configure the HTTP cache headers (apache, nginx)
- config response headers (iis)

## misc js
- avoid creating new objects when possible
- load JS files at the end of the page
- async load scripts and fetch data
- JSON is faster than XML

## misc
- don't fix it if it is not broken
- you don't always need a framework or a library
- put as much logic as you can on the server-side

## images
- use native image resolution (orig width, height)
- use the right format (PNG, JPEG..)
- use image preview for videos
- compress your images

imagemin-cli

shortpixel

## tests
- create tests: unit, integration
- use framework like mocha/qunit for JS/node
- test yourself

## the extra mile
think about security
* owasp cheat sheet series project

think about a11y
* try without a mouse


webhint (cli / browser)

## philosophy
1. insulate customer from complexity
2. help user accomplish goals faster and securely
3. make user awesome


fred.dev

## FOUC, death of progressive enhancement
change how we build

## graceful degradation
"I like an escalator because an an escalator can never break, it can only become stairs." - Mitch Hedberg

## progressive enhancement
conflating what is good for the user is what is good developers?

## FOUC
- FOIT (invisible text)
- FOUT (unstyled text)
- https://font-display.glitch.me
FUBC (unbehaviored content)

First paint WebPageTest.org
users tolerate stuff we create
  "hard to hear"

the great lie
> "tech-layered delivery (HTML > CSS > JS) is 'morally' superior"

"I can't watch this video, what's wrong with this picture?"

responsive design (ethan marcotte @beep)
real users don't resize the window

the great divide (in the web community) - css tricks
lots of tweets about what's wrong with the web
blame on both sides

> progressive enhancement is dead
-- tom dale

we created the divide on the tech

is "no JS" a relevant use case today?
mapquest example

can we fight for the user? put their concerns first?

HTML doc
"priority of constituancies"

adaptation

user agent --> user advocate

configuration

product + ui + ux = imprintable design
  - user is imprinted on the experience
  - #ImprintableDesign

progressive enh = devs & tech,
instead we need design focused on *each* person

flawed: designing for consistency
  - not concerned that button is slightly off

flawed: if the device can do it, the user wants it
  - showing webGL rendered map when low connectivity and 2% battery, no way to communicate my situation
  - how web content can affect power usage

who's using your site?
  - usually google analytics
  - statistics marginalize people
    - 1% people have 100% bad experience

common thread:
> *we* know better than any user does

E12y (empowerability)
  - how are you empowering people experiencing your site?
  - higher bar: empower **people**
  - #E12y

user -> custopmsr -> person
build a web that celebrates people

flawed: browser knows best
- there are things browser doesn't know
- CPU/Memory available? sure
- power unlimited? no
- data unlimited? no, costing user money
- hands usable? maybe, what if holding toddler in one hand
- lighting conditions? maybe, walking in the sun

can we just *ask* the person?
- pick your font size
  - some people it's a critical part of their experience
  - not necessarily just an a11y concern 
  - reccomendation from w3c

gmail > "load basic html" feature
- would you like the stripped down version of the experience?

flawed: people always want the most powerful experience

need a new term: people empathy

how do we begin practicing? start asking the question
give user more control
- precedents
- prefers color scheme
- prefers reduced motion
- save data
- reader mode
- client hints

currencies the user understands
- speed (slower than was before)
- battery level
- cost (bandwidth)
- how much do I want to spend vs save?
fidleity slider? what fidelity of experience do I want?
want a low fi experience because my situation is different right now

sites & apps built not in layers of tech but in degrees of fidelity

browser must veto server over resource responses, "no, I'm not going to load webgl right now"

we shouldn't wait for browsers to adopt

> **start building in *options*, start exposing *choices***

objections > we didn't ask to swap out old build for webpack
don't ask permission to make web better



