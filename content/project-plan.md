# Project plan

>>**Clone this repo and document your specific choice here.**

## Best Practices 

- Validate RAT's before you start the project 
- Create in short increments and optimize in short iterations
- Include all stakeholders in all phases
- Optimize only what can be measured
- Collaborate using the agile board
- Communicate
- Peer review
- Automate
- Monitor

## Development Phases

Alle new systems are built in phases. In agile project these phases are done incrementally. Only trivial systems or experienced teams don't need a functional or technical design.

### 1. Requirements engineering and RAT's

Requirements describe, using human language, prototypes and sketches, the functionality and non-functionality of a
system concise enough to be used for system validation and acceptance testing.
This stages is done in collaboration with all stake-holder.

#### RAT's

RAT or Riskiest Assumptions Tests using POC's en prototypes are done to reduce uncertainty to an acceptable level.
The objective in this phase is to fail as cheap and soon as possible. If that fails, the project can continue.

### 2. Functional design and architecture

Functional design creates the desired modularity of the system based on functional dependencies and architecture. It
formally describes the behaviour of it using pseudocoding, UML, BPML etc.
A functional design needs to be complete to be useful.

#### Architecture

The architecture defines the most basic patterns of the application, often based on corporate standards. Architecture has many aspects:
- Security
- Integration
- Application

### 3. Technical design

Technical design translates the functional design into codeable constructions, using the appropriate technical
standards, architectures and patterns.
The design is formulated in UML.
Technical design is not meant to be complete, just complete enough to manage coding complexity.

### 4. Implementation (coding)

Coding creates an instantiable image of the software application.
De code defines the state space (type) of the application. The user-interactions define its actual state (instance).

## Product Stages

### Proof-of-concept

A POC is an assumption (in)validator. Often multiple POC’s are needed.

### Prototype

A prototype is a functionality / UX demonstrator, without the full set of non-functionals and in one-off fashion.

### Minimum Viable Product

Minimum Viable Product is that version of the product that enables a full turn of the Build-Measure-Learn loop
with a minimum amount of effort and the least amount of development time.
It's also a test run for the entire DevOps setup.

### Beta release

The Beta is a production-release which can be tested in a larger, tolerant user group to iron out the last flaws.

## Architectures

### 
