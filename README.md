# C-Project-Login-Form
Simple project
              
              
                                                      c++ simple project APPLICANT LOGIN


#include <iostream>
using namespace std;

//function declare
void personal_informations();
void check_age();
void next_step();
void wrong_information();

// global variable
int password, captcha, age, information;
long long int mobile;
char name[35], middle[20], gmail[20], last[20];

int main()

{
    //applicant login
    cout << "___ APPLICANT LOGIN ___" << endl;
    cout << endl;
    cout << "Enter password ( only four digit) :";
    cin >> password;
    cout << endl;
    cout << "Enter mobile number :";
    cin >> mobile;
    cout << endl;
    cout << "Enter E-mail id :";
    cin >> gmail;
    cout << endl;
    cout << "This CAPTCHA are [1234] type  :";
    cin >> captcha;
    cout << endl;
    //End applicant login

    //condition of applicant login
    if (password >= 1000 && password <= 9999)
    {
        if (mobile >= 1000000000 && mobile <= 9999999999)
        {
            if (captcha == 1234)
            {
                cout << "*** YOUR LOGIN IS SUCCESFUL ****" << endl
                     << endl;

                personal_informations(); // go to personal_informations step
            }
            else
            {
                cout << "Warning" << endl;
                cout << "capatcha is wrong plz correct type  ";
            }
        }
        else
        {
            cout << "Warning" << endl;
            cout << "Mobile number is wrong plz Enter 10 digit Mobile Number";
        }
    }
    else
    {
        cout << "Warning" << endl;
        cout << " Password is wrong plz Enter 4 digits Number";
    }
}

//personal information
void personal_informations()
{

    cout << "___ PERSONAL INFORMATION ___" << endl;
    cout << "Enter your first name  :";
    cin >> name;
    cout << endl;
    cout << "Enter your last name  :";
    cin >> last;
    cout << endl;
    cout << "Enter your middle name  :";
    cin >> middle;
    cout << endl;
    cout << "Enter your age  (below < 18):";
    cin >> age;
    check_age(); //function is useing your age is above 18 or not
    cout << endl
         << endl;
}
//End personal information

//checking age above 18 or not
void check_age()
{
    if (age <= 18)
    {
        next_step(); // is use to go to next step and checking your information
    }
    else
    {
        cout << "warning" << endl;
        cout << "your age 18 >above you can not login form";
    }
}
// End checking age above 18 or not

//check your information
void next_step()
{

    cout << "________ CHECK YOUR INFORMATION ________" << endl;
    cout << "1] YOUR FULL NAME  IS :" << name << " " << middle << " " << last << endl;
    cout << "2] AGE IS  :" << age << endl;
    cout << "3] MOBILE NUMBER  IS  :" << mobile << endl;
    cout << "2] E-GMAIL  IS  :" << gmail << endl;
    cout << "2] PASSWORD IS  :" << password << endl
         << endl;
    cout << "YOUR INFORMATION IS RIGHT YOU TYPE(1) if not YOUR INFORMATION IS WRONG YOU TYPE(2) =";
    cin >> information;

    wrong_information();
}
// End check your information

// your form is complited
void wrong_information()
{
    if (information == 1)
    {
        cout << "***YOUR FORM IS COMPLITED***";
    }
    else if (information == 2)
    {
        personal_informations(); // if your information is wrong so call by personal information
    }
}








*************************output*****************************






___ APPLICANT LOGIN ___

Enter password ( only four digit) :2121

Enter mobile number :8976546754

Enter E-mail id :chinche212gmail.com

This CAPTCHA are [1234] type  :1234

*** YOUR LOGIN IS SUCCESFUL ****

___ PERSONAL INFORMATION ___    
Enter your first name  :jay     

Enter your last name  :chinche

Enter your middle name  :dnyaneshwar

Enter your age  (below < 18):18
________ CHECK YOUR INFORMATION ________
1] YOUR FULL NAME  IS :jay dnyaneshwar chinche
2] AGE IS  :18
3] MOBILE NUMBER  IS  :8976546754
2] E-GMAIL  IS  :chinche212gmail.com
2] PASSWORD IS  :2121

YOUR INFORMATION IS RIGHT YOU TYPE(1) if not YOUR INFORMATION IS WRONG YOU TYPE(2) =1
***YOUR FORM IS COMPLITED***
