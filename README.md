# AMLT_1_SiraevaGM
Task1 Interpretable Machine Learning по курсу AMLT


## The Dataset about bank data: 
https://github.com/pycaret/pycaret/blob/master/datasets/bank.csv

Description:
Customer data:
1 - age: age <br>
2 - job: type of job (administrator, worker, entrepreneur, maid, manager, pensioner, self-employed, service industry, student, technician, unemployed, unknown) <br>
3 - marital: marital status (divorced, married, not married, unknown; Note: "divorced" means divorced or widowed) <br>
4 - education: education (primary, secondary, higher and unknown) <br>
5 - default: has default credit? (no, yes, unknown.) <br>
6 - housing: is there a mortgage? (no, yes, unknown.) <br>
7 - loan: is there a personal loan? (no, yes, unknown.) <br>
8 - balance: balance.

#### Data on the last contact within the campaign:
9 - contact: type of contact ("cellular", "phone") <br>
10 - month: last contact month ('jan', 'feb', 'mar', ..., 'nov', 'dec') <br>
11 - day: last contact day of the week ('mon', 'tue', 'wed', 'thu', 'fri') <br>
12 - duration: duration of the last contact, in seconds <br>

#### Others:
13 - campaign: the number of contacts made during this campaign for this client (includes the last contact) <br>
14 - pdays: the number of days since the last contact with the customer from the previous campaign (999 means that the customer has not previously contacted) <br>
15 - previous: number of contacts made before this campaign for this client <br>
16 - poutcome: the result of a previous marketing campaign ("failure", "nonexistent", "success") <br>
17 - deposit: Has the client agreed to issue a term deposit? ("yes", "no")

The goal is 
to predict whether the client will open deposit or not. So its binary classification problem with target variable of deposit column
<img width="1155" height="167" alt="image" src="https://github.com/user-attachments/assets/69dd1f53-4c79-4140-ae20-b0f32903375a" />

We applied for the classification task model  RandomForestClassifier

<img width="419" height="182" alt="image" src="https://github.com/user-attachments/assets/d9830f50-5629-4913-9007-b2d705c7f364" />

<img width="1867" height="513" alt="image" src="https://github.com/user-attachments/assets/743ca336-cb5d-464f-bd7c-4d917fb21fe9" />

<img width="1868" height="507" alt="image" src="https://github.com/user-attachments/assets/acb4e898-637e-4536-a8af-2e33c2609ea5" />

<img width="1872" height="597" alt="image" src="https://github.com/user-attachments/assets/2e969f07-f1a9-4059-998d-77ca27d1e542" />

<img width="1873" height="402" alt="image" src="https://github.com/user-attachments/assets/7d598802-1393-46e3-b417-af2835998d86" />


<img width="1864" height="724" alt="image" src="https://github.com/user-attachments/assets/948a5ac1-810b-4c76-b2a1-6bc419f31ebc" />

The comparision between evaluation models

<img width="928" height="128" alt="image" src="https://github.com/user-attachments/assets/464b00e5-f5a0-4c69-a11a-94f8ef886378" />


Well, we can say that all models identify duration and recent campaign-related attributes, such as poutcome and pdays, as the most significant positive drivers for deposit opening. While SHAP, permutation importance, and ELI5 mostly agree on the top influential features, there are some differences in the ranking and in the identification of negatively contributing features, where demographic variables like job, age, and education appear most often. ELI5 and permutation model are atcually the same - just differs the goal of the model - one is more for vizualization (ELI5), but the results are the same as expected. 

Overall, all interpretability approaches highlight the dominant role of campaign engagement over static demographic data in predicting a client's decision.






