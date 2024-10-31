Assignment: Student Management System using OOP in Python
Objective
Design and implement a CLI-based Student Management System in Python using OOP principles. The
system should manage student records, course enrollments, and grade assignments, with the added
capability to save and load data to/from a file.
Instructions
Section A: Class Design and Implementation
1. Class 1: Person
○ Attributes:
■ name (str): Name of the person.
■ age (int): Age of the person.
■ address (str): Address of the person.
○ Method:
■ display_person_info(): Print the details of the person (name, age, and address).
2. Class 2: Student (inherits from Person)
○ Additional Attributes:
■ student_id (str): Unique identifier for each student.
■ grades (dict): Dictionary containing subjects and their respective grades (e.g.,
{"Math": "A", "Science": "B"}).
■ courses (list): List of courses the student is enrolled in.
○ Methods:
■ add_grade(subject, grade): Add or update the grade for a specified subject.
■ enroll_course(course): Enroll the student in a specified course.
■ display_student_info(): Print all details of the student, including enrolled courses
and grades.
3. Class 3: Course
○ Attributes:
■ course_name (str): Name of the course.
■ course_code (str): Unique course code.
■ instructor (str): Name of the instructor.
■ students (list): List to store students enrolled in this course.
○ Methods:
■ add_student(student): Add a student to the course.
■ display_course_info(): Display the course details and the list of enrolled students.
Section B: System Functionalities
Develop a menu-driven CLI for users to interact with the system. Below is a description of the main
options and functionalities.
1. Add Student
○ Prompt the user for the following details: name, age, address, and student_id.
○ Create a new Student object with these details and add it to the system.
2. Enroll in Course
○ Prompt the user for the student_id and course_code.
○ Enroll the student with the specified ID in the course with the specified code.
3. Add Grade
○ Prompt the user for student_id, course_code, and grade.
○ Assign or update the grade for the student in the specified course. Ensure the student is
enrolled in the course before assigning a grade.
4. Display Student Details
○ Prompt the user for the student_id.
○ Retrieve and display the student’s details, including enrolled courses and grades.
5. Display Course Details
○ Prompt the user for the course_code.
○ Retrieve and display the course’s details, including the list of enrolled students.
Section C: Error Handling and File Operations
1. Error Handling
○ Verify that student_id and course_code exist before processing any operations.
○ Ensure grades are only assigned to students for courses in which they are enrolled.
2. Bonus Challenge: Save and Load Data
○ Implement two functions to manage file operations:
■ save_data(): Save all student and course data to a file in JSON format.
■ load_data(): Load data from the file, restoring student, course, and enrollment
information when the program restarts.
Sample Input Output:
Main Menu
When the program starts, display the main menu:
==== Student Management System ====
1. Add New Student
2. Add New Course
3. Enroll Student in Course
4. Add Grade for Student
5. Display Student Details
6. Display Course Details
7. Save Data to File
8. Load Data from File
0. Exit
Example Actions and Outputs
1. Add New Student
Input:
Select Option: 1
Enter Name: Sami
Enter Age: 22
Enter Address: Dhaka
Enter Student ID: S001
Output:
Student Sami (ID: S001) added successfully.
2. Add New Course
Input:
Select Option: 2
Enter Course Name: Physics
Enter Course Code: PHY101
Enter Instructor Name: Dr. ABC
Output:
Course Physics (Code: PHY101) created with instructor Dr. ABC.
3. Enroll Student in Course
Input:
Select Option: 3
Enter Student ID: S001
Enter Course Code: PHY101
Output:
Student Sami (ID: S001) enrolled in Physics (Code: PHY101).
4. Add Grade for Student
Input:
Select Option: 4
Enter Student ID: S001
Enter Course Code: PHY101
Enter Grade: A
Output:
Grade A added for Sami in Physics.
5. Display Student Details
Input:
Select Option: 5
Enter Student ID: S001
Output:
Student Information:
Name: Sami
ID: S001
Age: 22
Address: Dhaka
Enrolled Courses: Physics
Grades: {'Physics': 'A'}
6. Display Course Details
Input:
Select Option: 6
Enter Course Code: PHY101
Output:
Course Information:
Course Name: Physics
Code: PHY101
Instructor: Dr. ABC
Enrolled Students: Sami
7. Save Data to File
Input:
Select Option: 7
Output:
All student and course data saved successfully.
8. Load Data from File
Input:
Select Option: 8
Output:
Data loaded successfully.
0. Exit
Input:
Select Option: 0
Output:
Exiting Student Management System. Goodbye!

