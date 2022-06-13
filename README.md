# Autonomous testing

> By the end of 2025, 30% of organizations will have implemented an autonomous automation strategy and will outperform competitors in quality and customer experience satisfaction metrics.

source: [Innovation Insight for Autonomous Testing](https://www.gartner.com/doc/3992325)


# Autonomous testing

Autonomous testing applies AI- and ML-based technologies to make the testing process independent from human intervention.

## The Path to Autonomous Testing

1. Manual, human driven
2. Automated
3. Autonomous

## From autonomous exploration to autonomous testing.

# Levels of Autonomy

There are several definitions of autonomy levels: [Gartner](https://www.gartner.com/doc/reprints?id=1-25Z5AK9P&ct=210506&st=sb), [Test.ai / Jason Arbon](https://medium.com/appdiff/test-autonomy-levels-7de7967d030e), [Applitools](https://applitools.com/blog/not-only-cars-the-six-levels-of-autonomous/).

In most cases there are inspired from automotive industry. Both, the Automotive autonomy [SAE classification](https://en.wikipedia.org/wiki/Self-driving_car#SAE_Classification) and the SW autonomy testing recognize 6 levels of autonomy.

## Automotive autonomy (SW testing inspired by)

_Human driver monitors the driving environment_

0. **No Automation**: The full-time performance by the human driver of all aspects of the dynamic driving task, even when "enhanced by warning or intervention systems".

1. **Driver Assistance**: The driving mode-specific execution by a driver assistance system of "either steering or acceleration/deceleration". Using information about the driving environment and with the expectation that the human driver performs all remaining aspects of the dynamic driving task.

2. **Partial Automation**: The driving mode-specific execution by one or more driver assistance systems of both steering and acceleration/deceleration. Using information about the driving environment and with the expectation that the human driver performs all remaining aspects of the dynamic driving task.

_Automated driving system monitors the driving environment_

3. **Conditional Automation**: The driving mode-specific performance by an automated driving system of all aspects of the dynamic driving task with the expectation that the human driver will respond appropriately to a request to intervene.

4. **High Automation**: The driving mode-specific performance by an automated driving system of all aspects of the dynamic driving task even if a human driver does not respond appropriately to a request to intervene the car can pull over safely by guiding system.

5. **Full Automation**: The driving mode-specific performance by an automated driving system of all aspects of the dynamic driving task under all roadway and environmental conditions that can be managed by a human driver.

Some videos explaining it in simple way:

- BMW Fully Car Autonomous Automated Driving (LEVEL 5) https://youtu.be/GA_NKVBpcVQ
- What are the different levels of Autonomous Vehicle? https://youtu.be/6592pKyQfyE

## SW Testing Autonomy Levels

Gartner definition of SW Testing Autonomy Levels:

0. Manual testing
1. Assisted testing
2. Partially automated testing
3. Integrated automated testing
4. Intelligent automated testing
5. Autonomous testing

## Features / functionalities required achieve autonomy levels

### 0. Manual testing

_The human is in complete control of the test activities and scripts at all times. There is no tool assistance._

- Features: Documentation tools
- Examples: Excel, Word, Jira

### 1. Assisted testing

_The human writes test automation scripts that can repeatedly execute a test case, using data-driven features to cover multiple input scenarios. The *focus is on scripting and coding*, while tools such as test editors and simple capture/replay provide some assistance._

- Features: TODO
- Examples: Selenium + Java/Python/JavaScript, Cypress.io, Playwright

### 2. Partially automated testing

_*The human enhances test automation scripts*, either coded or codeless, that were created using recording facilities, log file analysis, customer journey analysis or model-based testing (business process model, application model, etc.)._

- Features: Record & play tools, xDD?(TDD, BDD, etc.) - _only in case_ it is provided into testing as input created as output from analytical activity.
- Examples: Selenium IDE, Dredd

### 3. Integrated automated testing

_The human defines the high-level intent of a test case for a particular business process (e.g., by visually defining the business process workflow). Tests are then executed based on this definition._

- Features: TODO
- Examples: TODO

### 4. Intelligent automated testing:

_Testbots perform exploratory testing and generate and execute most test scenarios independently. Tests will actively run through fallback scenarios and test scripts will be automatically updated (e.g., when a test case fails because of an updated component of the application under test)._

- Features: TODO
- Examples: TODO

### 5. Autonomous testing:

_No human assistance is needed and machines are able to evaluate an application, decide what, when, where and how testing should be performed, and summarize the results to provide a release/no-release decision based on test results_

- Features: TODO
- Examples: TODO

# Current market and future potential

Current estimated adoption rate of autonomous testing by Gartner (report published 28 October 2020) is less than 5% of the addressable market. The same report states that by the end of 2025, 30% of organizations will have implemented an autonomous automation strategy.

# Reinforcement learning

Execution flow might be built based on the algorithm used games to train bot to play games
https://www.youtube.com/watch?v=t1A3NTttvBA

## Reinforcement learning with TensorFlow

https://github.com/GoogleCloudPlatform/tensorflow-without-a-phd
https://github.com/tensorflow/agents/blob/master/docs/tutorials/1_dqn_tutorial.ipynb
https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf

# Natural Language Processing (NLP) Based Test Automation

Test script development is a tedious process and updating and maintaining them for every change does not come easy. A lot of time is spent on the initial test script authoring.

Though there are other approaches like the Record and Playback method to automation testing, NLP based testing is not only intuitively easy but reliable.

With NLP, you can still write your own tests but without the complexities of traditional test automation.

Natural language processing is an artificial intelligence specialty by which machines can identify, interpret, and generate human language. NLP arises from the intersection of many disciplines such as computational linguistics and computer science. The aim of NLP is to build machines that can approximate human language comprehension.

sources:

- https://testsigma.com/blog/natural-language-processing-nlp-based-test-automation/
- https://www.functionize.com/blog/how-nlp-will-drive-the-future-of-software-testing/

## NPL with TensorFlow

https://www.youtube.com/playlist?list=PLQY2H8rRoyvzDbLUZkbudP-MFQZwNmU4S

words > sentences
actions > scenarios

sentiment > failure level?

sequence length:

- simple solution: [padding](https://youtu.be/r9QjkdSJZ2g), or [here](https://colab.research.google.com/drive/1qDCHeK-tym0ecwAeHhz_bWeZhjOPZPj7)
- advanced approach: [ragged tensor](https://www.tensorflow.org/guide/ragged_tensor)

# ML and Testing

Examples of application the ML into testing:

- NLP and natural language generation research may map to test case generation.
- Game theory and reinforcement learning may map well to the problem of discovering a system and hunting for bugs.

Other

- Object Recognition
- Perceiving Application State
- Execution sequence generation: see NPL sequence-to-sequence problem (https://en.wikipedia.org/wiki/Seq2seq) ... to generate more logical sequences of actions
- Test flow generation: see

# Autonomous Testing Tools
List of tools trying to achieve fully autonomous testing or at least so-called autonomous assistance

## Providers / potential solutions ?

http://www.applitools.com - currently good for visual testing / validation

http://www.appvance.ai

- step 1: the tool generates application blueprint in a few minutes
- step 2: cognitive script generation (from production log provided in e.g. csv)
- step 3: execute test which could be functional, security or performance

http://www.botium.ai - more for chat bot testing

http://www.diffblue.com - more for unit testing

http://www.functionize.

- record & play / low-code / codeless tool
- features: JavaScript custom coding available, DB & API connectivity, 2FA
- code is generated by ML (NPL) from plain English

http://www.mabl.com

http://www.prodperfect.com - autonomous E2E software testing tool, collect data from production, generates tests and execute them

http://www.sealights.io - DevOps, more focused on code, not very clear and specific on their website

http://www.testcraft.io - features: recording tests, AI auto-fix for flaky test, modeler for design tests

http://www.testim.io -

http://www.testmodeller.io

http://www.testsigma.com

https://autonomiq.io/ - aquired by [Saucelab](https://saucelabs.com/platform/low-code-testing) in Feb 2021

https://www.accelq.com/

https://www.functionize.com/

https://testrigor.com/

https://apptest.ai/

https://www.eggplantsoftware.com/

https://www.aifex.fr/

## Visual testing tools

https://github.com/Visual-Regression-Tracker/Visual-Regression-Tracker

https://percy.io/

https://github.com/rajdeepv/nakal - no autonomous testing 

https://crossbrowsertesting.com/visual-testing


# YT ideas

https://youtu.be/R-S94tYmH04

[![Autonomous Visual Regression Testing](https://img.youtube.com/vi/R-S94tYmH04/0.jpg)](https://youtu.be/R-S94tYmH04)


https://youtu.be/EBtuOj9hdKc

[![Autonomní testování](https://img.youtube.com/vi/EBtuOj9hdKc/0.jpg)](https://www.youtube.com/watch?v=EBtuOj9hdKc)


https://youtu.be/Q8s8ENQLWfA

[![Autonomous Testing and the Future of Software Development](https://img.youtube.com/vi/Q8s8ENQLWfA/0.jpg)](https://youtu.be/Q8s8ENQLWfA)


https://youtu.be/Q8s8ENQLWfA

[![OPENING KEYNOTE Test Automation’s Next Great Wave: Autonomous Testing](https://ewig5qf9cgn.exactdn.com/wp-content/uploads/2022/02/220224-FOT-Frameworks-EMEA-Session-Cards-831-%C3%97-542-px-768x501.jpg?strip=all&lossy=1&ssl=1)](https://applitools.com/event/opening-keynote-test-automations-next-great-wave-autonomous-testing/)



# Resources & interesting sources

https://medium.com/appdiff/test-autonomy-levels-7de7967d030e

https://www.gartner.com/doc/reprints?id=1-25Z5AK9P&ct=210506&st=sb

https://www.pnsqc.org/wp-content/uploads/2018/09/38-Santiago-AI-Driven-Test-Generation.pdf

https://sersc.org/journals/index.php/IJFGCN/article/view/5815/3604

https://medium.com/appdiff/test-autonomy-levels-7de7967d030e

https://www.coursera.org/learn/machine-learning

https://testautomationu.applitools.com/testing-machine-learning-models/
