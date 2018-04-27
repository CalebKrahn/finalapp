# My Final App
## Caleb Krahn

### This is the website for my Final App in my CIS-277 Advanced C++ class.

## Description
This app is used to determine whether you need to take your garbage out or not. It does not take into account for holidays or delayed garbage days. The app should ask which day your garage is taken, then get what day of the week it is, then tell you whether you need to take your garbage out or not.

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
  
  
  
  
  
# Ignore this bit. It's so I know what to use for formatting.
You can use the [editor on GitHub](https://github.com/CalebKrahn/finalapp/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/CalebKrahn/finalapp/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
