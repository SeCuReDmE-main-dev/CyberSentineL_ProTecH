# data\_splitting.py

\# Sample code for data splitting

from sklearn.model\_selection import train\_test\_split

\# Define features and target variable

X = normalized\_features

y = df\['Threat\_Label']

\# Split the data into training and testing sets

X\_train, X\_test, y\_train, y\_test = train\_test\_split(X, y, test\_size=0.2, random\_state=42)
