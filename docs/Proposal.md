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

Start Progam
IF choice is "1" (DISPLAY):
    GET students_data from ref
    IF students_data exists:
        FOR EACH student in students_data:
            PRINT student ID and Name
            IF student has subjects:
                FOR EACH subject and grade:
                    PRINT subject name and grade
    ELSE:
        PRINT "No students found."

ELSE IF choice is "2" (ADD):
    INPUT sid, name, section, math_grade, cs_grade
    CREATE student object
    SAVE student to ref
    PRINT "Success!"

ELSE IF choice is "3" (UPDATE):
    INPUT sid
    IF sid exists in database:
        INPUT new name, section, math_grade, cs_grade
        UPDATE database record at sid with new values
    	PRINT "Update successful"
    ELSE:
        PRINT "Student not found."

ELSE IF choice is "4" (DELETE):
    INPUT sid
    IF sid exists:
        REMOVE record from database
        PRINT "Deleted successfully"
    ELSE:
        PRINT "Student not found"

ELSE IF choice is "5" (FEATURES):
    WHILE True:
        DISPLAY "FEATURES" (Average, Passing, Search, Organize, Failing, Back to Main Menu)
        GET choice
        IF choice is "6": BREAK (Back to main menu):
        	INPUT sid
        	GET student data from database
        IF student does not exist or has no grades:
            PRINT "Error"
			CONTINUE to next iteration
	    CASE choice OF:
            "1": CALCULATE average of all grades and PRINT
            "2": PRINT subjects where grade <= 2.50
            "3": INPUT subject name, GET and PRINT specific grade
            "4": SORT subjects by grade (descending) and PRINT
            "5": PRINT subjects where grade > 2.50
            DEFAULT: PRINT "Invalid choice"

ELSE IF choice is "6" (EXIT):
    PRINT "Exiting Program. Goodbye!"
    TERMINATE loop

ELSE:
    PRINT "Invalid choice"

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

