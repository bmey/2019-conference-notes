# Thinking in Tests (Jim Shore)

Some think TDD is just writing tests first, then writing app code. Needs to be thought of as a continuous process w short cycles.

TDD is less about testing and more about having control and understanding of your code.

Evolutionary design - solve the problems in front of you today, and have freedom to refactor at will and simplify architecture later.

"Embrace change", plan to adapt
honeymoon and backpacking examples
have plans, but also plan to adapt

experiment, get feedback, learn, and adapt

# Scaling R&D without dedicated QA (Adam Archer - Shopify)

4,000 employees
800,000 businesses
$125B sales

focusing on the core
800 deploys per day, 40 to core
83k request per seconds

all done w/out a QA team
believe QA is part of developer's role
devs own their own changes from authoring to QA to deployment

## tools and process
tools and process don't matter

`dev clone shopify`

`dev up`

`dev server`

### pull requests
give people context they need to be successful

PR template
- what are you trying to accomplish
- what approach did you choose and why
- impact of changes
- did you...
  - test these changes?
  - can this be rolled back?


tape bot posts automated comments to add context
we test like crazy
we code review

`dev tophat push`
`dev tophat pull`
`dev tophat stop`
`dev ios tophat XXX` = run on local simulator, too
associated w PR, can use state of machine from PR

### deploying to prod
- "shipit" tool (merge queue)
- PR > queue > canaries > monitory/verify > deploy to rest
- shipit manages deploys, no manual intervention required
- automated messages to say what's wrong/why locked (e.g. during a rollback/revert)

chat ops, ops uses chat bots to control things
spy bot sends you a direct message "go watch the ops channel, your PR is about to deploy"
deploy dashboards (catered to canary state and prod)
- includes business metrics like num signups / purchases dropped?

Dev ATC rotation

Tools and process don't matter, culture is key

## culture
can't control this, best you can do is set values to aspire to

shopify values
- we are powered by a trust battery, expect people to act autonomously and in control of own decision making
  - as you do more things, battery charges and grows, more opps open
- we are contant learners, roles aligned w personal growth plans
- we default to open internally
  - CLT host AMAs all the time, messages are more public
- we thrive on change
  - not just being comfortable
- we are merchant obsessed, deep empathy, encourage employees to run their own shops, be a merchant yourself, go talk to merchants, find about their problems
  - tell a story about individual merchants all the time (their livelihood depends on us)

engineering
- devs ship their own changes
- leave signposts
- reduce friction
  - QA teams come when devs don't have time and support to do this effectively
tl;dr = when things are hard, going wrong, we invest, projects to improve this
- devs own their own time, devs are free to help others and solve problems they want to (even if it's someone else's problem)


# old solutions to new problems - josh justice (big nerd ranch)
the problem now is test maintainability

5 patterns from "xUnit test patterns (refactoring test code)" by gerard meszaros

takeaways
- new testing approaches
- clearer explanation of benefits
- shared language and support

"code smells" > "warning signs"

## warning sign: flexible test (using conditionals in tests)
sol = simple tests

## mystery guest
tests should be obvious, don't abstract setup away
approach: inline setup
approach 2: delegated setup (creation methods)
  e.g. createAddress
approach 3: common setup (beforeEach)
  this can still be a problem especially for nested or long describe blocks

## irrelevant information
don't distract readers with details that don't matter

sol: minimal fixture
sol2: parameterized creation method
  - intent-revealing names
```javascript
function createAddress(overrides = {}) {
  return {
    ...defaultAddress,
    ...overrides,
  };
}
```
sol3: test data creation libraries
  if find yourself writing the same creation methods a lot

## interacting tests
problem = shared fixture again
sol: creation methods, fresh fixture
  each test creates it's own fixture for use
  e.g. `_.cloneDeep(orders[0])`

## production logic in tests
"why am I copying the production code in the test?" what value is this bringing?
if logic wrong in one, wrong in both

solution: hard-coded test data (can be seen as a smell)
must decide what is best for you, trade offs

## takeaway
let's talk in patterns, take advantage of our rich testing history

# robust tests for unconventional environments - carolina pinzon (dapper labs)
tests that make dev lives better will make a better product


# How to build the TDD habit in your team - Ryan Marsh

emotional, not based on logical choices

"the power of habit" charles duhigg

basal ganglia - where habits are stored

cue > routine > reward

conway's game of life exercise
- delete your code! (no reward)
- bell throughout the day, then 3 minute TDD cycle

ryan@thestack.io

# 99% is not enough - Isaac Schlueter
isaacs

# Pros and Cons of UI Testing Tools - Clare So
selenium, puppeteer, cypress

# tests > types - Colin Ihrig (Joyent)
there are tradeoffs for types that most devs and project managers don't consider

types add verbosity & complexity

a language is a big dependency, their bugs are now your bugs
"The TypeScript Tax"

can still provide a type declaration file (.d.ts)

# Integration testing w Cypress - Nancy Du (rangle.io)
found that lots of clients' test suites are
- no integ, skewed to lots of unit
- no integ, equal amount of e2e and unit
- only unit
- only manual

integration tests can be hard for stakeholders to understand

mocks become difficult to setup + maintain

write based on AC of user story

use cypress

auto-record package to make managing mocks easier to maintain

# test flakiness - jason palmer (spotify)
jest core team member

auth of jest-junit

## cost of flakiness
- time & money (retriggering ci builds, local builds, etc)
- loss of confidence (resort to manual verification)

## task team
tasked to reduce time it takes to get code merged for iOS, android, and desktop web app

initially focused on builds, shifted to why builds were failing

## causes of test flakiness
- hard to "see" flakiness. it's not obvious by looking at the code
  - we are not immune
- example shown is e2e test making network requests, flaky by nature
- inconsistent assertion timing
  - async await test + dom-testing-library
  - `await wait(() => ...)`
- reliance on test order
  - shared state between tests
  - reset state between tests
- e2e tests
  - write less of them

polly-jest-presets

vcr, auto recording and playback of network requests

!measure flakiness, show devs their tests are flaky, how long it takes, how often they fail

flakybot - exercise tests to ensure they aren't flaky

master guardian - detects flaky tests
- auto creates JIRA tickets for owners of flaky tests
- sends team about the new tickets on slack
- retries flaky pre-merge tests in order to avoid failing PRs and blocking other devs

## how do I build these tools?
**start w data**
- output JUnit.xml from your tests
- create a DB of that info
- jest-junit

**choose a flakiness detection technique**
1. most accurate
    - run each updated test 50-100 times in CI
    - flakiness % = failed runs / total runs
    - did this for awhile at spotify, but chose next
2. the most Ok
    - record test results for every master commit
    - fast and easy to implement
    - not as accurate
3. the most badass
    - run each changed test 3-5 times after instrumenting for code coverage
    - calc the coverage delta between each run
    - warn about potentially being flaky, would show that test goes down diff paths and is not deterministic

@palmerj3

# Component-driven design & viz test coverage - Michael Shilman (chroma)
maintainer of storybook
@mshilman

ui states are combinatorial
every ui test is an integration test
- slow to spin up browser
- flaky, lots can go wrong
- underspec'ed - HTML != viz output

how?
- break down designs into components
- catalog relevant states for each component as a story
- build out components __in isolation__
- recompose components into screens

^ this is actually testing

chromatic (automated viz tests for storybook)

open source project > visual coverage as a future add-on for storybook