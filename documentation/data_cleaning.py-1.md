# data\_cleaning.py(1)

import pandas as pd

\# Load the dataset

df = pd.read\_csv('network\_traffic\_data.csv')

\# Remove irrelevant columns

df.drop(\['Timestamp'], axis=1, inplace=True)

\# Handle missing values

df.fillna(0, inplace=True)

\# Filter out noise

df = df\[df\['Packet\_Length'] > 0]
