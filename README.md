# inheritance
from datetime import date

class person:
     def __init__(self,name,dob,city):
        self.name=name
        self.dob=dob
        self.city=city
        def age(self):
            return date.today().year - self.dob

class student(person):
    fees = 10000
    no_of_students=0
    def __init__(self,name,rollno,dob,city):
        super().__init__(name,dob,city)
        self.rollno=rollno
        student.no_of_students = student.no_of_students+1
        
   
    
class Mechanical(student):
    fees=12000
    def __init__(self,name,rollno,dob,city,year):
        super().__init__(name,rollno,dob,city)
        self.year=year

class Teacher(person):
     def __init__(self,name,dob,city,students=[]):
            super().__init__(name,dob,city)
            self.students=students
            def show_students(self):
                for student in self.students:
                    print(student.name)
            
        

        
stu1=Mechanical('priya',180,2003,'Theni',2013)
stu2=Mechanical('Banupriya',179,2002,'Theni',2015)
t1=Teacher('ram',1992,'Theni',[stu1,stu2])
print(t1.name)
