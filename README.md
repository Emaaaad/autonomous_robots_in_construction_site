# Construction Monitoring with PDDL

This repository contains a PDDL (Planning Domain Definition Language) project for monitoring construction sites using robots equipped with various sensors. The project involves defining a domain and a problem where robots move around a construction site, collect data using different sensors, process this data, and update a Building Information Model (BIM).

## Table of Contents

- [Introduction](#introduction)
- [Domain Description](#domain-description)
- [Problem Description](#problem-description)
- [Setup](#setup)
- [Usage](#usage)
- [File Structure](#file-structure)

## Introduction

In this project, we use PDDL to model a construction monitoring scenario. Robots move between different locations on a construction site, use sensors to collect data, process this data, and update the BIM. The project demonstrates the use of PDDL to define actions, predicates, and goals for automated planning.

## Domain Description

The domain defines the types, predicates, and actions involved in the construction monitoring scenario:

- **Types**: Robot, Location, Configuration, Sensor, Analysis
- **Predicates**: 
  - `at`: Location of the robot
  - `connected`: Connectivity between locations
  - `stable`: Stability status of the robot
  - `inspected`: Inspection status of a location
  - `manipulator_extended`, `manipulator_retracted`, `manipulator_positioned`: Manipulator states
  - `sensors_on`, `sensors_off`: Sensor states
  - `data_collected`, `data_transferred`, `data_processed_onboard`: Data collection and processing states
  - `structural_integrity_analyzed`, `worker_activity_analyzed`, `temperature_variation_analyzed`: Analysis statuses
  - `initial_inspection_done`, `inspection_done_twice`: Inspection statuses
  - `data_formatted`, `bim_updated`, `session_closed`: Reporting statuses

## Problem Description

The problem file specifies the initial state and goals for the construction monitoring scenario:

- **Objects**: Robot, locations, configurations, and sensors
- **Initial State**: The robot's starting location, connectivity between locations, initial states of the manipulator and sensors, and initial inspection counts
- **Goals**: Complete inspections, analyze data, process data, update BIM, and return to the starting location

## Setup

To work with this project, you need a PDDL solver that supports BFWS. Here are the steps to set up the project:

 Clone the repository:
   ```sh
   git clone https://github.com/Emaaaad/autonomous_robots_in_construction_site.git
   ```
## Usage 

To run the planner with the provided PDDL files using the Planning.Domains editor:

Go to the [Planning editor](https://editor.planning.domains/#) .

Create a new project and upload the `domain.pddl` (domain file) and `problem.pddl` (problem file).

Select the BFWS planner from the available planners.

Run the planner to solve the problem.

## File Structure

`domain.pddl` : The PDDL domain file defining the construction monitoring domain.

`problem.pddl` : The PDDL problem file specifying the initial state and goals for the construction monitoring scenario.
