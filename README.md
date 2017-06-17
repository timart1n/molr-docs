# Concepts and Vision
The purpose of this document is mainly to lay out a common vision and concepts which are implemented (or shall be implemented) in the molr project.

## Purpose
Molr shall make it simple to create modular systems, where it has to be possible to exchange (deploy) parts of them at runtime (This parts are called *mole*s in the following). While this requirement can be seen common to standard microservice architectures, there are several key features that molr shall provide in addition:

* The moles are related to one mother-system, which typically is a service for a dedicated purpose (If we think of examples in the cern acclerator environment, then the mother-system could e.g. the sequencer and the moles would be sequencer agents). The moles provide certain snippets of functionality (denoted as *missions* in the following) to the mother system.
* The moles provide functionality to execute the missions in different modes. At a minimum, we see: "run them", "step through them".
* Ideally, the mole can be deployed through the mother system, so tha only one entry point is required and coupling to other technologies can be minimized (and/or encapsulated)

The following picture shows an overview of an example system using molr:
![Molr Overview](molr-overview.PNG)

