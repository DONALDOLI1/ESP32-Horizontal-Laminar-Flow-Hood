<div align="center">

# ESP32 Horizontal Laminar Flow Hood

**OLITECH · Système de commande embarqué pour hotte à flux laminaire**

![Project stage](https://img.shields.io/badge/Project-Manufactured%20%26%20tested-success)
![Microcontroller](https://img.shields.io/badge/MCU-ESP32-blue)
![CAD](https://img.shields.io/badge/CAD-KiCad-blue)
![PCB fabrication](https://img.shields.io/badge/PCB-Photochemical%20process-orange)
![Languages](https://img.shields.io/badge/README-FR%20%7C%20EN-informational)

*Design, PCB manufacturing and embedded automation of a horizontal laminar flow hood.*

</div>

---

**Marque / Brand:** OLITECH  
**Concepteur / Designer:** OLI OLI DONALD  
**Pays / Country:** Cameroun / Cameroon  
**Microcontrôleur / Microcontroller:** ESP32  
**Logiciel de conception / Design software:** KiCad  
**Fabrication PCB / PCB manufacturing:** Méthode photochimique / Photochemical process

## Table des matières / Table of contents

- [🇫🇷 Français](#-français)
  - [Présentation](#présentation)
  - [Objectifs du projet](#objectifs-du-projet)
  - [Architecture fonctionnelle](#architecture-fonctionnelle)
  - [Conception électronique](#conception-électronique)
  - [Fabrication et assemblage du PCB](#fabrication-et-assemblage-du-pcb)
  - [Galerie du projet](#galerie-du-projet)
  - [Documents techniques](#documents-techniques)
  - [État de réalisation](#état-de-réalisation)
  - [Compétences mobilisées](#compétences-mobilisées)
- [🇬🇧 English](#-english)
  - [Overview](#overview)
  - [Project objectives](#project-objectives)
  - [Functional architecture](#functional-architecture)
  - [Electronic design](#electronic-design)
  - [PCB manufacturing and assembly](#pcb-manufacturing-and-assembly)
  - [Project gallery](#project-gallery)
  - [Technical documentation](#technical-documentation)
  - [Project status](#project-status)
  - [Skills involved](#skills-involved)
- [Contact](#contact)

---

## 🇫🇷 Français

### Présentation

**ESP32 Horizontal Laminar Flow Hood** est un projet de conception et de réalisation d'un système électronique de commande destiné à une hotte à flux laminaire horizontale.

Le système repose sur un microcontrôleur **ESP32**, utilisé comme unité centrale pour gérer plusieurs fonctions de l'équipement : l'éclairage normal, l'éclairage ultraviolet (UV), la ventilation et la surveillance de la pression.

Une carte électronique dédiée a été conçue, fabriquée et assemblée afin de centraliser les circuits de commande et les interfaces nécessaires au fonctionnement du système.

Le projet couvre plusieurs étapes de développement matériel : conception électronique, routage du PCB, fabrication photochimique, implantation des composants, intégration au prototype et essais finaux.

### Objectifs du projet

- Automatiser plusieurs fonctions de la hotte à l'aide d'un ESP32.
- Gérer indépendamment l'éclairage normal et l'éclairage UV.
- Programmer une temporisation pour l'éclairage UV.
- Intégrer une sécurité fondée sur la détection de présence.
- Commander le moteur de ventilation selon deux vitesses.
- Surveiller la pression et signaler les situations nécessitant une intervention de maintenance.
- Concevoir et fabriquer une carte électronique adaptée au système.

### Architecture fonctionnelle

L'ESP32 constitue l'unité centrale de commande. Il reçoit les commandes des boutons-poussoirs et les informations des dispositifs de détection et de surveillance. Il pilote ensuite les équipements à travers les circuits de commande et les relais.

#### Gestion de l'éclairage normal

L'éclairage normal est commandé par un bouton-poussoir dédié. Une action permet de l'activer et une nouvelle action permet de le désactiver.

#### Gestion de l'éclairage ultraviolet (UV)

L'éclairage UV fonctionne selon une temporisation programmée d'environ **3 minutes**, suivie d'un arrêt automatique.

Une sécurité basée sur un capteur de présence permet également d'interrompre immédiatement l'éclairage UV lorsqu'une présence est détectée pendant son fonctionnement.

#### Commande du moteur de ventilation

Le moteur dispose de deux vitesses de fonctionnement. Un bouton-poussoir permet de sélectionner successivement les trois états suivants :

1. Petite vitesse.
2. Grande vitesse.
3. Arrêt du moteur.

#### Surveillance de la pression

Deux seuils sont utilisés pour signaler les besoins de maintenance :

| Seuil | Intervention associée |
|---|---|
| 15 Pa | Maintenance préventive |
| 30 Pa | Maintenance corrective |

Ces valeurs correspondent aux seuils définis pour le système.

### Conception électronique

La carte électronique dédiée a été conçue sous **KiCad**. Elle regroupe les interfaces nécessaires à la commande des équipements et à la gestion des différentes entrées du système.

Les travaux de conception comprennent :

- La réalisation du schéma électronique.
- L'implantation des composants.
- Le routage des pistes du circuit imprimé (PCB).
- La préparation des documents nécessaires à la fabrication.

### Fabrication et assemblage du PCB

La fabrication du circuit imprimé a été réalisée personnellement par **méthode photochimique**.

Les différentes étapes suivies sont les suivantes :

1. **Préparation du typon :** impression du tracé des pistes sur un support transparent.
2. **Insolation :** exposition de la plaque photosensible aux rayons UV à l'aide d'une insoleuse, avec le typon comme masque.
3. **Révélation :** traitement de la plaque avec une solution révélatrice afin de faire apparaître le motif des pistes.
4. **Gravure chimique :** utilisation du perchlorure de fer pour éliminer le cuivre non protégé et former les pistes conductrices.
5. **Perçage :** réalisation des trous destinés aux composants.
6. **Implantation et soudure :** montage des composants électroniques sur la carte.
7. **Vérification et tests :** contrôle de la carte assemblée et réalisation des tests électriques.
8. **Intégration au prototype :** montage de la carte dans la hotte.
9. **Tests finaux :** vérification du fonctionnement global et des différentes fonctions automatisées.

Cette réalisation a permis de mettre en œuvre l'ensemble du processus de développement d'un circuit imprimé, depuis sa conception numérique jusqu'à sa fabrication et son intégration dans un prototype.

### Galerie du projet

Les vues 3D de la carte conçue sous KiCad ainsi que les photographies des différentes étapes de fabrication et d'intégration seront présentées dans le dossier [images/](images/).

### Documents techniques

Les documents techniques seront regroupés dans le dossier [documents/](documents/).

| Document | Description |
|---|---|
| Côté composants (PDF) | Implantation des composants électroniques |
| Typon (PDF) | Tracé utilisé pour la fabrication photochimique |
| Schéma électronique (PDF) | Schéma électrique de la carte |

### État de réalisation

| Étape | État |
|---|---|
| Conception électronique | Réalisée |
| Conception et routage du PCB | Réalisés |
| Fabrication photochimique | Réalisée |
| Perçage et implantation | Réalisés |
| Assemblage de la carte | Réalisé |
| Intégration au prototype | Réalisée |
| Tests finaux | Réalisés |

### Compétences mobilisées

- Programmation de microcontrôleurs ESP32.
- Électronique de commande et interfaces de puissance.
- Automatisation et gestion des séquences de fonctionnement.
- Intégration de capteurs et d'actionneurs.
- Conception de circuits imprimés sous KiCad.
- Fabrication de PCB par méthode photochimique.
- Assemblage, intégration et tests de prototypes électroniques.

---

## 🇬🇧 English

### Overview

**ESP32 Horizontal Laminar Flow Hood** is a project involving the design and implementation of an electronic control system for a horizontal laminar flow hood.

The system is based on an **ESP32 microcontroller**, which manages several equipment functions, including normal lighting, ultraviolet (UV) lighting, ventilation and pressure monitoring.

A dedicated electronic board was designed, manufactured and assembled to centralize the control circuits and interfaces required by the system.

The project covers the complete hardware development process, from electronic design and PCB routing to photochemical manufacturing, component assembly, prototype integration and final testing.

### Project objectives

- Automate several hood functions using an ESP32.
- Independently control normal and UV lighting.
- Implement timed UV operation.
- Integrate a presence-based safety mechanism.
- Control the ventilation motor at two different speeds.
- Monitor pressure and identify maintenance conditions.
- Design and manufacture a dedicated electronic control board.

### Functional architecture

The ESP32 acts as the main control unit. It receives push-button commands and information from the detection and monitoring devices, then controls the equipment through relay and control circuits.

#### Normal lighting

Normal lighting is controlled using a dedicated push button. One press switches the lighting on, and another press switches it off.

#### Ultraviolet (UV) lighting

UV lighting operates with a programmed duration of approximately **3 minutes**, followed by automatic shutdown.

A presence sensor provides an additional safety function by immediately switching off the UV lamp whenever presence is detected during operation.

#### Ventilation motor control

The motor has two operating speeds. A push button cycles through three operating states:

1. Low speed.
2. High speed.
3. Motor stop.

#### Pressure monitoring

Two pressure thresholds are used to indicate maintenance requirements:

| Threshold | Associated intervention |
|---|---|
| 15 Pa | Preventive maintenance |
| 30 Pa | Corrective maintenance |

These values correspond to the thresholds defined for the system.

### Electronic design

The dedicated electronic board was designed using **KiCad**. It integrates the interfaces required to control the equipment and manage the system inputs.

The design work includes:

- Electronic schematic development.
- Component placement.
- PCB track routing.
- Preparation of manufacturing documentation.

### PCB manufacturing and assembly

The printed circuit board was personally manufactured using the **photochemical process**.

The manufacturing and assembly stages were:

1. **PCB artwork preparation:** printing the track layout onto a transparent film.
2. **UV exposure:** exposing the photosensitive board using a UV exposure unit and the printed artwork.
3. **Development:** applying a developer solution to reveal the circuit pattern.
4. **Chemical etching:** using ferric chloride to remove the unprotected copper and form the conductive tracks.
5. **Drilling:** making the holes required for component mounting.
6. **Component placement and soldering:** assembling the electronic components onto the board.
7. **Inspection and testing:** checking the assembled board and carrying out electrical tests.
8. **Prototype integration:** installing the board into the hood prototype.
9. **Final testing:** verifying the overall system and its automated functions.

This process provided practical experience in the complete PCB development workflow, from digital design to physical manufacturing and prototype integration.

### Project gallery

The KiCad 3D board views, manufacturing photographs and prototype integration pictures will be presented in the [images/](images/) directory.

### Technical documentation

Technical documents will be stored in the [documents/](documents/) directory.

| Document | Description |
|---|---|
| Component layout (PDF) | Electronic component placement |
| PCB artwork (PDF) | Artwork used for photochemical manufacturing |
| Electronic schematic (PDF) | Electrical schematic of the board |

### Project status

| Stage | Status |
|---|---|
| Electronic design | Completed |
| PCB design and routing | Completed |
| Photochemical manufacturing | Completed |
| Drilling and component placement | Completed |
| Board assembly | Completed |
| Prototype integration | Completed |
| Final testing | Completed |

### Skills involved

- ESP32 microcontroller programming.
- Electronic control and power interfaces.
- Automation and operating-sequence management.
- Sensor and actuator integration.
- PCB design using KiCad.
- Photochemical PCB manufacturing.
- Electronic prototype assembly, integration and testing.

---

## Contact

**OLI OLI DONALD · OLITECH**  
Cameroon

*OLITECH — Learning · Designing · Building.*
