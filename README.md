# Autonomous testing - drivers

> By the end of 2025, 30% of organizations will have implemented an autonomous automation strategy and will outperform competitors in quality and customer experience satisfaction metrics.

Source: [Innovation Insight for Autonomous Testing, Gartner](https://www.gartner.com/doc/3992325)

> Despite the acknowledged benefits of automation, less than half of QA professionals are automating more than 50% of their tests. Graphical user interface **(GUI) tests are notoriously difficult to automate, and as a result, the majority of GUI test cases are still conducted manually.** For QA teams responsible for GUI testing, 42% will run their tests via a combination of both manual and automated testing, with 31% running their tests solely via manual execution.

Source: [Six Stages from Manual to Autonomous Testing, SmartBear ](https://smartbear.com/resources/ebooks/six-stages-from-manual-to-autonomous-testing/)

> Implementation of an autonomous testing tool can help your company in three ways:
>
> - Zero / Minimal human dependence for testing: 40-70% incremental savings of QA efforts
> - 4x faster QA cycle time with 100% test and automation coverage
> - Zero Critical Defect Slippage to production and improved release confidence

Source: [Autonomous Software Testing, Hexaware Technologies Limited](https://hexaware.com/services/digital-assurance/autonomous-software-testing/)

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

- Features: Scripting tools / IDEs, recorders, code inspectors
- Examples: Selenium + Java/Python/JavaScript, Cypress.io, Playwright, Chrome DevTools

### 2. Partially automated testing

_*The human enhances test automation scripts*, either coded or codeless, that were created using recording facilities, log file analysis, customer journey analysis or model-based testing (business process model, application model, etc.)._

- Features: Record & play tools, xDD?(TDD, BDD, etc.) - _only in case_ it is provided into testing as input created as output from analytical activity.
- Examples: Selenium IDE, Dredd

### 3. Integrated automated testing

_The human defines the high-level intent of a test case for a particular business process (e.g., by visually defining the business process workflow). Tests are then executed based on this definition._

### 4. Intelligent automated testing

_Intelligent automated testing involves the use of test bots to perform exploratory testing and generate and execute test scenarios independently. These tests are designed to actively run through fallback scenarios and update test scripts as needed, such as when a test case fails due to an updated component of the application under test._

While test bots used as web crawlers can perform thorough testing of a web application by exploring its navigational structure, it can be difficult to turn their crawling trace into a minimal test suite that still achieves the same level of coverage. This is because test cases generated from a crawling trace may be dependent on each other and may fail when executed in isolation, and they may also be redundant, covering the same targets multiple times.

See also [Dependency-Aware Web Test Generation](resources/2020-Biagiola-ICST2020-Dependency-Aware-Web-Test-Generation.pdf)

### 5. Autonomous testing

_No human assistance is needed and machines can evaluate an application, decide what, when, where and how testing should be performed, and summarize the results to provide a release/no-release decision based on test results_

# Machine Learning and Testing

> By 2025, 70% of enterprises will have implemented an active use of AI-augmented testing, up from 5% in 2021.

> By 2025, organizations that ignore the opportunity to utilize AI-augmented testing will spend twiceas much effort on testing and defect remediation compared with their competitors that takeadvantage of AI.

Source: [Market Guide for AI-Augmented Software Testing Tools, 2021](resources/2021-Market-Guide-for-AI-Augmented-Software-Testing-Tools.pdf)

> By 2027, 80% of enterprises will have integrated artificial intelligence (AI)-augmented testing tools into their software engineering toolchain, which is a significant increase from 10% in 2022.

Source: [Market Guide for AI-Augmented Software Testing Tools, 2022](resources/2022-Market-Guide-for-AI-Augmented-Software-Testing-Tools.pdf)

Examples of application of Machine Learning in testing:

- NLP and natural language generation research may map to test case generation.
- Game theory and reinforcement learning may map well to the problem of discovering a system and hunting for bugs.

Other

- Object Recognition
- Perceiving Application State
- Execution sequence generation: see NPL sequence-to-sequence problem (https://en.wikipedia.org/wiki/Seq2seq) ... to generate more logical sequences of actions
- Test flow generation: see

## Reinforcement learning

Execution flow might be built based on the algorithm used games to train a bot to play games https://www.youtube.com/watch?v=t1A3NTttvBA

**Reinforcement learning with TensorFlow**

- https://github.com/GoogleCloudPlatform/tensorflow-without-a-phd
- https://github.com/tensorflow/agents/blob/master/docs/tutorials/1_dqn_tutorial.ipynb
- https://storage.googleapis.com/deepmind-media/dqn/DQNNaturePaper.pdf

## Natural Language Processing (NLP) Based Test Automation

Test script development is a tedious process and updating and maintaining them for every change does not come easy. A lot of time is spent on the initial test script authoring.

Though there are other approaches like the Record and Playback method to automation testing, NLP-based testing is not only intuitively easy but reliable.

With NLP, you can still write your own tests but without the complexities of traditional test automation.

Natural language processing is an artificial intelligence specialty by which machines can identify, interpret, and generate human language. NLP arises from the intersection of many disciplines such as computational linguistics and computer science. NLP aims to build machines that can approximate human language comprehension.

sources:

- https://testsigma.com/blog/natural-language-processing-nlp-based-test-automation/
- https://www.functionize.com/blog/how-nlp-will-drive-the-future-of-software-testing/

**NPL with TensorFlow**

https://www.youtube.com/playlist?list=PLQY2H8rRoyvzDbLUZkbudP-MFQZwNmU4S

words > sentences
actions > scenarios

sentiment > failure level?

sequence length:

- simple solution: [padding](https://youtu.be/r9QjkdSJZ2g), or [here](https://colab.research.google.com/drive/1qDCHeK-tym0ecwAeHhz_bWeZhjOPZPj7)
- advanced approach: [ragged tensor](https://www.tensorflow.org/guide/ragged_tensor)

# Autonomous Testing Tools

[List of tools](/TOOLS.md) trying to achieve fully autonomous testing or at least so-called autonomous assistance.

# Current market state

## Market size and predictions

![Market size and predictions](/images/Market-size-and-predictions.png)

> The testing tool market (excluding mainframe testing) segment is $2,319.7 million, which is expected to increase at a 7.5% compound annual growth rate (CAGR) in constant currency through 2026.
> There is strong interest in the AI- augmented testing tools market from investors — the vendors in this research have received private investments of more than $300 million since 2020.

Source: [Market Guide for AI-Augmented Software Testing Tools, 2022](resources/2022-Market-Guide-for-AI-Augmented-Software-Testing-Tools.pdf)

## Hype Cycle for Agile and DevOps, 2022 - Autonomous Testing

Full report [here](resources/Hype-Cycle-for-Agile-and-DevOps-2022.pdf)

![Hype Cycle for Agile and DevOps, 2022](/images/Hype-Cycle-for-Agile-and-DevOps-2022.png)

[Gartner Hype Cycles, Explained](https://youtu.be/jB1RDz9jaj0)

## Hype Cycle for AI in Software Engineering, 2024

Full report [here](resources/Hype-Cycle-for-AI-in-SW-Engineering-2024.pdf)

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

## The Forrester Wave™: Continuous Automation Testing Platforms, Q4 2022

> All testers must be enabled to easily combine different types of testing and automate end-to-end.

TuringBots, coined by Forrester, are AI-powered software that can help software developers and entire development teams plan, design, build, test, and deploy application code.

TuringBots are featured in Forrester’s top 10 technology trends of 2022 because we believe that they are giving birth to a new generation of software development.

Full report [here](resources/The-Forrester-Wave_Continuous-Automation-Testing-Platforms-Q4-2022.pdf)

# Resources & interesting sources

- [Test Autonomy Levels, Jason Arbon](https://medium.com/appdiff/test-autonomy-levels-7de7967d030e)
- [Innovation Insight for Autonomous Testing, Gartner](https://www.gartner.com/doc/3992325)
- [Supervised Machine Learning: Regression and Classification, Coursera](https://www.coursera.org/learn/machine-learning)
- [Intro to Testing Machine Learning Models, Applitools](https://testautomationu.applitools.com/testing-machine-learning-models/)
- [Six Stages from Manual to Autonomous Testing, SmartBear](https://smartbear.com/resources/ebooks/six-stages-from-manual-to-autonomous-testing/)

## Video ideas

- [(EN) Autonomous Visual Regression Testing | Marcel Veselka, Jan Beránek a Ondřej Winter](https://youtu.be/R-S94tYmH04)
- [(EN) Autonomous Testing and the Future of Software Development](https://youtu.be/Q8s8ENQLWfA)
- [(EN) Test Automation’s Next Great Wave: Autonomous Testing](https://applitools.com/event/opening-keynote-test-automations-next-great-wave-autonomous-testing/)
- [(CZ) Autonomní testování│Ondřej Winter a Jan Beránek](https://youtu.be/EBtuOj9hdKc)
