# model\_training.py

from sklearn.model\_selection import train\_test\_split

from sklearn.ensemble import RandomForestClassifier

from sklearn.metrics import accuracy\_score

\# Split the data into training and testing sets

X = df\_scaled.drop('Label', axis=1)

y = df\_scaled\['Label']

X\_train, X\_test, y\_train, y\_test = train\_test\_split(X, y, test\_size=0.2, random\_state=42)

\# Initialize and train the model

clf = RandomForestClassifier(random\_state=42)

clf.fit(X\_train, y\_train)

\# Make predictions

y\_pred = clf.predict(X\_test)

\# Evaluate the model

accuracy = accuracy\_score(y\_test, y\_pred)

print(f'Accuracy: {accuracy}')
