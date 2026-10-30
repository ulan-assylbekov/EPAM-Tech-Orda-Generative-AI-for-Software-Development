# Generative AI Applications: Examples from My Practice

This report describes two examples of how I use generative AI in my work: testing the Oysyn mobile application and researching methods for detecting AI-generated text. In both cases, I use OpenAI Codex as an assistant, while I remain responsible for defining tasks, evaluating results, and deciding what to do next.

## 1. Testing a Mobile Application with Generative AI

I use OpenAI Codex to help verify the results of my development work on Oysyn, a Flutter mobile application I developed for the company. I ask the agent to help check the interface and individual features, analyze code, and create automated tests. One concrete example is checking the interface on small mobile screens: the login and PIN setup forms, bottom navigation, document cards, and report screen must fit within the available space, and text must not overlap buttons. The project includes Flutter tests that reproduce specific screen dimensions for these checks. The business value is less time spent repeating checks after changes and a lower risk of releasing an application with interface problems that affect usability or functionality.

The technical challenge is that a passing automated test does not guarantee correct behavior on a physical device. The on-screen keyboard, system navigation bars, network conditions, and server responses can all affect the result. The AI may also misunderstand the expected behavior or overlook an important scenario, while a test based on incorrect logic may reinforce an existing error. I therefore treat Codex as a testing assistant: I define the expected results and evaluate the proposed checks. Comprehensive application testing requires supplementing automated tests with checks on physical devices.

### Implementation Used

- [OpenAI Codex](https://developers.openai.com/codex/) — An AI agent I use to analyze the project and help create and run application checks.

## 2. An AI Agent for Researching AI-Generated Text Detection Methods

I use OpenAI Codex as a research agent to find and organize information about methods and technologies for distinguishing human-written text from AI-generated text. I define the initial research direction, and the agent helps find scientific publications, descriptions of approaches, and existing solutions in publicly available sources, consolidate the information, and compare methods. I then study the collected materials myself, refine the conclusions, adjust my requests, and set the direction for further research. This is an iterative process: the findings help me formulate new questions and explore promising approaches in greater depth. The practical value is a substantial reduction in the time I spend searching for information, conducting an initial review, and consolidating findings, allowing me to focus more on evaluating technologies and their potential application in Oysyn.

The technical challenges involve source reliability and the comparability of findings: detection methods may be evaluated using different languages, text types, and datasets, so reported performance cannot be compared without examining the experimental conditions. The AI agent may overlook an important publication, misrepresent a method, or draw an overly confident conclusion. I therefore verify references and key claims against the original materials, make corrections, and guide subsequent research. I pay particular attention to technological limitations, including false positives in which human-written text is incorrectly classified as AI-generated. The agent helps collect and structure information, while I remain responsible for evaluating methods and choosing the next research direction.

### Implementation Used

- [OpenAI Codex](https://developers.openai.com/codex/) — An AI agent I use to find, organize, and conduct an initial analysis of information about AI-generated text detection methods and technologies.
