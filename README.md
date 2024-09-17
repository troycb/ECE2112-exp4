# ECE2112 Experiment 4
Experiment 4 contains a problem for the student to identify the codes and functions needed in cleaning and visualizing data and to e able to apply and use the different codes and functions in creating a Python program that will be used in data wrangling and data visualization.

## ECE Board Problem
The problem asks to analyze the given data and present different data frames and visuals using different data wrangling and data visualization techniques.
### Data Frames
  1. The first data frame is the name, GEAS score, and Electronics score of those who took the Instrumentation track, have a score higher than 70 in Electronics, and their hometown is Luzon, which is made by using **board.loc[(board['Hometown']=='Luzon')&(board['Track']=='Instrumentation')&(board['Electronics']>70),['Name', 'GEAS','Electronics']]**, where the conditions that the row must contain the string 'Luzon' in the column 'Hometown'. the string 'Instrumentation' in the column 'Track', the values in the column 'Electronics' must be above 70, and to only show the columns Name, GEAS, and Electronics must be satisfied.
![image](https://github.com/user-attachments/assets/86ff34b9-b6c1-48e8-ad38-561af0f95c90)

  2. The second data frame is the name, track, Electronics score, and the Average score of those who are female, their average is 55 and higher, and their hometown is Luzon. Before making the data frame, the column 'Average' needs to be created, as there was no column with the index 'Average' in the given data. It is created by using **board['Average'] = board[['Math','Electronics','GEAS','Communication']].mean(axis=1)**, where it will calculate for the mean score of each row in the data and its value is set for each row. The data frame is then made by using **Mindy = board.loc[(board['Hometown']=='Mindanao')&(board['Gender']=='Female')&(board['Average']>=55),['Name','Track','Electronics','Average']]**, where the conditions that the row must contain the string 'Mindanao' in the column 'Hometown', the string 'Female' in the column 'Gender', the values in the column 'Average' must be 55 or higher, and to only show the columns Name, Track, Electronics, and Average must be satisfied.
![image](https://github.com/user-attachments/assets/616889da-f2b7-429b-af10-21ec1e92e0c8)

## Data Visualization
The data visualization must show how the different features contribute to average grades. This is done by using the **plt.bar** and creating a bar graph with the tracks, gender, and hometown at the x-axis while the average score is at the y-axis. plt.bar is used three times for each feature as the function can only use one column at a time. The chosen track in college, gender, or hometown can contribute to a higher average score. The people who are female took the Microelectronics track, and their hometown is Luzon, which has a higher average score.
![image](https://github.com/user-attachments/assets/3fbc5ede-a301-436e-9106-bcb3e12b9172)
