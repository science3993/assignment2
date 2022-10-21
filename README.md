import numpy as np

a=np.random.randint(1,20,15)

a=a.reshape(3,5)

a

a.shape

a[np.where(a==np.max(a))]=0

a

import pandas as pd

df=pd.read_csv("./data.csv")

mean_value=df['Calories'].mean()

df['Calories'].fillna(value=mean_value,inplace=True)

df.head(25)

df.Duration.describe()

df.Pulse.describe()

df[(df['Calories']>500) & (df['Calories']<1000)]

df[(df['Calories']>500 & (df['Pulse']<100))]

df_modified=df.drop("Maxpulse",axis=1)

df_modified

df=df.drop("Maxpulse",axis=1)

df

df['Calories']=df['Calories'].astype(int)

df.dtypes

df.plot.scatter( x = 'Duration', y = 'Calories')

prgmng_df=pd.DataFrame({"popularity":[22.2, 17.6, 8.8, 8, 7.7, 6.7]},index=['Java','Python','PHP','JavaScript', 'C#', 'C++'])

prgmng_df

prgmng_df.plot.pie(y='popularity',autopct='%1.1f%%')
