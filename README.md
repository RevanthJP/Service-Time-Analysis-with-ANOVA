# Service Time Analysis with ANOVA

## EXECUTIVE SUMMARY
The staff of a service centre for electrical appliances includes three technicians who specialize in repairing three widely used electrical appliances from three different manufacturers. It was desired to study the effects of Technician and Manufacturer on the service time. Each technician was randomly assigned five repair jobs on each manufacturer's appliance, and the time to complete each job (in minutes) was recorded.

## INTRODUCTION
In this problem, the dataset is about technicians of a service centre who are specialized in repairing three widely used electrical appliances from three different manufacturers. The dataset has been analyzed using descriptive analysis and prepared for working with ANOVA. Both One-way ANOVA and Two-way ANOVA are used to find a solution for this problem.

## DATA DESCRIPTION
The given dataset contains the following columns and their descriptions are provided below:

- **Technician** – Contains technicians' group information.
- **Manufacturer** – Contains information about the different manufacturers.
- **Job** – Contains information about types of jobs.
- **Service_Time** – Contains the service time taken for each job by each technician.

## DATA SAMPLE
The sample of the given dataset is shown in the table below.

<img width="241" alt="image" src="https://github.com/user-attachments/assets/dd60d231-4871-45b3-9576-a15279862ae5">


## EXPLORATORY DATA ANALYSIS
Let us check for missing values and data types of the features in the dataset before proceeding further.

<img width="250" alt="image" src="https://github.com/user-attachments/assets/5147f331-c9bb-45bb-8dce-66ab81b1c8b4">


The dataset contains four features and forty-five non-null values in each feature. All the features in the dataset have integer data types. Upon checking the unique counts of each feature, it is found that **Technician**, **Manufacturer**, and **Job** each have three categories, with 15 entries for each category under each feature.

## Descriptive Analysis
Now, let us see the descriptive statistics of the given dataset using the table below.

<img width="349" alt="image" src="https://github.com/user-attachments/assets/3243be9d-d508-4932-b733-01b8e4823ae7">


From the table, we can see that the average time taken for a single service is 55.8 minutes, and the longest service time recorded is 70 minutes.

### STATE THE NULL AND ALTERNATE HYPOTHESIS FOR CONDUCTING ONE-WAY ANOVA FOR BOTH THE VARIABLES ‘MANUFACTURER’ AND ‘TECHNICIAN’ INDIVIDUALLY.

- **Null Hypothesis (Manufacturer)**: The mean service time taken for each manufacturer is the same.
- **Alternative Hypothesis (Manufacturer)**: The mean service time taken for at least one manufacturer is different.

- **Null Hypothesis (Technician)**: The mean service time taken for all three technician groups is the same.
- **Alternative Hypothesis (Technician)**: The mean service time taken for at least one technician group is different.

### PERFORM ONE-WAY ANOVA FOR VARIABLE ‘MANUFACTURER’ WITH RESPECT TO THE VARIABLE ‘SERVICE TIME’. STATE WHETHER THE NULL HYPOTHESIS IS ACCEPTED OR REJECTED BASED ON THE ANOVA RESULTS.

One-way ANOVA for variable **‘Manufacturer’** with respect to the variable **‘Service Time’** has been performed, and the results are given below.

The mean of the groups of variable **‘Manufacturer’** with respect to **‘Service Time’** is shown in the table below.

<img width="150" alt="image" src="https://github.com/user-attachments/assets/075d0459-6ccc-4b53-8072-d67c3091f858">


The mean service times of all the three groups are almost equal, except for the third group, which is slightly lower. The figure below also visualizes the mean of the three groups.

<img width="412" alt="image" src="https://github.com/user-attachments/assets/7d00192d-5cc2-4a5f-b924-452d415bfa0b">


Now, let us have a look at the p-value using the table below.

<img width="398" alt="image" src="https://github.com/user-attachments/assets/350356a3-dce2-4647-aba7-42b91436e9d6">


The p-value is significantly greater than 0.5. Since the mean value of the groups is almost the same and the p-value is greater than 0.5, the null hypothesis cannot be rejected, and it remains true here.

### PERFORM ONE-WAY ANOVA FOR VARIABLE ‘TECHNICIAN’ WITH RESPECT TO THE VARIABLE ‘SERVICE TIME’. STATE WHETHER THE NULL HYPOTHESIS IS ACCEPTED OR REJECTED BASED ON THE ANOVA RESULTS.

One-way ANOVA for variable **‘Technician’** with respect to the variable **‘Service Time’** has been performed, and the results are given below.

The mean of the groups of variable **‘Technician’** with respect to **‘Service Time’** is shown in the table below.

<img width="132" alt="image" src="https://github.com/user-attachments/assets/78d00c4f-aee6-4b79-89ed-28762fd11ee8">


The mean of all three technician groups is almost equal, except for the third group, which is slightly higher.

Let us visualize the mean using the point plot and see how it is spread. The figure below helps us understand visually that all the three means are closely aligned.

<img width="394" alt="image" src="https://github.com/user-attachments/assets/405d8ec6-38e7-4d7e-b856-ec09d3374848">


Now, let us have a look at the p-value using the table below.

<img width="380" alt="image" src="https://github.com/user-attachments/assets/85a4a93c-7083-4ee8-98d3-ca1363b5a932">


The p-value is higher than the significance level of 0.5.

From the one-way ANOVA performed above, the null hypothesis remains true as the p-value is greater than 0.5, and also, the mean of all the three technician groups is similar.

### ANALYZE THE EFFECTS OF ONE VARIABLE ON ANOTHER WITH THE HELP OF AN INTERACTION PLOT. WHAT IS AN INTERACTION BETWEEN TWO TREATMENTS?

The effect of one variable on another is visualized in the figure below using the interaction plot.

<img width="452" alt="image" src="https://github.com/user-attachments/assets/495ff837-fbc2-4455-b5a5-ef93d8f516e9">

Figure shows the interaction between each variable and their effects on each other. It can be clearly seen that the service time for each technician group varies with respect to the manufacturer.

- Technician group 1 finishes the work quicker for manufacturer 2 and has a high service time for manufacturer 1.
- Technician group 2 has a lesser service time for manufacturer 1 and vice versa for manufacturer 2.
- Technician group 3 completes the service quicker when it is manufacturer 3 compared to the other two manufacturers.

### PERFORM A TWO-WAY ANOVA BASED ON THE VARIABLES ‘MANUFACTURER’ & ‘TECHNICIAN’ WITH RESPECT TO THE VARIABLE ‘SERVICE TIME’ AND STATE YOUR RESULTS.

Two-way ANOVA has been performed based on the variables **‘Manufacturer’** and **‘Technician’** with respect to **‘Service Time’**. The result of the two-way ANOVA performed is displayed in the table below.

<img width="390" alt="image" src="https://github.com/user-attachments/assets/dd821821-4666-41e7-b381-5b8af0432407">

From the table above, it can be concluded that when the variables technician and manufacturer are considered separately, the variance is not significant. However, when both variables are considered together, the p-value is less than 0.5, indicating significant variance between the groups.

### BUSINESS IMPLICATIONS OF PERFORMING ANOVA FOR THIS PARTICULAR CASE STUDY

Upon performing one-way and two-way ANOVA, several business implications can be made:

- Since certain technicians have shorter service times for specific manufacturers, the service centre can ensure that the right technicians are assigned to the manufacturers they perform well with. This would help in achieving faster service.
- Cross-training sessions for every technician can be organized by the service centre in collaboration with each manufacturer. This would ensure that all technicians are trained to service all appliances manufactured by the three manufacturers, promoting balanced work distribution.
- Given that the dataset provided contains limited data on service time, technicians, and manufacturers, a more detailed study could be conducted to analyze why certain technician groups take more time servicing specific manufacturers' appliances. This analysis would help in identifying challenges faced by each technician and provide necessary support and training to overcome these challenges.
