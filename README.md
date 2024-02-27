# Rating of shows and movies
import seaborn as sns
import matplotlib.pyplot as plt

# Create a count plot of ratings
sns.countplot(data=netflix, x='rating')

# Rotate the x-axis labels for better readability
plt.xticks(rotation=90, ha="right")

# Set the figure size
plt.figure(figsize=(13, 13))

# Set the title
plt.title('Rating')

# Show the plot
plt.show()

AOEqzRn2nDgrAAAAAElFTkSuQmCC (580Ã—479)

### Relation between Type and Rating
import seaborn as sns
import matplotlib.pyplot as plt
plt.figure(figsize=(10,8))
sns.countplot(x='rating',hue='type',data=netflix)
plt.title('Relation between Type and Rating')
plt.show()




#Pie-chart for the Type: Movie and TV Shows
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np

# Assuming you have a DataFrame named 'netflix' containing your data

# Count the occurrences of each type
type_counts = netflix['type'].value_counts()

# Define labels and sizes for the pie chart
labels = type_counts.index
sizes = type_counts.values

# Define colors for the pie chart
colors = plt.cm.Wistia(np.linspace(0, 1, len(labels)))

# Define explode (to separate slices)
explode = (0, 0.1)  # "explode" the second slice (TV show)

# Set the figure size
plt.figure(figsize=(9, 9))

# Create the pie chart
plt.pie(sizes, labels=labels, colors=colors, explode=explode, shadow=True, startangle=90, autopct='%1.1f%%')

# Add title and legend
plt.title('Distribution of Type', fontsize=25)
plt.legend()

# Show the plot
plt.show()



