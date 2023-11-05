# CSci 144 - Intelligent Systems | Course Work 3

## Exhaust Fan Controller using FLC

### Introduction
The Exhaust Fan Controller is a system designed to control the speed of an exhaust fan based on input variables such as temperature and air quality. The goal is to regulate the fan speed to maintain a comfortable and healthy indoor environment. This system uses fuzzy logic to make intelligent decisions regarding the fan speed.

### Prerequisites
Before running the code, make sure you have the following Python libraries installed:

- NumPy
- scikit-fuzzy (skfuzzy)
- Matplotlib

You can install these libraries using pip if they are not already installed:

```
pip install numpy scikit-fuzzy matplotlib
```

### Code Description
The Python code defines a fuzzy logic-based exhaust fan controller using the scikit-fuzzy library. The code consists of the following components:
1. ***Universe of Discourse***: Defines the range of values for the input and output variables:
    - temperature: Ranges from 0°C to 55°C.
    - air_quality: Ranges from 0% to 100%.
    - fan_speed: Ranges from 0 to 3.0.

2. ***Membership Functions***: Defines the membership functions for the input and output variables, which represent the degree of membership to fuzzy sets. Fuzzy sets are defined for temperature (Very Cold, Cold, Medium, Hot, Very Hot), air quality (Low, Moderate, High), and fan speed (Off, Low, Medium, High).

3. ***Plotting Membership Functions***: Visualizes the membership functions for temperature, air quality, and fan speed using Matplotlib.

4. ***Fuzzy Rules***: Defines a set of fuzzy rules that determine the fan speed based on input conditions. Rules are defined for all possible combinations of temperature and air quality.
The following table presents the fuzzy rules that determine the fan speed based on temperature and air quality:

<table>
  <tr>
    <th>Temperature / Air Quality</th>
    <th>very cold</th>
    <th>cold</th>
    <th>medium</th>
    <th>hot</th>
    <th>very hot</th>
  </tr>
  <tr>
    <th>low</th>
    <td>low</td>
    <td>medium</td>
    <td>high</td>
    <td>high</td>
    <td>high</td>
  </tr>
  <tr>
    <th>moderate</th>
    <td>low</td>
    <td>low</td>
    <td>medium</td>
    <td>high</td>
    <td>high</td>
  </tr>
  <tr>
    <th>high</th>
    <td>off</td>
    <td>off</td>
    <td>medium</td>
    <td>medium</td>
    <td>high</td>
  </tr>
</table>

5. ***Control System Creation***: Creates a fuzzy control system using the defined rules.

6. ***Control System Simulation***: Sets input values for temperature and air quality and computes the fan speed using the control system.

7. ***Output and Visualization***: Prints the calculated fan speed and plots the output membership function for fan speed.

### Running the Code
To run the code, simply execute the following command in the terminal:

```
python exhaust_fan_controller.py
```

### Usage
1. Define the universe of discourse, membership functions, and rules according to your specific requirements.
2. Create a Control System and Control System Simulation.
3. Set input values for temperature and air quality using fan_sim.input.
4. Compute the fan speed using fan_sim.compute().
5. Print the calculated fan speed and visualize it.

### Example
In the provided code, input values of temperature and air quality are set to 28°C and 100%, respectively, and the calculated fan speed is printed and visualized.

### Output
The code will print the fan speed and display a graph showing the fan speed membership.

### Conclusion
The Exhaust Fan Controller is an example of how fuzzy logic can be used to control a fan speed based on temperature and air quality. You can adapt the code and rules to suit your specific application and requirements.