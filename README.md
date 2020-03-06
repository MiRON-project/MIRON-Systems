# MIRON-Systems
Systems developed in MiRon Project

# SystemWebotsTiagoNavigationMiron

This system is built with Components from the Servicerobotics-Ulm repository, forked and with some bug fixes in [ComponenRepository](https://github.com/MiRON-project/ComponentRepository.git), and the AROSYS ITP, also forked [AROSYSComponents](https://github.com/MiRON-project/AROSYS-Components.git). 

It is based on the [SystemTiagoNavigation](https://github.com/MiRON-project/AROSYS-Systems/tree/master/SystemWebotsTiagoNavigation) system, but incorporates significant changes for managing the skill within the architecture.
Modified Components and Behaviors:
* ComponentSkillInterface: The SkillExecutionTask.cc module has been modified for capturing the skill from the ZMQ server and annotate it on the ComponentKB. After updating a skill, the component will poll the ComponentKB for obtaining the associated response (i.e. skill_result).
* BehaviorNavigationScenario.smartTcl: Minor changes for updating a NIL skill and skill_result on the ComponentKB.
* startUp.smartTcl: Relevant changes for polling the ComponentKB and capturing the new skills and manage them, writing on the ComponentKB the resulting skill_results. Currently, only three skills are considered: ACTIVATELOCALIZATION, APPROACHLOCATION, and DEACTIVATELOCALIZATION.

Servicerobotics-Ulm Components:
* ComponentTCLSequencer
* ComponentKB
* SmartCdlServer
* SmartMapperGridMap
* SmartPlannerBreadthFirstSearch
* SmartAmcl

AROSYS Components
* ComponentWebots
* ComponentWebotsLidar
* ComponentWebotsTIAGo
