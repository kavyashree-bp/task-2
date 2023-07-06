# task-2
import matplotlib.pyplot as plt

# Dummy data
states = ['State A', 'State B', 'State C', 'State D']
active_cases = [500, 700, 400, 300]
deaths = [50, 30, 40, 20]
recovered = [450, 670, 360, 280]

# Create a bar chart
plt.figure(figsize=(10, 6))
plt.bar(states, active_cases, label='Active Cases')
plt.bar(states, deaths, label='Deaths', bottom=active_cases)
plt.bar(states, recovered, label='Recovered', bottom=[a + d for a, d in zip(active_cases, deaths)])

# Add labels and title
plt.xlabel('States')
plt.ylabel('Number of Cases')
plt.title('COVID-19 Cases by State')

# Add legend
plt.legend()

# Display the chart
plt.show()
