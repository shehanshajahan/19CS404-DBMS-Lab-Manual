# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---


## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University 
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites.

# ER Diagram Submission - Student Name
```
Name : Shehan Shajahan
Register Number : 212223240154
```
## Scenario Chosen:
University Database

## ER Diagram:
![image (3)](https://github.com/user-attachments/assets/0916079e-b3e8-4b2b-99bd-5fd315bbc010)



## Entities and Attributes:
- Student: StudentID,Name,Gender,DOB,Email,Phone,Address
- Instructor: InstructorID,Name,Phone,Email
- Department: DepartmentID,Department Name,Head of Department
- Course: CourseID,Course Name,Credits
- Enrollment : EnrollmentID,EnrollmentDate,Grade
- Schedule : ScheduleID,Day,Time
- Classroom : ClassroomID,Building,Room Number,Capacity
...

## Relationships and Constraints:
- Enrollment (StudentID,CourseID )
- Course (DepartmentID, CourseID)
- Instructor(InstructorID,CourseID)
- Schedule(CourseID,ClassroomID)
...


## RESULT
Thus,we have created an E-R Diagram for the chosen scenario successfully defining necessary entities,attributes,relationships and constraints.
