# CompFiguration REST API System Design
| Author | Adam Mitchell |
|--|--|
| Version | 0.1.0 |

## What's covered in this document?
This document will provide a brief overview of the system architecture for the CompFiguration proof of concept web backend application and highlight and explain key design decisions. Various high-level topics will be covered; including DevOps, framework choices, database configuration and a holistic system design diagram. 

This document will not cover the code structure for individual elements of the system, any specific information regarding system details such as IP addresses and login details, nor provide contribution guidelines. 

The R&D process is inherently iterative and, as such, the current state of the system may not always match that of the system design diagram. The developers shall endeavour to ensure that the system design document remains aligned with the current state of the system, however, this is not always possible. An accurate record of the current state of the system can be obtained through a list of Git commits. 

The version number of the system design will be kept in line with that of versions of the application released onto the Master branch of the repository. For example, when version 0.2.0 of the application is released, the system design document will be aligned with this version of the system. 

## Holistic System Design
Some stuff here, including a nice shiny diagram

## FeathersJS
[Feathers](https://github.com/feathersjs/feathers) is an extremely popular backend web framework for Node.js specifically designed to be lightweight and support real-time and Represential State Transfer (REST) applications. It's open-source and has a multitude of extensions for database integration, testing and supports a number of popular frontend frameworks. Feathers removes the need to spend hours on a 'Hello, World' just to get up and running with a handy Command Line Interface (CLI) tool to generate a lot of the boilerplate code.

## Versioning
This code-base will make best efforts to adhere to [SemVer 2.0.0](https://semver.org/).

## Testing Strategy and Frameworks
Common practice with modern web-based applications is to automate testing and the integration of new code into the existing code-base. This is the practice of Continuous Integration (CI). This repository will use [GitHub Actions](https://github.com/features/actions) for CI. 

As the application is written in Node.JS and is highly asynchronous, we will utilise the popular [Mocha](https://mochajs.org/) for test automation. Further to this, good practice is to implement a technique such as Test Driven or Behaviour Driven Development (TDD/BDD); this project will utilise another popular framework, [chai](https://www.chaijs.com/), to aid this.

Lastly, tests are great - but you need to be sure that you're actually testing your code-base and any libraries to facilitate this. [Istanbul](https://istanbul.js.org/) is one such library and integrates extremely easily with Mocha to provide code coverage reports. Whilst in the proof-of-concept stage a very acceptable code coverage percentage is between 80 and 90%.  
