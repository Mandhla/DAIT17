# DAIT17
#include <cstdlib>
#include <iostream>
#include <fstream>
#include <string>

using namespace std;

class Student{
    string regNum;
    string fName;
    float studentFees;
public:
void SetRegNum(string regN);
void SetFullName(string fn);
void SetStudentFees(float fees);
string GetRegNum();
string GetFullName();
float GetStudentFees();
};

void Student::SetRegNum(string regN){
    regNum=regN;
}

string Student::GetRegNum(){
    return regNum;
}

void Student::SetFullName(string fn){
    fName=fn;
}

string Student::GetFullName(){
    return fName;
}

void Student::SetStudentFees(float fees){
    studentFees=fees;
}

float Student::GetStudentFees(){
    return studentFees;
}

class SOT:public Student{
    string lab;
    string staff;
    string course;
public:
    void SetLab(string lb);
    void SetStaff(string stf);
    void SetCourse(string crse);
    string GetLab();
    string GetStaff();
    string GetCourse();
    
};

void SOT::SetCourse(string crse){
    course=crse;
}
string SOT::GetCourse(){
    return course;
}

class Law:public Student{
    int semester;
    string lecturer;
public:
    void SetSemester(int smstr);
    void SetLecturer(string lctur);
    int GetSemester();
    string GetLecturer();
};

class Diploma:public SOT{
    string daitModules;
    
};

class Certificate: public SOT{
    string caitModules;
};

class Hardware: public Diploma{
    int numberOfArduinoKits;
};

class Software: public Diploma{
    int numberOfcomputers;
    
};

int main(int argc, char** argv) {
    string name;
    string course;
    Software obj1;
    string filename;
    cout<<"Hello User"<<endl;
    cout<<"Enter your full name:"<<endl;
    getline(cin,name);
    cout<<"What is your course:"<<endl;
    getline(cin,course);
    obj1.SetFullName(name);
    obj1.SetCourse(course);
    
    return 0;
}
