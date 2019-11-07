# Pushing Through Friction - Dan Na
"if only we did this one 'obvious to me' thing, it'd be better"

talks.danielna.com
@dxna

spent lots of evenings feeling frustrated about work
found repeating lots of 1:1s

1. what causes friction?
2. how can orgs and individuals overcome?

## what is friction?
friction is not only technical

friction is uncomfortable

pushing through this friciton is worth it, often people will leave to avoid these problems, but that means there is friction everywhere

## why does it occur?
company growth
uber example
mostly painful for mid-sized companies

startups are trying to survive, trade long-term problems for shipping fast

"teams executing in concert with operational excellence"

this growth and problems are inevitable

some of this friction is preventable

plane crash example (aviation safety)
- procedures in place for safety, procs never performed
- ignoring an alert once >> always, becomes normal

"normalization of deviance"
- danluu.com/wat
- deviant behavior becomes the norm
- what things do you first encounter at your job??
- this is within our control

orgs and processes incur friction ***slowly***

## how do we fix it?

### orgs
fix #1 short term - discrete fixes
  - doc sources of truth and keep them updated

single points of failure
  - leads to burnout
  - when those leave, the company is screwed

create a culture of documentation
  - make updating it a part of AC

fix #2 - adopt processes to vet tech decisions
RFC - request for comments, template example on slides

tanya reilly - check out blog post

send survey to all new hires month after starting - 
  how could this be better, what's missing, what have you seen work better elsewhere?

### long-term (org)
fix #1 address hard truths kindly
hospital example
- workers afraid to speak up
- doctor hard to confront, sensitive about his hand writing
- avoiding conflict in leadership roles can have disastrous outcomes

project example, discover major problem
1. continue towards failure
2. stop the project
^ decided to continue to launch
sunk-cost fallacy
people left - couldn't trust company could make correct decisions anymore

acknowledgement for work and effort, sensitive to emotional impact, concerned for well-being

fix #2 celebrate the glue work
noidea.dog/glue

often considered non-promotable work, but this reduces org friction

make glue work promotable work, mandatory for promotion

fix #3 make psychological safety ____


## individuals
develop and own your sense of agency

intrinsic motivators
- autonomy
- purpose
- mastery

example: billing components > checkout ui

need courage, persistence, and pragmatic optimism

there's often the correct path and the easy path. take the correct path because it will lead to to better outcomes

caveat - don't be a hero or an asshole

### strategies
strat#1 have important discussions face to face
- or video conference

strat#2 get to know other people on other teams in the org

strat#3 new idea? try it once
- will often yeild valuable insights

## this is the job
push through with optimism and kindness


# how to craft accessible experiences
@georgezamfir, slack
- #a11y questions

common perception that you can do a11y by accident, this doesn't make sense
experience not considered in this case
fixing anything after the product was built (including a11y) is expensive

new mindset: a11y is an experience
- F6 key to switch menu by section, arrow keys
- don't read all replies / all content, mabe just excerpt

window-based screen reader that displays text?

call a11y out in all specs (design, tech, product)
  - spec this together (cross-functional)
  - QA - not much extra at this point, should just work

standard nav patterns for keyboard
- wrote a doc derived from native UI (windows/mac)
- did deviate, but made conscious decisions

test w all screen readers
- ctrl+k shortcut, bug between apple and chromium
- speced experience, if differences, came up w workarounds, try to make them all work the same way
- jaws tries to be smart if things aren't accessible, can give mixed signals
  - if something doesn't work in NVDA, can indicate real bug that jaws might be hiding

- he tests w NVDA

- added a11y success criteria
  - color
  - keyboard
  - screen reader experience
  - ^made sense for slack, if have product that's mostly reading, screen reader or content heavy, start w keyboard

not easy, but need to start



# Measuring the Adoption of Web Performance Techniques - Paul Calvano

HTTP archive tracks how the web is built
- runs on top of lighthouse / web page test

rules from 2008 most boil down to reducing requests

PageSpeed Insights (lighthouse)

crazy cat shop example
- has an image problem

images are biggest offender across the web

saw side benefit, once reduced/lazy load images, might have other side benefits like faster loading of JS resources

30% sites received score of zero for image optimization

important to choose the right image format
- flowcharts exist on web

responsive images?

brotli compression algo
- 15-25% better compress ratio than gzip
- trade-off, longer speed for compress/decompress
- can pre-compress resources?
- compression level estimator

nginx default compress level = gzip1, could be better and is configurable
- check yours!

to bundle or not to bundle?
- depends on your situation
- consider your "coverage" tab in chrome devtools
- 48% of sites have more than 100kb of unused css
  - unused resources also add processing cost

"cost of javascript" article
- v8.dev/blog-cost-of-jsvascript2019

web page test feature - single point of failure test
  - show what happens when 3rd parties don't work correctly

lots of css & js being done before start render

diff between bandwidth and latency
- CDN can reduce latency

resource hints
- dns-prefetch
- preconnect
- prefetch
- prerender
- preload

3rd party protocol overhead
- preconnect > dns-prefetch
- google fonts uses preconnect
- recommend preconnect in http response header

connection overhead for sharded hosts

cache! the fastest request is the one you don't make
- use cache-control headers
- serve more resources over 1st party connections
- check out long cache TTL lighthouse score

amanac.httparchive.org
- coming nov 2019

HTTP archive guided tour bit.ly/2JmDnSH

# Mentoring, Teaching, and advocating in the age of influencers

## mentoring vs teaching
mentoring = focus on personal, individual growth
answer questions in public

"worklife" podcast by adam grant
- networking for people that hate networking episode
- build up your skills first, build yourself up so people will come to you
  - start teaching by writing blog posts

## do you consider yourself an influencer?
coding instagram


## one weird lesson
- use mayo instead of butter for grilled cheese
- indian food - flavor from cumin, warm oil, throw in cumin seeds, not burned, take seeds off
- xyz 


## how to build levelled learning experiences?
- self-driven workshops, try to pair w ?similar/different experience levels??
- lunch and learns, be friendly fun and engaging
  - be entertaining in slides (beyonce)
  - LL cooljs
  - wutangular
  - let people know there is a path and are approachable

how use viz for teaching?
1. create viz's
1. teach how to think with data and create viz
- be precise w viz so people aren't confused/interpet the wrong way
- viz that are colorful, bright, interactive, maybe animate, but has a purpose/reason
  - reached a woman and allowed her to connect w her son on computer science

local public library usually open to having teachers come and speak/teach

how to build online courses/presence from scratch
- intentionally and consistently
- what is your thing? for him, twitter and youtube, but can vary
- showed up consistently for 8 years
- be prepared for platforms to go down
  - get your stuff in a protected place
- be genuine and be yourself
  - share about who you are, your kids, we're all human and have own interests
  - people have a culture bond bc of it
  

? how to build people up if most are juniors?
? challenges when working as a remote worker? with a remote worker?
? what resources can my daughters use?


# surviving your stack - kevin daly
you shouldn't listen to anyone
should be based on 
- data
- use cases
- cost
- talent/personnel

not bc
- conference
- blog on internet
- tech giant using it
- ^don't be a copy cat

his definition of stack
process
dev > commit > build/test > deploy > runtime env > users

*stack as culture*
people <> process <> technology
organic

how do you choose a stack?
you are not google, your problems are not the same

a cautionary tale (the hype machine)
akka is cool but...
nobody at the company knew how it worked
running at 1% utilization, huge cost
90% market penetrated

go fast and break, or do it the right way?
why not both?
need to be strategic

people
recruiting should be more conversational
how do they learn? do they believe and match company values?
everything else can be learned or trained
do a whiteboarding exercise
  brainstorm w the candidate

lessons learned from RBC ventures (built 16 products)
- agility
- consistency
- flexibility
- productivity + cost
- job candidate availability

lessons - gotchas
- what is a full stack dev? can't know everything
- what happens with a partial product market fit?
- technical debt?
- node stack doesn't fit every use case?


takeaways
- understand your scale from the most pessimistic to most optimistic view
- don't over-engineer
- know the size of your market
- avoid the hype machine
- ! stack is not technology, but people, process, and tech
- !!dogmatically pursuing a stack as a single source of truth is a recipe for disaster

questions
- how to give people room to experiment/grow? ask for business cases, build prototypes
- how to get resisting people on board? use a matrix of the decision, have data that shows how we reached a decision
- how to avoid tech debt? testing, code reviews
  - shout out to sonar, documenting tech debt
  - consider cost to testing


# open source / you belong here - jason lengstorf
@jlengstorf
learnwithjason.dev
* live pairing with others to build things
* slides at git.io/you-belong-here

open source is good business

awkward social dynamcis
walk into a room and say - "hey, can I touch your stuff?"

creating a community doesn't happen by accident, it is deliberate
- actively reach out and welcome new contributors
  - do they need any help getting that PR up and through?
- remember how steep the learning curve can be
- invest in community as a primary measure of success
  - if community growing, more represented, more modeling behavior we want to see, that is the metric (not just money)
  - people want to be part of a community that treats them well and makes them feel like they belong

stack overflow committed to treating people well as a core value, core part to their success

dev.to online community to help people learn code
hacktoberfest > open 5 PRs

***you*** belong here

we have a tendency to see our problems as puzzles, once solved/assembled can leave it alone
- not how people work
- community like a campfire, need materials and initial fire, need to tend the fire & keep fueling it or it will burn out
- once going, keeps everyone warm, everyone can pitch in and then it doesn't feel like so much work.

pac-man circle, don't be closed, room for people to join
"good first issues" labels / "help wanted" labels
coding coach - pair ppl with mentors

example: marcy stutton's gatsby accessibility statement

swag store! (example, gatsby swag)
  - have kyber swag?

safety

read "the culture code" by daniel coyle

April wensel - "compassionate coding"


# connecting the dots and tying threads
@jpamental / rwt.io

rwt.io/newsletter

## think, then do
- thought is more important than speed
- design apis first
  - allows to expose only what you need
- great games
  - start w a purpose
- great replies
  - great feedback is specific, goal oriented, organized

## we make choices based upon the idea of "open"

## let's talk about friction
- in conversation
  - "turn friction into healthy productive debates"
- lies within the gaps between how things are and how they should be
- to create interest
  - sometimes typography needs to challenge you

## being human: caring for ourselves
- we're still browser people who are the shepherds of design, ux, perf, and a11y
- how we relate to each other
  - rather than saying "improve this", provide suggestions/examples
- caring for people
- to people, planet, and devices
  - what can we do about it?
- are we giving people a choice?
  - we assume the person wants the most powerful experience
  - are we being respectful of their choices?
- to devices
  - features have weight and consequences
- to the planet
  - constant increases in processing load have consequences
    - lost resources, increased waste
- we're all in this together
  - web / planet
  - projects (design, product, dev)
  - a community is mearured not by its good actors but by the worst actors they tolerate
    - there are real consequences for people's behavior
- let's be human together