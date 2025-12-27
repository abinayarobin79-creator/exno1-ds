# Exno:1
Data Cleaning Process

# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# Algorithm
STEP 1: Read the given Data

STEP 2: Get the information about the data

STEP 3: Remove the null values from the data

STEP 4: Save the Clean data to the file

STEP 5: Remove outliers using IQR

STEP 6: Use zscore of to remove outliers

# Coding and Output
            <<include your coding and its corressponding output screen shots here>>
df=pd.read_csv("data_set.csv")

df

<img width="1029" height="388" alt="Screenshot 2025-12-27 193612" src="https://github.com/user-attachments/assets/41296dbb-6292-4d86-8c65-fb140b261ec2" />

df.isnull()

<img width="855" height="654" alt="Screenshot 2025-12-27 193626" src="https://github.com/user-attachments/assets/c4db59c0-7f5e-4b38-8cab-c19ca06e51ae" />

df.isnull().sum()

<img width="396" height="245" alt="Screenshot 2025-12-27 193638" src="https://github.com/user-attachments/assets/5163ab31-ca6f-429d-be97-a88eb4382f9e" />

df.notnull()

<img width="1022" height="449" alt="Screenshot 2025-12-27 193649" src="https://github.com/user-attachments/assets/2fe93786-6db6-47fb-9051-2b74bce4e906" />

print(df.dropna(axis=0))

<img width="643" height="775" alt="Screenshot 2025-12-27 193702" src="https://github.com/user-attachments/assets/2fdceac6-debe-4216-ae4f-a1a8408e6652" />

print(df.dropna(axis=1))

<img width="507" height="282" alt="Screenshot 2025-12-27 193716" src="https://github.com/user-attachments/assets/653683e7-a6fa-48a4-a159-fe74947c5612" />

dfs=df[df['num_episodes']>20]

dts

<img width="1024" height="656" alt="Screenshot 2025-12-27 193730" src="https://github.com/user-attachments/assets/97b4d233-1e49-494f-adc5-3cd2021c4dee" />

dfs=sd[sd['country'].str.startswith(('C'))&(df['num_values']>15)]

dfs

<img width="1029" height="685" alt="Screenshot 2025-12-27 193745" src="https://github.com/user-attachments/assets/d6c117be-11d8-45da-b6d3-7a0d1765eefa" />

df.iloc[:4]

<img width="1022" height="154" alt="Screenshot 2025-12-27 193758" src="https://github.com/user-attachments/assets/64e0819f-3a0f-48b3-88b8-42029cea6380" />

df.iloc[[1,3,5],[1,3]]

<img width="308" height="154" alt="Screenshot 2025-12-27 193805" src="https://github.com/user-attachments/assets/787626a4-a80d-452d-88e4-10b3da27f4f5" />

df.iloc[0:4,1:4]

<img width="412" height="181" alt="Screenshot 2025-12-27 193813" src="https://github.com/user-attachments/assets/81a95600-8d0b-4b8d-99e1-f379a6a3dbb9" />

dff=df.fillna(0)

dff

<img width="1026" height="389" alt="Screenshot 2025-12-27 193826" src="https://github.com/user-attachments/assets/08f678a8-d552-419e-bcc0-05eae71c5efc" />

df.fillna(method='ffill')

<img width="1023" height="395" alt="Screenshot 2025-12-27 193836" src="https://github.com/user-attachments/assets/298cb85f-0556-40f3-9794-20867357d658" />

df.fillna(method='bfill')

<img width="1020" height="418" alt="Screenshot 2025-12-27 193848" src="https://github.com/user-attachments/assets/cde9af9c-0c9b-47e7-aa73-d2141c0b3ac8" />

df['num_episodes'].fillna(value=df['num_episodes'].mean())

<img width="428" height="247" alt="Screenshot 2025-12-27 193859" src="https://github.com/user-attachments/assets/b3846bc7-8dfe-4ed0-ac9f-daa1096f198d" />

df['num_episodes'].fillna(value=df['num_episodes'].mean(),inplace=False)

<img width="409" height="248" alt="Screenshot 2025-12-27 193906" src="https://github.com/user-attachments/assets/ac93d527-013f-4269-834d-e18d8bdbb1f7" />

import matplotlib.pyplot as plt plt.bar(df["country"],df["num_episodes"])

plt.show()

<img width="735" height="463" alt="Screenshot 2025-12-27 193920" src="https://github.com/user-attachments/assets/932af5e8-42ef-4edf-b7a7-cfe9084f1d2f" />

plt.barh(df["country"],df["num_episodes"])

plt.show()

<img width="790" height="466" alt="Screenshot 2025-12-27 193931" src="https://github.com/user-attachments/assets/ceb35379-df2d-447b-94b5-01e55342043c" />

plt.plot(df["country"],df["num_episodes"])

plt.show()

<img width="734" height="465" alt="Screenshot 2025-12-27 193940" src="https://github.com/user-attachments/assets/c3a8c11b-3653-4168-a1d6-29f021ae5891" />

plt.scatter(df["country"],df["num_episodes"])

plt.show()

<img width="733" height="462" alt="Screenshot 2025-12-27 193949" src="https://github.com/user-attachments/assets/e5e075bd-21e6-4c0a-ac6b-4be7272bd979" />

# Result
The Data cleaning process is completed successfuly
