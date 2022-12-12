# PYTHON

import pandas as pd
import time
no_of_student=int(input("Enter the no record you want to enter"))
student=[]
marks=[]
updated_marks=[]
print("ENTER THE NAME OF STUDENT ")
for i in range(no_of_student):
    a=input(f"{i+1}. ")
    student.append(a)
time.sleep(3)
print(" ")
print("ENTER THE STUDENT MARKS ")
for i in range(no_of_student):
    b=int(input(f"{student[i]} "))
    marks.append(b)

zipped1 = list(zip(student,marks))
df1 = pd.DataFrame(zipped1, columns=['NAME', 'MARKS'])
print(df1)
time.sleep(3)
print(" ")

print("ENTER THE UPDATED MARKS OF STUDENT")
for i in range(no_of_student):
    c=int(input(f"{student[i]} "))
    updated_marks.append(c)
print(" ")
zipped = list(zip(student,marks, updated_marks))
df = pd.DataFrame(zipped, columns=['NAME', 'MARKS', 'UPDATED MARKS'])
print(df)
time.sleep(3)
print(" ")

a1=(max(marks))
index = marks.index(a1)
print(f"ACCORDING TO MARKS YOU SUBMMITED HIGHEST MARKS IS OF {student[index]}")
print(" ")
time.sleep(2)
a2=(max(updated_marks))
index1 = updated_marks.index(a2)
print("="*80)
print(f"ACCORDING TO UPDATED MARKS YOU SUBMMITED HIGHEST MARKS IS OF {student[index1]}")
print(f"DIFFERENCE BETWEEN MARKS OBTAIN AND UPDATED MARKS OF {student[index1]} is {a2-a1}")
print("="*80)
