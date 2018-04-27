# My Final App
## Caleb Krahn

### This is the website for my Final App in my CIS-277 Advanced C++ class.

## Description
This app is used to determine whether you need to take your garbage out or not. It does not take into account for holidays or delayed garbage days. The app should ask which day your garage is taken, then get what day of the week it is, then tell you whether you need to take your garbage out or not.
  
  
```
#include <iostream>  
#include <string.h>  
#include <time.h>  
  
  
using namespace std;  
  
int main() {  
  time_t now = time(0);  
 struct tm timeinfo = *localtime(&now);  
 string garbageday, currentday;  
 int tm_wday = timeinfo.tm_wday;  
   
 cout << "Enter what day of the week your garbage gets taken." << endl;  
 getline(cin, garbageday);  
   
 if(garbageday == "sunday")  
    {garbageday = "Sunday";}  
 else if(garbageday == "monday")  
    {garbageday = "Monday";}  
 else if(garbageday == "tuesday")  
    {garbageday = "Tuesday";}  
 else if(garbageday == "wednesday")  
    {garbageday = "Wednesday";}  
 else if(garbageday == "thursday")  
    {garbageday = "Thursday";}  
 else if(garbageday == "friday")  
    {garbageday = "Friday";}  
 else if(garbageday == "saturday")  
    {garbageday = "Saturday";}  
  
  
   
 switch(tm_wday) {  
  case 0: currentday = "Sunday";  
          break;  
  case 1: currentday = "Monday";  
          break;  
  case 2: currentday = "Tuesday";  
          break;  
  case 3: currentday = "Wednesday";  
          break;  
  case 4: currentday = "Thursday";  
          break;  
  case 5: currentday = "Friday";  
          break;  
  case 6: currentday = "Saturday";  
          break;  
 }  
   
 if (currentday == garbageday) {  
   cout << "Today is: " << currentday << "." << endl << "You said your garbage day is: " << garbageday << "." << endl << "That means you need to take out the garbage." << endl;  
 }  
 else {  
   cout << "Today is: " << currentday << ".\nIt is not garbage day." << endl;  
 }  
   
}  
```
