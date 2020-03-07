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

## DevOps
During development of the proof of concept, a single Git repository will be used to for all code bases. This repository is, of course, located [here](https://github.com/CompFigurationLtd/CompFiguration-Backend). The primary reason for this is to reduce development costs, however, this does align with a key design choice highlighted further into this document. 

### Versioning
This code base will make best efforts to adhere to [SemVer 2.0.0](https://semver.org/).

### Testing
Common practice with modern web-based applications is to automate testing and the integration of new code into the existing code-base. This is the practice of Continuous Integration (CI). This repository will use [GitHub Actions](https://github.com/features/actions) for CI. 

As the application is written in Node.JS and is highly asynchronous, we will utilise the popular [Mocha](https://mochajs.org/) for test automation. Further to this, good practice is to implement a technique such as Test Driven or Behaviour Driven Development (TDD/BDD); this project will utilise another popular framework, [chai](https://www.chaijs.com/), to aid this.

### Make sure tests workflow doesn't run!

