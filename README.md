##🎓 Student Management System

A beginner-friendly Python project that demonstrates a simple role-based student management system using lists, dictionaries, conditional statements, and user input.

**🚀 Features**

- Role-Based Access: Supports three roles — Student, Admin, and Operator.
- Basic Authentication: Checks the member's role and password.
- Student Portal: Allows students to view their marks.
- Admin Portal: Allows admins to view help commands and add student records.
- Operator Portal: Allows operators to add and delete student records.
- Input Validation: Handles invalid members, incorrect passwords, unknown student names, and invalid commands.

**🛠️ Technologies Used**

- Python 3
- Lists
- Dictionaries
- Conditional Statements ("if", "elif", "else")
- Nested Conditions
- User Input and Output

**📋 How It Works**

1. The user enters their role: "student", "admin", or "operator".
2. The program checks the password associated with that role.
3. After successful authentication, the user can access the features available to their role.
4. Students can check their marks.
5. Admins can add student records.
6. Operators can add or delete student records.

**▶️ How to Run**

1. Install Python 3.
2. Download or clone this repository.
3. Open a terminal in the project directory.
4. Run the program:

python student_management.py


**👨‍💻 Author**

**Garv**
GitHub: **"@Garv725"** (https://github.com/Garv725)

**📚 Learning Purpose**

This project was created to practise Python programming, logical thinking, debugging, and the use of lists and dictionaries in a practical application.

More improvements may be added in future. 
```python

x = ['student', 'admin', 'operator']
n = {'GARV': 100, 'A': 90, 'B': 85}
s = {'student': 1234, 'admin': 2498, 'operator': 4895}
h = ['help', 'ch']

member = input("Enter who you are: ").lower()

if member in x:
    print('You are', member, 'please enter your password')
    passw = int(input('Enter the password: '))

    if passw == s[member]:
        print("You are in,", member)

        if member == x[0]:
            stu = input("Enter your name: ").upper()

            if stu not in n:
                print("Invalid name")
            else:
                print("Your marks are:", n[stu])

        elif member == x[1]:
            ad = input("Enter what to do: ").lower()

            if ad == h[0]:
                print("The help list is:", h)

            elif ad == h[1]:
                ad = input("What to do: ").lower()

                if ad == 'add':
                    name = input("Enter the name: ").upper()
                    marks = int(input("Enter the marks: "))
                    n[name] = marks
                    print("The new dictionary is:", n)

                else:
                    print("Invalid admin command")

            else:
                print("Invalid admin option")

        elif member == x[2]:
            op = input("Enter what to do: ").lower()

            if op == h[0]:
                print("The help list is:", h)

            elif op == h[1]:
                op = input("What to do: ").lower()

                if op == 'add':
                    name = input("Enter the name: ").upper()
                    marks = int(input("Enter the marks: "))
                    n[name] = marks
                    print("The new dictionary is:", n)

                elif op == 'del':
                    item = input("Enter the name to delete: ").upper()

                    if item in n:
                        del n[item]
                        print("The new dictionary is:", n)
                    else:
                        print("Name not found")

                else:
                    print("Invalid operator command")

            else:
                print("Invalid operator option")

    else:
        print("Incorrect password")

else:
    print("Invalid member")

