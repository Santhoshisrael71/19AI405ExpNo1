<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Santhosh P</h3>
<h3>Register Number: 212224220088/Staff Id: TSML006</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

## PROGRAM 
```
import random

# Initialize rooms and patient temperatures
rooms = {
    "Room 1": random.uniform(97, 102),
    "Room 2": random.uniform(97, 102)
}

current_room = "Room 1"
performance = 0

print("Initial Patient Temperatures:")
for room, temp in rooms.items():
    print(room, ":", round(temp, 2), "°F")

print("\nAgent Starting Location:", current_room)

# Function to treat patient
def treat_patient(room):
    global performance
    temperature = rooms[room]

    print("\nChecking", room)
    print("Patient Temperature:", round(temperature, 2), "°F")

    if temperature > 98.5:
        print("Patient is unhealthy. Prescribing medicine...")
        performance += 1
        rooms[room] = 98.0  # After treatment
        print("Patient treated successfully.")
    else:
        print("Patient is healthy. No treatment needed.")

# Agent checks first room
treat_patient(current_room)

# Move to second room
print("\nMoving to another room...")
performance -= 1

current_room = "Room 2"
treat_patient(current_room)

# Final Performance
print("\nFinal Performance Score:", performance)

```
## OUTPUT
<img width="626" height="518" alt="image" src="https://github.com/user-attachments/assets/7f4e8a75-cf47-42a8-9be9-36cc922c9428" />

## RESULT
Thus the Developing AI Agent with PEAS Description was implemented using python programming.

