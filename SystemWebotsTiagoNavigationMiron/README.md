# SystemWebotsTiagoNavigationMiron

![Architecture](model/SystemWebotsTiagoNavigationMironComponentArchitecture.jpg)

This system is built with Components from the Servicerobotics-Ulm repository, forked and with some bug fixes in [ComponenRepository](https://github.com/MiRON-project/ComponentRepository.git), and the AROSYS ITP, also forked [AROSYSComponents](https://github.com/MiRON-project/AROSYS-Components.git). 

It is based on the [SystemTiagoNavigation](https://github.com/MiRON-project/AROSYS-Systems/tree/master/SystemWebotsTiagoNavigation) system, but incorporates significant changes for managing the skill within the architecture.

Servicerobotics-Ulm Components:
* ComponentTCLSequencer
* ComponentKB
* SmartCdlServer
* SmartMapperGridMap
* SmartPlannerBreadthFirstSearch
* SmartAmcl

AROSYS Components
* ComponentWebots

MIRON Components
* ComponentWebotsRobot
* ComponentWebotsPersonRecognition

MIRON Behavior:
* BehaviorNavigationScenario

MIRON Data:
* MOOD2Be (Executor)
* bundles/ModelRepository/ABR (skills and test.xml with tree)
* ZMQServer (not integrated yet)
