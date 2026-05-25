## ExpNo 1 :Developing AI Agent with PEAS Description
## Name : Nithish R
## Reg no : 212223040135
## AIM:
To find the PEAS description for the given AI problem and develop an AI agent.

## Theory
## Medicine prescribing agent:
Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.

## PEAS DESCRIPTION:
<img width="831" height="162" alt="Screenshot 2025-09-17 112409" src="https://github.com/user-attachments/assets/a4934469-d1d2-4107-b972-00985ccbde9d" />

## DESIGN STEPS
## STEP 1:Identifying the input:
Temperature from patients, Location.

## STEP 2:Identifying the output:
Prescribe medicine if the patient in a random has a fever.

## STEP 3:Developing the PEAS description:
PEAS description is developed by the performance, environment, actuators, and sensors in an agent.

## STEP 4:Implementing the AI agent:
Treat unhealthy patients in each room. And check for the unhealthy patients in random room

## STEP 5:
Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented

## Program :
~~~import random

class VacuumCleanerAgent:
    def __init__(self): 
        self.location = "A" 
        self.dirt_status = {
            "A": True,
            "B": True,
        }  
        self.performance = 0

    def move_left(self): 
        if self.location == "B":
            self.location = "A"

    def move_right(self): 
        if self.location == "A":
            self.location = "B"

    def suck_dirt(self): 
        if self.dirt_status[self.location]:
            self.dirt_status[self.location] = False
            print(f"Sucked dirt in location {self.location}")

    def do_nothing(self): 
        pass

    def perform_action(self, action):   action
        if action == "left":
            self.performance = self.performance - 1
            self.move_left()
        elif action == "right":
            self.performance = self.performance - 1
            self.move_right()
        elif action == "suck":
            self.performance = self.performance + 10
            self.suck_dirt()
        elif action == "nothing":
            self.do_nothing()
        else:
            print("Invalid action")

    def print_status(self):  # Print the current status of the agent
        print(f"Location: {self.location}, Dirt Status: {self.dirt_status}, ", end="")
        print(f"Perfomance Measure: {self.performance}")

agent = VacuumCleanerAgent()
agent.perform_action("left")
agent.print_status()
agent.perform_action("suck")
agent.print_status()
agent.perform_action("right")
agent.print_status()
agent.perform_action("suck")
agent.print_status()
agent.perform_action("nothing")
agent.print_status()
~~~

## Output :
<img width="816" height="212" alt="image" src="https://github.com/user-attachments/assets/31a1b663-3976-4d11-981b-aa784a0aaa21" />

## Result :
Thus the Developing AI Agent with PEAS Description was implemented using python programming.
