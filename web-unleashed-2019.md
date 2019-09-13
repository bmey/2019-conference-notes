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






# Built With ❤️: Why Developer Experience Matters


# Building Web Apps That Don’t Suck

