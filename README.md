# Autonomous testing

> By the end of 2025, 30% of organizations will have implemented an autonomous automation strategy and will outperform competitors in quality and customer experience satisfaction metrics.

Source: [Innovation Insight for Autonomous Testing, Gartner 2020](https://www.gartner.com/doc/3992325)

# Autonomous testing

Autonomous testing applies AI- and ML-based technologies to make the testing process independent from human intervention.

## The Path to Autonomous Testing

1. Manual, human-driven
2. Automated
3. Autonomous

## From autonomous exploration to autonomous testing.

# Levels of Autonomy

There are several definitions of autonomy levels: [Gartner](https://www.gartner.com/doc/reprints?id=1-25Z5AK9P&ct=210506&st=sb), [Test.ai / Jason Arbon](https://medium.com/appdiff/test-autonomy-levels-7de7967d030e), [Applitools](https://applitools.com/blog/not-only-cars-the-six-levels-of-autonomous/) or [SmartBear](https://smartbear.com/resources/ebooks/six-stages-from-manual-to-autonomous-testing/).

In most cases, there are inspired by the automotive industry. Both, the Automotive autonomy [SAE classification](https://en.wikipedia.org/wiki/Self-driving_car#SAE_Classification) and the SW autonomy testing recognize 6 levels of autonomy.

## Automotive autonomy (autonomous SW testing adopted)

_Human driver monitors the driving environment_

0. **No Automation**: The full-time performance by the human driver of all aspects of the dynamic driving task, even when "enhanced by warning or intervention systems".

1. **Driver Assistance**: The driving mode-specific execution by a driver assistance system of "either steering or acceleration/deceleration". Using information about the driving environment and with the expectation that the human driver performs all remaining aspects of the dynamic driving task.

2. **Partial Automation**: The driving mode-specific execution by one or more driver assistance systems of both steering and acceleration/deceleration. Using information about the driving environment and with the expectation that the human driver performs all remaining aspects of the dynamic driving task.

_Automated driving system monitors the driving environment_

3. **Conditional Automation**: The driving mode-specific performance by an automated driving system of all aspects of the dynamic driving task with the expectation that the human driver will respond appropriately to a request to intervene.

4. **High Automation**: The driving mode-specific performance by an automated driving system of all aspects of the dynamic driving task even if a human driver does not respond appropriately to a request to intervene the car can pull over safely by guiding system.

5. **Full Automation**: The driving mode-specific performance by an automated driving system of all aspects of the dynamic driving task under all roadway and environmental conditions that can be managed by a human driver.

Some videos explain it in a simple way:

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

## Features / functionalities required to achieve autonomy levels

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

_No human assistance is needed and machines can evaluate an application, decide what, when, where and how testing should be performed, and summarize the results to provide a release/no-release decision based on test results_

- Features: TODO
- Examples: TODO

# Reinforcement learning

Execution flow might be built based on the algorithm used games to train a bot to play games https://www.youtube.com/watch?v=t1A3NTttvBA

## Reinforcement learning with TensorFlow

https://github.com/GoogleCloudPlatform/tensorflow-without-a-phd
https://github.com/tensorflow/agents/blob/master/docs/tutorials/1_dqn_tutorial.ipynb
https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf

# Natural Language Processing (NLP) Based Test Automation

Test script development is a tedious process and updating and maintaining them for every change does not come easy. A lot of time is spent on the initial test script authoring.

Though there are other approaches like the Record and Playback method to automation testing, NLP-based testing is not only intuitively easy but reliable.

With NLP, you can still write your own tests but without the complexities of traditional test automation.

Natural language processing is an artificial intelligence specialty by which machines can identify, interpret, and generate human language. NLP arises from the intersection of many disciplines such as computational linguistics and computer science. NLP aims to build machines that can approximate human language comprehension.

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

Examples of application of the ML into testing:

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

- step 1: the tool generates an application blueprint in a few minutes
- step 2: cognitive script generation (from production log provided in e.g. csv)
- step 3: execute test which could be functional, security or performance

http://www.botium.ai - more for chatbot testing

http://www.diffblue.com - more for unit testing

http://www.functionize.

- record & play / low-code / codeless tool
- features: JavaScript custom coding available, DB & API connectivity, 2FA
- code is generated by ML (NPL) from plain English

http://www.mabl.com

http://www.prodperfect.com - autonomous E2E software testing tool, collect data from production, generates tests and executes them

http://www.sealights.io - DevOps, more focused on code, not very clear and specific on their website

http://www.testcraft.io - features: recording tests, AI auto-fix for a flaky test, modeler for design tests

http://www.testim.io -

http://www.testmodeller.io

http://www.testsigma.com

https://autonomiq.io/ - acquired by [Saucelab](https://saucelabs.com/platform/low-code-testing) in Feb 2021

https://www.accelq.com/

https://www.functionize.com/

https://testrigor.com/

https://apptest.ai/

https://www.eggplantsoftware.com/

https://www.aifex.fr/

https://dev-tools.ai/

https://touca.io/

## Visual testing tools

https://github.com/Visual-Regression-Tracker/Visual-Regression-Tracker

https://percy.io/

https://github.com/rajdeepv/nakal - no autonomous testing

https://crossbrowsertesting.com/visual-testing

# Video ideas

## EN

- [(EN) Autonomous Visual Regression Testing | Marcel Veselka, Jan Beránek a Ondřej Winter](https://youtu.be/R-S94tYmH04)
- [(EN) Autonomous Testing and the Future of Software Development](https://youtu.be/Q8s8ENQLWfA)
- [(EN) Test Automation’s Next Great Wave: Autonomous Testing](https://applitools.com/event/opening-keynote-test-automations-next-great-wave-autonomous-testing/)

## CZ

- [(CZ) Autonomní testování│Ondřej Winter a Jan Beránek](https://youtu.be/EBtuOj9hdKc)

# Current market state

## Market size and predictions

![Market size and predictions](/images/Market-size-and-predictions.png)

## Hype Cycle for Agile and DevOps, 2022 - Autonomous Testing

Full report [here](resources/Hype-Cycle-for-Agile-and-DevOps-2022.pdf)

![Hype Cycle for Agile and DevOps, 2022](/images/Hype-Cycle-for-Agile-and-DevOps-2022.png)

[Gartner Hype Cycles, Explained](https://youtu.be/jB1RDz9jaj0)

**Analysis By:** Joachim Herschmann, Jim Scheibmeir

**Benefit Rating:** High

**Market Penetration:** 5% to 20% of target audience

**Maturity:** Adolescent

**Definition:**
Autonomous testing comprises AI- and ML-based technologies and practices to make software testing activities independent from human intervention. It continuously improves testing outcomes by learning from the data collected from performed activities. It extends traditional test automation beyond the automated execution of test cases to include fully automated planning, creation, maintenance and analysis of tests.

**Why This Is Important**
Software engineering leaders seeking to release faster without degrading quality are looking for more efficient ways of testing, which includes all phases of the testing life cycle. As such, autonomous testing is a driver for a holistic approach to automating the broader set of quality and testing activities related to requirements quality, design quality, code quality, release quality and operational resilience in an integrated way. This increases the degree of autonomy for those activities.

**Business Impact**
The adoption of autonomous testing has the potential to significantly improve an IT organization’s ability to serve and delight its customers. It can be an enabler for adjusting testing scenarios and overall software quality parameters as part of a continuous quality initiative aimed at optimizing end-user experience. It will also help to constitute a closed-loop system that provides continuous feedback about critical quality indicators.

### Drivers

- A high dependency on human expertise and interaction limits how quickly modern digital businesses can design, build and test new software.
- Where automated testing is already in place, current levels of automation often remain below expectations due to a continued dependency on human intervention in maintaining the automation as applications under test (AUT) evolve.
- The pressure to innovate quickly for market differentiation without compromising on quality relies both on a higher velocity and a higher degree of autonomy of the related activities.
- While delivery cycle time is decreasing, the technical complexity required to deliver a positive user experience and maintain a competitive edge is increasing. The answer is not more testing but more intelligent testing enabled by AI technologies.

### Obstacles

- Risk of doing nothing: Waiting until feature-complete autonomous testing solutions are available leads to a loss in competitive advantage, and reduced agility and innovation.
- Unrealistic goals: Underestimating the time required to acquire new skills and setting wrong expectations about the time required to become successful can be obstacles.
- Managing data quality: Gathering, cleaning and processing of data and training of the model are not trivial tasks and require adequate skills. Moreover, they are not yet autonomous processes.
- Internal pushback: Autonomous testing requires significant investment in new areas such as data science and analytics. While this will motivate some team members, others may see the approach as a threat to their known way of working and they may be afraid to adjust.
- Immaturity of tools: Currently available tools are still relatively new, have a narrow scope of technology coverage and still need to prove their value.

### User Recommendations

- Set the right expectations about where autonomous testing can provide value, what its current limitations are and what is needed for it to be successful.

- Maximize the impact of autonomous testing by leveraging it as an enabler of a systematic approach to achieve the quality goals of business and development. Focus on key business value enablement and determine where it can help with revenue, cost and risk management.

- Familiarize yourself with advanced analytics and ML. Invest in augmented analytics tools that employ ML algorithms to mine existing data for current and future projects.

- Allocate ownership and appoint staff with the required skills such as data analytics by identifying the required roles, technologies and practices.

- Select tools that best match available skills and development style by assessing application profiles and different teams’ needs.

**Sample Vendors:**
ACCELQ; Applitools; Avo Automation; Diffblue; Functionize; mabl; ProdPerfect; test.ai; testRigor

# Resources & interesting sources

https://medium.com/appdiff/test-autonomy-levels-7de7967d030e

https://www.gartner.com/doc/reprints?id=1-25Z5AK9P&ct=210506&st=sb

https://www.pnsqc.org/wp-content/uploads/2018/09/38-Santiago-AI-Driven-Test-Generation.pdf

https://sersc.org/journals/index.php/IJFGCN/article/view/5815/3604

https://medium.com/appdiff/test-autonomy-levels-7de7967d030e

https://www.coursera.org/learn/machine-learning

https://testautomationu.applitools.com/testing-machine-learning-models/

https://smartbear.com/resources/ebooks/six-stages-from-manual-to-autonomous-testing/
