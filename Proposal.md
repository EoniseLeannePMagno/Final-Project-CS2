_Project Proposal_

Project Title: Grade-Book

Problem Statement:
The problem is that when grading students, various issues can occur that make the process inefficient or inaccurate. The project requires correct and reliable data on students’ grades. Many students and teachers face difficulties in grading due to time constraints, human errors, and other complications. When using a data set, grading can also be affected by syntax errors or incorrect code, leading to wrong outputs.

Project Objectives:
	1.	To compute student grades using a coding program.
	2.	To help teachers and students generate useful summaries such as averages and pass/fail results.
	3.	To practice programming concepts by applying them to real-life situations.

Planned Features:
	1.	Compute the general average of one student.
	2.	List the subjects where the student scored 2.5 or better.
	3.	Determine the final grade of a student for the entire school year.
	4.	Organize the student’s grades using any preferred sorting method.
	5.	Notify students whenever they have a failing grade.

Planned Inputs and Outputs:

Inputs:
	•	Student ID
	•	Student name
	•	Section
	•	Subject name
	•	Grade
	•	Sorting option

Outputs:
	•	Student’s general average
	•	Subjects where the student scored ≥ 2.50
	•	Student’s final overall grade for the school year
	•	Sorted list of the student’s grades
	•	List of the student’s failing grades


_Pseudocode_

Start Program
Load JSON file "students.json" containing all student data
Display menu of features:
    1. Show all student records
    2. Compute general average of a student
    3. List subjects where the student scored ≤ 2.50
    4. List failing subjects (grade > 3.0)
    5. Sort a student’s subjects by grade
    6. Exit program
Ask user to choose a feature
IF user chooses 1:
        For each student in JSON data:
            Display Student ID, Name, Section
            Display all subjects with their grades
ELSE IF user chooses 2:
        Ask for Student ID
        Find the student in JSON data
        Compute total of all grades
        Compute general average = total / number of subjects
        Display the general average
ELSE IF user chooses 3:
        Ask for Student ID
        Find the student in JSON data
        Create a list of subjects with grade ≤ 2.50
        Display the list, or display “None” if empty
ELSE IF user chooses 4:
        Ask for Student ID
        Find the student in JSON data
        Create a list of subjects with grade > 3.0
        Display the list, or display “None” if empty
ELSE IF user chooses 5:
        Ask for Student ID
        Find the student in JSON data
        Ask user for sorting option (ASC or DESC)
        Sort the student’s subjects by grade according to the chosen order
        Display the sorted subjects with grades
ELSE IF user chooses 6:
        Display "Exiting program..."
ELSE:
        Display "Invalid choice. Please try again."
Repeat menu until user chooses 6
End Program


_JSON dataset:_

[
  {
    "id": 1,
    "name": "Maria Santos",
    "section": "7-Ampere",
    "subjects": {
      "Math2": 1.5,
      "Math3": 1.75,
      "Biology1": 2.0,
      "Chem1": 1.25,
      "Physics1": 1.75,
      "Computer Science2": 1.25,
      "PEHM2": 1.0,
      "VE2": 1.75,
      "Social Science2": 1.5,
      "English2": 1.25,
      "Filipino2": 1.75
    }
  },
  {
    "id": 2,
    "name": "Juan Dela Cruz",
    "section": "7-Curie",
    "subjects": {
      "Math2": 2.5,
      "Math3": 2.75,
      "Biology1": 2.0,
      "Chem1": 2.25,
      "Physics1": 2.5,
      "Computer Science2": 2.0,
      "PEHM2": 1.75,
      "VE2": 2.5,
      "Social Science2": 2.25,
      "English2": 2.0,
      "Filipino2": 2.75
    }
  },
  {
    "id": 3,
    "name": "Ana Reyes",
    "section": "7-Rutherford",
    "subjects": {
      "Math2": 1.0,
      "Math3": 1.25,
      "Biology1": 1.5,
      "Chem1": 1.0,
      "Physics1": 1.25,
      "Computer Science2": 1.0,
      "PEHM2": 1.25,
      "VE2": 1.25,
      "Social Science2": 1.0,
      "English2": 1.25,
      "Filipino2": 1.5
    }
  },
  {
    "id": 4,
    "name": "Carlo Mendoza",
    "section": "7-Newton",
    "subjects": {
      "Math2": 2.75,
      "Math3": 3.0,
      "Biology1": 2.5,
      "Chem1": 2.75,
      "Physics1": 2.5,
      "Computer Science2": 2.25,
      "PEHM2": 2.0,
      "VE2": 2.5,
      "Social Science2": 2.25,
      "English2": 2.75,
      "Filipino2": 2.5
    }
  },
  {
    "id": 5,
    "name": "Liza Villanueva",
    "section": "7-Ampere",
    "subjects": {
      "Math2": 1.25,
      "Math3": 1.5,
      "Biology1": 1.75,
      "Chem1": 1.25,
      "Physics1": 1.5,
      "Computer Science2": 1.0,
      "PEHM2": 1.25,
      "VE2": 1.0,
      "Social Science2": 1.25,
      "English2": 1.25,
      "Filipino2": 1.5
    }
  },
  {
    "id": 6,
    "name": "Pedro Cruz",
    "section": "7-Curie",
    "subjects": {
      "Math2": 3.0,
      "Math3": 2.75,
      "Biology1": 2.5,
      "Chem1": 3.0,
      "Physics1": 2.75,
      "Computer Science2": 2.5,
      "PEHM2": 2.0,
      "VE2": 2.5,
      "Social Science2": 2.75,
      "English2": 3.0,
      "Filipino2": 2.75
    }
  },
  {
    "id": 7,
    "name": "Sofia Ramos",
    "section": "7-Rutherford",
    "subjects": {
      "Math2": 1.75,
      "Math3": 2.0,
      "Biology1": 2.25,
      "Chem1": 2.0,
      "Physics1": 1.75,
      "Computer Science2": 1.5,
      "PEHM2": 1.25,
      "VE2": 1.75,
      "Social Science2": 2.0,
      "English2": 1.5,
      "Filipino2": 1.75
    }
  },
  {
    "id": 8,
    "name": "Miguel Torres",
    "section": "7-Newton",
    "subjects": {
      "Math2": 2.25,
      "Math3": 2.5,
      "Biology1": 2.75,
      "Chem1": 2.5,
      "Physics1": 2.25,
      "Computer Science2": 2.0,
      "PEHM2": 2.25,
      "VE2": 2.0,
      "Social Science2": 2.25,
      "English2": 2.5,
      "Filipino2": 2.75
    }
  },
  {
    "id": 9,
    "name": "Grace Lim",
    "section": "7-Ampere",
    "subjects": {
      "Math2": 1.0,
      "Math3": 1.25,
      "Biology1": 1.0,
      "Chem1": 1.25,
      "Physics1": 1.0,
      "Computer Science2": 1.0,
      "PEHM2": 1.25,
      "VE2": 1.0,
      "Social Science2": 1.25,
      "English2": 1.0,
      "Filipino2": 1.25
    }
  },
  {
    "id": 10,
    "name": "Andrei Bautista",
    "section": "7-Curie",
    "subjects": {
      "Math2": 2.5,
      "Math3": 2.75,
      "Biology1": 3.0,
      "Chem1": 2.5,
      "Physics1": 2.25,
      "Computer Science2": 2.5,
      "PEHM2": 2.25,
      "VE2": 2.75,
      "Social Science2": 3.0,
      "English2": 2.75,
      "Filipino2": 2.5
    }
  }
]


_Flowchart_
(Found in the Github Repository)

