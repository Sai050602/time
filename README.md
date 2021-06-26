#include <iostream>
#include <iomanip>
 
using namespace std;
 
class Time
{
    private:
        int seconds;
        int h,m,s;
    public:
        void inputTime(void);
        void convertingtoSeconds(void);
        void displayTime(void);
};
 
void Time::inputTime(void)
{
    cout << "Enter time:" << endl;
    cout << "Hours?   ";          
	cin >> h;
    cout << "Minutes? ";          
	cin >> m;
    cout << "Seconds? ";          
	cin >> s;
}
 
void Time::convertingtoSeconds(void)
{
    seconds = h*3600 + m*60 + s;
}
 
void Time::displayTime(void)
{
    cout << "The time is = " << setw(2) << setfill('0') << h << ":"
                             << setw(2) << setfill('0') << m << ":"
                             << setw(2) << setfill('0') << s << endl;
    cout << "Time in total seconds: " << seconds;
}
 
int main()
{
    Time T; 
     
    T.inputTime();
    T.convertingtoSeconds();
    T.displayTime();
     
    return 0;
}
