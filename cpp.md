# C++ 

C++ is next level of C
It's very fast 

- advanced graphic apps 
- embedded systems 
- video games 

Language levels: 

- High level languages: Python, Java, C#
- Middle Level: C++, C
- Low Level: ASM
- Hardware 


### What is C++ good for?

C++ is a **high-performance**, **compiled**, **multi-paradigm** language.  
It's used when you need:
- Speed 
- Memory control 
- Hardware-level access 
- Large system development 

#### Applications of C++:

| Field / Application | Example |
|------------------|-----------|
| **Game development** | Unreal Engine, game engines, physics engines |
| **Operating systems**  | Parts of Windows, macOS, Linux kernels, drivers |
| **Embedded systems** | IoT devices, robotics, firmware, automotive software |
| **Finance / Trading**  | High-frequency trading (HFT) systems, quantitative finance models |
| **Graphics / Simulations**  | 3D modeling, CAD software, VR/AR, rendering engines |
| **Telecommunications**  | Network protocol stacks, 5G, baseband processing |
| **High-performance computing (HPC)**  | Supercomputers, parallel processing (with OpenMP, CUDA for GPUs) |
| **Databases**  | MySQL, MongoDB internals are written in C++ |
| **Compilers / Interpreters**  | Compilers like Clang, parts of GCC, LLVM |
| **Real-time systems**  | Automotive ECUs, avionics, space systems |


**C++ gives you power over performance and hardware**.

---

### Comparing with Python

Python is a **high-level**, **interpreted**, **dynamically-typed** language.

#### Applications of Python:

| Field / Application | Example |
|------------------|-----------|
| **Data Science / AI / ML**  | TensorFlow, PyTorch, scikit-learn |
| **Web Development**  | Django, Flask, FastAPI |
| **Scripting / Automation**  | Automation scripts, DevOps tools |
| **API development**  | FastAPI, Flask |
| **Data Analysis / Visualization**  | Pandas, Matplotlib, Seaborn |
| **Rapid prototyping**  | Quick MVPs, proof of concepts |
| **Cybersecurity**  | Penetration testing tools |
| **Education**  | Teaching programming basics, notebooks (Jupyter) |
| **Desktop applications**  | Tkinter, PyQt for GUI apps |
| **Cloud / Serverless**  | AWS Lambda, GCP Cloud Functions (Python runtime) |

**Python is fast for development, readable, and has huge libraries**.

---

### Side-by-Side Comparison: C++ vs Python

| Feature | C++ | Python |
|---------|-----|--------|
| **Performance** |  Extremely fast (compiled to machine code) |  Slower (interpreted) |
| **Memory Control** |  Manual (fine control: pointers, memory allocation) | Automatic (garbage collected) |
| **Ease of Use** |  Complex (manual setup, syntax heavy) |  Simple (clean syntax, beginner-friendly) |
| **Use Case** | Systems, embedded, performance-critical | Rapid development, scripting, ML/AI |
| **Error handling** | Compile-time (many caught early) | Runtime (errors show during execution) |
| **Cross-platform** |  But needs manual compilation |  Easy (interpreted) |
| **Libraries & Ecosystem** | Strong for performance & hardware | Huge ecosystem, esp. data/ML/web |
| **Development speed** |  Slower (compile/test cycle) |  Fast (write, run, debug quickly) |
| **Job market** | System software, embedded, HFT, game dev | ML Engineer, Data Scientist, Web Developer, Automation Engineer |

---

### When to use which?

| Scenario | Recommended |
|----------|-------------|
| Real-time system (robotics, aerospace, automotive) | **C++** |
| High-frequency trading, low latency |  **C++** |
| Quick data analysis or prototyping | **Python** |
| Machine learning and AI |  **Python** |
| Building performance-critical engines |  **C++** |
| Automation scripts or web servers |  **Python** |
| Game engine development |  **C++** |
| Teaching programming to beginners |  **Python** |

---


- **Python** for prototyping, ML/AI, fast testing.

- **C++** for mastering system-level thinking, algorithms, and performance-critical work (telecom, embedded, real-time).

A lot of companies **prototype in Python**, and once the solution works, **rewrite the performance-critical parts in C++**.


---


VS Code considereed IDE (Integrated Development Environments)
We need a compiler to converts source code to machine instructions. For windows we go with GCC, and for mac we use clang 
The extensions for C++ in VS Code are `C/C++` and `Code Runner`

For the compiler on mac we do this: 

terminal: 

`gcc -v` 

`clang --version`

`xcode-select --install`


we always write `#include <iostream>`
The `iostream` is a header file that contains functions for basic input and output operations. By writing this, we'll have access to usefull input and output operations 

Then we need a main function for the programming.

```c++
int main(){

   return 0; 
}
```

The `return 0` is for saying: if we reached `return 0`, then there is no problem in running the program. If `1` is returned, it means there is a problem. 

To write an output we write `std::` which means standard. 

then we write: `std::cout` where `c` means character. Alltogether means standard character output. 

then we use `<<` which means left shift operator when used with numbers. 

`std::cout<<"Hello"<<std::endl;`

If we include `using namespace std;` before the `int main()`, then there is no need to write `std` each time. 

---

```c++
#include <iostream>
using namespace std;
int main(){

    cout << "Hello World" << endl;
    
    return 0; 
}
```
---
```c++
#include <iostream>
int main(){

    std::cout << "Hello World" << std::endl;
    std::cout << "Hi how are you" << std::endl;
    std::cout << "How's everything" << '\n'; 

    // comment  
    
    /*
    This is for multiple lines of comments 
    You can write notes for some explanations 
    */

    return 0;
}
```
---

```c++
#include <iostream>

#include <map>
#include <set>
#include <string>
#include <vector> // for dynamic matrix and vector 

int main() {

    std::map<std::string, int> m = {{"a", 1}};
    
    std::set<int> s = {3, 1, 2};
    
    struct Point { int x; int y; };
    
    class Car { private: int speed; }; // Like struct but private by default
    
    std::vector<int> v = {1,2,3,4}; 
    // dynamic array (resizable), random access, you can increase the size with push_back like: v.push_back(3); 
    std::vector<std::vector<int>> arr = {
        {1,2,4,5,6},
        {1,2,3,4,5},
    };

    std::array<int, 3> arr = {1,2,3}; 
    // Fixed-size array (like a C array, but safer). Cannot change size after declaration.

    std::set<int> s = {3, 1, 2, 1}; // becomes {1, 2, 3}
    // Ordered container with unique elements.
    // Automatically sorted (by default using <).
    // No random access (you can’t do s[0]).

    int arr[5] = {1,2,3,4,5}; 
    
    int arr[3][4] = {
        {1,2,3,4},
        {5,6,7,8},
        {6,7,8,8}
    };

    std::tuple<int,double,char, std::string> A = {1,2.2,'a',"Hi"}; 
    std::pair<int,std::string> P = {1,"X"};

    struct Point {int x; int y;}; 
    // struct is to group variables under one name     
    
    return 0;
}
```
---

## Python Eauivalence: 

```python

import numpy as np 

# Array and Vector
arr = [1, 2, 3, 4, 5]
v = [9, 10, 11, 12, 13]

# Tuple and Pair
t = (1, 2.4, 'a')
p = (1, "Hello")

# Struct (Point)
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

# Class (Car)
class Car:
    def __init__(self):
        self.__speed = 0

    def setSpeed(self, s):
        self.__speed = s

    def getSpeed(self):
        return self.__speed


arr = [
    [1, 2, 3, 4],
    [5, 6, 7, 8],
    [9, 10, 11, 12]
]

arr = np.array([
    [1, 2, 3, 4],
    [5, 6, 7, 8],
    [9, 10, 11, 12]
])
```
---


```c++
#include <iostream>

int main(){

    int x; //decleration (i.e., define integer variable x)
    // integer number means ..., -1, 0, 1, 2, ...
    // so we can't input 1.2 for example, cause it's not integer anymore and we need to define double variable 
    x = 5; // assign a value to the variable x 
    // you can also say: int x = 5
    // std::cout << x;
    int y = 6;
    std::cout << x << '\n' ;
    std::cout << y << '\n' ;
    int sum = x + y;
    std::cout << sum << '\n' ;

    // double (numbers including decimal)
    double h = 2.77;
    std::cout << h << '\n';

    // single character 
    char grade = 'A';
    char initial = 'B';

    std::cout << initial << '\n';

    // char can only store a single characer. 
    // for example we can't store 'BC' with char
    
    // boolean (true or false), it's like a light switch (on/off)
    bool student = true;
    bool power = false; 
    
    // string (objects that represents a sequence of text)
    std::string name = "Hamed";
    std::cout << name << '\n'; 

    std::string day = "Friday";

    std::cout << "Hello " << name <<'\n'; // printing variable along with text 

    int age = 25; 
    std::cout << "You are " << age << " years old" << '\n';

    return 0;
}
```

---

```c++
#include <iostream>
int main(){
    // writing a program to calculate the circumference of a circle 
    const double PI = 3.14159; 
    // since we don't want this fix variable pi be changed, we use the command const
    // The common name convention for constants is to make all of the letters uppercase
    // so const is for making the variable 'read only' and not being able to change it 
    double radius =  10; 
    double circumference = 2*PI*radius; 
    std::cout << circumference << "cm";

    const int LIGHT_SPEED = 299792458;
    const int WIDTH = 10;

    return 0;
}
```
---

```c++
#include <iostream>
// Namespace: for preventing name conflicts in large projects 
// Allows for indentically named entities as long as namespaces are different 

namespace first{
    int x = 1; 
}
namespace second{
    int x = 2; 
}

int main(){
    int x = 0; 
    std::cout << x << '\n';
    std::cout << first::x << '\n';
    std::cout << second::x << '\n';

    return 0;
}



int main(){
    using namespace first; 
    std::cout << x;

    return 0; 
}



int main(){
    // if we use this we don't need to write std each time 
    using namespace std; 
    string name = "Hamed"; 
    cout << "Hi " << name;  
    return 0; 
}

int main(){
    // The problem is if we use the namespace std, there will be conflict with other namespaces 
    // therefore it's better to use this: 
    using std::cout; 
    using std::string; 

    return 0; 
}
```



---

```c++
#include <iostream>
#include <vector>

// suppose we have a very long data type and we want to give it a nickname (alias)
// our data type is: 
//std::vector<std::pair<std::string, int>>
// Instead of repeating this datatype, we can define a nickname for it and use: typedef ...... nickname

typedef std::vector<std::pair<std::string,int>> pairlist_t;

// pairlist is the nickname for this data type, then we add _t, as an indicator of type


int main(){
    
    pairlist_t pairlist; 

    return 0; 
}


//////////////////////////////////

// another example is: 

typedef std::string text_t; 
typedef int number_t; //instead of int datatype, we can use number_t 

int main(){

    // std::string FirstName = "Hamed"; 
    text_t FirstName = "Hamed";
    std::cout << FirstName << '\n';

    number_t age = 26; 
    std::cout << age <<'\n';

    return 0; 
}

// instead of typedef, we can use 'using'
// 'using' is more popular 

// typedef std::string text_t; 
// typedef int number_t; 

using text_t = std::string;
using number_t = int; 
```

---

```c++
#incluede <iostream>
int main(){
    // arithmetric operations = return the result of a specific arithmetric operation (+ - * /)
    int students = 20; 
    // students = students + 2; 
    students += 2; 
    students++; 
    students--;
    students/=2;
    students*=2; 
    int remainder = students % 3; 
    std::cout<<students;
     
    return 0; 
}
```
---

```c++
#incluede <iostream>
int main(){
    // type conversion: conversion a value of one datatype to another 
    // implicit: automatic 
    // explicit: precede value wth new data type (int) 
    double x = (int) 3.14; // explicit 
    int pi = 3.14; // implicit 

    char x = 100; 
    std::cout<<x; // this'll display 'd' since the equivalent ASCII code for 100 is 'd'

    std::cout<<(char) 100; 

    // Example: 
    int correct = 8; 
    int questions = 10; 
    double score = correct / (double)questions * 100; 
    strd::cout<< score << "%"; 
    return 0; 
}
```

---


```c++
#include <iostream>

// cout << (insertion operator)
// cin >> (extractionoperator)

int main(){
    std::string name; 
    int age; 
    std::cout<< "what's your age? ";
    std::cin>>age;

    // std::cout<< "what's your name?";
    // std::cin>>name;

    // if we need a string that contains ' ' (space) in it, we use `getline`
    std::cout<< "what's your full name? ";
    std::getline(std::cin>>std::ws, name); 
    // `std::ws` eliminates any new line character or any white spaces before any user input. 

    std::cout<<"Hello "<< name<<'\n';
    std::cout<<"you are "<<age<<"years old";
    
    return 0; 
}
```

---


```c++

#include <iostream>

int main(){
    double x = 3; 
    double y = 4; 
    double z; 
    double k; 
    z = std::max(x,y); 
    std::cout<<z; 
    k = std::min(x,y); 
    std::cout<<k; 
    return 0; 
}
```

---

```c++
#include <iostream>
#include <cmath>

int main(){

    double x = 3; 
    double y = 4; 
    double f1; 
    double f2; 
    double f3; 
    double f4; 
    double f5;

    f1 = pow(2,3); // 2^3 
    f2 = sqrt(9);
    f3 = abs(-3); 
    f4 = round(x); 
    f5 = ceil(x); // round down
    return 0; 
}
```


```c++
/* cos example */
#include <stdio.h>      /* printf */
#include <math.h>       /* cos */

#define PI 3.14159265

int main ()
{
  double w, result;
  w = 60.0;
  result = cos ( w * PI / 180.0 );
  printf ("The cosine of %f degrees is %f.\n", w, result );
  return 0;
}
```
---

All `cmath` functions are here: https://cplusplus.com/reference/cmath/?kw=cmath

these are some samples: 

```c++
sin
asin
cos 
acos
tan
atan
atan2 // tan(y/x)
cosh
acosh
sinh
asinh
exp 
log // natural logatirhm (ln)
log10
modf // break into fractional and integral parts 
pow
sqrt 
cbrt //cubic root 
erf // error function 
tgamma // gamma function 
ceil 
floor 
nan // generate quiet NaN 
fmax // maximum value 
fmin // min value 
fabs // abs value 
isnan // is Not-A-Number 
```

---


```c++
#include <iostream>
#include <cmath>
int main(){
    double a; 
    double b; 
    double c; 
    std::cout<<"Enter side A: ";
    std::cin>>a; 
    std::cout<<"Enter Side B: "; 
    std::cin>>b;
    a = pow(a,2);
    b = pow(b,2);
    c = sqrt(a + b);
    // c = sqrt(pow(a,2) + pow(b,2)); 
    std::cout<< "side C: "<<c; 
    return 0; 
}
```
---


```c++
#include <iostream>
#include <cmath>
int main(){
    // if statement 
    int age; 
    std::cout<<"Enter your age ";
    std::cin>>age; 
    if(age >= 18 && age < 100){
        std::cout<<"Welcome to the site!"; 
    }
    else if(age<0){
        std::cout<<"You have not been born yet";
    }
    else if(age >= 100){
        std::cout<<"You are too old to enter this site"; 
    }
    else{
        std::cout<<"you are not old enough to enter!"; 
    }

    return 0; 
}
```

---


```c++

#include <iostream>
#include <cmath>
int main(){
    // switch = lternative to using many "else if" statements compare one value against matching cases 
    int month; 
    std::cout<<"Enter the month (1 - 12): "; 
    std::cin>> month; 
    switch(month){
        case 1: 
            std::cout<<"It is January"; 
            break;
        case 2: 
            std::cout<<"It is February"; 
            break;        
        case 3: 
            std::cout<<"It is March"; 
            break; 
        case 4: 
            std::cout<<"It is April"; 
            break; 
        case 5: 
            std::cout<<"It is May"; 
            break; 
        case 6: 
            std::cout<<"It is June"; 
            break; 
        case 7: 
            std::cout<<"It is July"; 
            break; 
        case 8: 
            std::cout<<"It is August"; 
            break; 
        case 9: 
            std::cout<<"It is September"; 
            break; 
        case 10: 
            std::cout<<"It is October"; 
            break; 
        case 11: 
            std::cout<<"It is November"; 
            break; 
        case 12: 
            std::cout<<"It is December"; 
            break; 
        default: 
            std::cout<<"Please enter in only numbers (1 - 12)"; 
    }

    return 0; 
}
```


---


```c++
#include <iostream>
#include <cmath>
int main(){
    char grade; 
    std::cout<<"what letter grade? "; 
    std::cin>> grade;
    switch(grade){
        case 'A':
            std::cout<<"You did great";
            break; 
        case 'B': 
            std::cout<<"You did good";
            break; 
        case 'C':
            std::cout<<"You did okay";
            break; 
        case 'D':
            std::cout<<"You did not good";
            break; 
        case 'F':
            std::cout<<"You Faild";
            break; 
        default: 
            std::cout<<"Please only enter in a letter grade (A - F)";
    }

    return 0; 
}
```


---


```c++

#include <iostream>
#include <cmath>
int main(){
    char op; 
    double num1;
    double num2; 
    double result; 
    std::cout<<"****** Calculator ******\n"; 

    std::cout<<"Enter either (+ - * /)";
    std::cin>>op;

    std::cout<<"Enter #1: "; 
    std::cin>>num1;

    std::cout<<"Enter #2: "; 
    std::cin>>num2;

    switch(op){
        case '+':
            result = num1 + num2; 
            std::cout<<"Result: "<<result<<'\n';
            break; 
        case '-':
            result = num1 - num2; 
            std::cout<<"Result: "<<result<<'\n';
            break;    
        case '*':
            result = num1 * num2; 
            std::cout<<"Result: "<<result<<'\n';
            break; 
        case '/':
            result = num1 / num2; 
            std::cout<<"Result: "<<result<<'\n';
            break; 
        default:
            std::cout<<"That wasn't a valid operator\n";

    }

    std::cout<<"************************"; 
    return 0; 
}
```

---


```c++

#include <iostream>
#include <cmath>
int main(){
    // ternary operator '?'  :  replacement to an if/else statement 
    // condition ? expression1 : expression2; 

    int grade = 75; 
    
    if(grade >= 60){
        std::cout<<"You pass";
    }
    else{
        std::cout<<"You fail";
    }
    // now instead of this if/else, we use ternary condition: 
    grade >= 60 ? std::cout<<"You pass" : std::cout<<"you fail"; 

    int number = 9; 
    number % 2 == 1 ? std::cout<<"Odd" : std::cout<<"Even"; 
    // or you can write: 
    number % 2 ? std::cout<<"Odd" : std::cout<<"Even"; 

    bool hungry = true; 
    hungry ? std::cout<<"you are hungry" : std::cout<<"You are full"; 
    // or you can write: 
    std::cout << (hungry ? "You are hungry" : "You are full"); 

    return 0; 
}
```


---


### FizzBuzz

```c++
#include <iostream>

int main() {
    for (int i = 1; i <= 100; ++i) {
        if (i % 3 == 0 && i % 5 == 0)
            std::cout << "FizzBuzz\n";
        else if (i % 3 == 0)
            std::cout << "Fizz\n";
        else if (i % 5 == 0)
            std::cout << "Buzz\n";
        else
            std::cout << i << "\n";
    }
    return 0;
}

```

---


```c++
#include <iostream>

int main() {
    
    // && = check if two conditions are true 
    // || = check if at least one of two conditions is true 
    // ! = reverses the logical state of its operand (if(!x) means if it's not x)

    int temp; 
    std::cout<<"Enter the temperature: ";
    std::cin>>temp; 

    if(temp > 0 && temp < 30){
        std::cout << "the temperature is good"; 
    }
    else{
        std::cout<<"The temperature is bad"; 
    }


    if(temp <= 0 || temp >= 30){
        std::cout << "the temperature is bad"; 
    }
    else{
        std::cout<<"The temperature is good"; 
    }


    bool sunny;
    if(sunny == true){
        std::cout<<"It is sunny outside";
    }
    else{
        std::cout<<"It is cloudy outside"; 
    }

    if(!sunny){
        std::cout<<"It is cloudy outside";
    }
    else{
        std::cout<<"It is sunny outside"; 
    }

    return 0;
}
```

---

```c++
#include <iostream>

int main() {
    
    double temp; 
    char unit; 
    std::cout<<"******* Temperature Conversion *******\n";

    std::cout<<"F = Fahrenheit\n"; 
    std::cout<<"C = Celsius\n";
    std::cout<<"what unit you like to convert to?"; 
    std::cin>>unit;

    if(unit == 'F' || unit == 'f'){
        std::cout<<"Enter the temperature in Celcius: ";
        std::cin>>temp; 
        temp = (1.8 * temp) + 32.0;
        std::cout<<"Temperature is: "<<temp<<"F\n";
    }
    else if(unit == 'C' || unit == 'c'){
        std::cout<<"Enter the temperature in Fahrenheit: ";
        std::cin>>temp; 
        temp = (temp - 32)/1.8; 
        std::cout<<"Temperature is: "<<temp<<"C\n";
    }
    else{
        std::cout<<"Please enter in only C or F\n";
    }

    std::cout<<"**************************************";

    return 0;
}
```

---

```c++
#include <iostream>

int main(){
    std::string name; 
    std::cout<<"Enter your name";
    std::getline(std::cin, name);
    
    if(name.length() > 12){
        std::cout<<"your name can't be over 12 characters";
    }
    else{
        std::cout<<"welcome "<<name;
    }

    if(name.empty()){
        std::cout<<"You didn't enter your name";
    }
    else{ 
        std::cout<<"Hello"<<name;
    }

    name.clear();
    std::cout<<"Hello"<< name;

    name.append("@gmail.com");
    std::cout<<"your username is now "<<name;

    std::cout<<name.at(0); 
    // at(0) means the character in '0' position of that name 

    name.insert(0,"@"); 
    // adding a character in a certain position
    std::cout<<name;

    std::cout<<name.find(''); // find position of ' ' (space)

    name.erase(0,3); // erase first character until the third one
    std::cout<<name;

    std::string S; 
    S.length();
    S.empty(); 
    S.clear(); 
    S.append("asasa"); 
    S.at(0);
    S.insert(3,"h"); 
    S.append("@yahoo.com"); 
    S.find(' '); 
    S.erase(0,2);


    return 0;
}
```

---


### Star Triangle Output 

```c++
int main() {
    int size = 5; 
    for(int i = 1; i <= size; i++){
        for(int j = 1; j <= size - i; j++){
                std::cout<<" "; 
        }
        for(int k = 1; k <= 2*i-1; k++){
            std::cout<<"*";
        }
        std::cout<<"\n";
    }

    // * * * * * 
    // * * * *
    // * * *
    // * *
    // *

    // -----------

    for(int i = 0; i <size;i++){
        for(int j = 0; j <= i; j++){
            std::cout<<"* ";
        }
        std::cout<<'\n';
    }
    
    // *
    // * *
    // * * *
    // * * * *
    // * * * * * 

    // ------------

    for(int i = 0; i < size; i++){
        for(int j = 0; j < size; j++){
            std::cout<<" "; 
        }
        for(int k = 0; k <= i; k++){
            std::cout<<"* "; 
        }
        std::cout<<'\n'; 
    }
    
    //     *
    //    * *
    //   * * *
    //  * * * *
    // * * * * *

    // -------------

    int i = 0; 
    while(i < size*2){
        if(i < size){
            for(int j = 0; j < size - i; j++){
                std::cout<<" "; 
            }
            for(int k = 0; k<= i; k++){
                std::cout<<"* "; 
            }
            std::cout<<'\n'; 
        }
        else if(i >= size){
            for(int q = 0; q <= i - size; q++){
                std::cout<<" "; 
            }
            for(int p = size; p > i - size; p--){
                std::cout<<"* "; 
            }
            std::cout<<'\n'; 
        }
        i++; 
    }

    //     * 
    //    * * 
    //   * * * 
    //  * * * * 
    // * * * * * 
    // * * * * * 
    //  * * * * 
    //   * * * 
    //    * * 
    //     * 



    return 0; 
}
```

---

```c++
#include <iostream>

int main() {
    std::string name; 
    while(name.empty()){
        std::cout<<"enter your name: ";
        std::getline(std::cin,name);
    }
    std::cout<<"Hello "<<name;

    return 0;
}
```
---


```c++
#include <iostream>

int main() {
    
    // do while loop = do some block of code first, then repeat again if condition is true 

    int number; 

    std::cout<<"enter a positive number #: "; 
    std::cin>>number;

    while(number < 0){
        std::cout<<"enter a positive number #: "; 
        std::cin>>number; 
    }
    std::cout<<"The number is "<<number; 

    // instead of writing this code we can write by using do-while loop 

    do{
        std::cout<<"enter a positive number #: "; 
        std::cin>>number;  
    }while(number< 0);

    std::cout<<"The number is "<<number; 

    return 0;
}
```
---

```c++
#include <iostream>

int main() {
    
    for(int i = 1; i <= 3; i++){
        std::cout<<i<<'\n';
    }
    std::cout<<"Hi\n";

    for(int i = 0; i < 5; i+=3){
        std::cout<<i<<'\n';
    }
    std::cout<<"Hi\n";

    return 0;
}
```
 
---

```c++
#include <iostream>

int main() {
    
    // break and continue (skip the current iteration)
    for(int i = 1; i<=20; i++){
        if(i == 13){
            break;
        }
        if(i == 15){
            continue;
        }
        std::cout<< i << '\n';
    }

    return 0;
}
```
---


```c++
#include <iostream>

int main() {
    
    int rows; 
    int columns; 
    char symbol; 

    std::cout<<"How many rows?: ";
    std::cin>>rows; 
    std::cout<<"How many columns?: ";
    std::cin>>columns;     
    std::cout<<"Enter a symbol to use: ";
    std::cin>>symbol; 

    for(int i = 1; i<=rows; i++){
        for(int j = 1; j<=columns; j++){
            std::cout<<symbol;
        }
        std::cout<<'\n';
    }

    return 0;
}
```

---

```c++
#include <iostream>

int main() {
    
    // pseudo-random = Not truly random (but close)
    srand(time(NULL));
    int num = rand();
    std::cout<<num; 

    int num = (rand() % 6) + 1; // random numbers from 1 to 6
    std::cout<<num;     

    return 0;
}
```
---

```c++
#include <iostream>
#include <ctime>

int main() {
    
    // random event
    srand(time(0)); // using current time as a random seed 
    int randNum = rand() % 5 + 1; // random number between 1 and 5

    switch(randNum){
        case 1: std::cout<<"you win a bumper sticker\n"; 
                break;
        case 2: std::cout<<"you win a bumper T-shirt\n"; 
                break;
        case 3: std::cout<<"you win a bumper free lunch\n"; 
                break;
        case 4: std::cout<<"you win a bumper gift card\n"; 
                break;
        case 5: std::cout<<"you win a concert ticket\n"; 
                break;
    }

    return 0;
}

---

```c++
#include <iostream>

int main(){

    int num; 
    int guess; 
    int tries; 

    srand(time(NULL));
    num = (rand() % 100) + 1;
    std::cout<<"***** Number Guessing Game *****\n">>

    do{
        std::cout<<"enter a guess between (1-100): "; 
        std::cin>>guess;
        tries++;  
        if(guess > num){
            std::cout<<"too high\n";
        }
        else if(guess < num){
            std::cout<<"Too low\n";  
        }
        else{
            std::cout<<"CORRECT! # of tries: "<<tries<<'\n';
        }
    }while(guess != num);

    std::cout<<"**************************************";

    return 0; 
}
```

---


```c++
#include <iostream>

// function 
void happyBirthday(){
    std::cout<<"Happy Birthday to you!\n";
    std::cout<<"Happy Birthday to you!\n";
    std::cout<<"Happy Birthday to you!\n";
    std::cout<<"Happy Birthday to you!\n";
}

int main(){
    
    happyBirthday();

    return 0; 
}
```
---
### We can also define the function after everything but we must write `void function` at the beginning: 


```c++
#include <iostream>

void happyBirthday(); 

int main(){
    
    happyBirthday();

    return 0; 
}

void happyBirthday(){
    std::cout<<"Happy Birthday to you!\n";
    std::cout<<"Happy Birthday to you!\n";
    std::cout<<"Happy Birthday to you!\n";
    std::cout<<"Happy Birthday to you!\n";
}
```
---

```c++
#include <iostream>

void happyBirthday(std:string name, int age); 

int main(){

    std::string name = "Bro";
    int age = 27; 

    happyBirthday(name,age);

    return 0; 
}

void happyBirthday(std:string name, int age){
    std::cout<<"Happy Birthday to" << name <<'!\n';
    std::cout<<"Happy Birthday to" << name <<'!\n';
    std::cout<<"Happy Birthday dear" << name <<'!\n';
    std::cout<<"Happy Birthday to" << name <<'!\n';
    std::cout<<"You are " << age << " years old!\n";
}
```
---


```c++
#include <iostream>

double square(double length);

int main(){
    // return = return a value back to the spot where you called the encompassing function 

    // the keyword 'void' must be matched to the output datatype of our defined function. 

    // If output is double, then instead of void we must write double. 

    double length = 5.0; 
    double area = square(length);
    std::cout<<"Area" << area << "cm^2\n";

    return 0; 
}

double square(double length){
    return length * length;  
}
```
---

```c++
#include <iostream>

double square(double length);
double cube(double length); 

int main(){

    double length = 5.0; 
    double area = square(length);
    double volume = cube(length); 
    std::cout<<"Area " << area << "cm^2\n";
    std::cout<<"Volume " << volume << "cm^3\n"; 

    return 0; 
}

double square(double length){
    return length * length;  
}

double cube(double length){
    return length * length * length; 
}

```
---

```c++
#include <iostream>

std::string concatStrings(std::string string1, std::string string2); 

int main(){
    
    std::string firstName = "Bro"; 
    std::string lastName = "Code"; 
    std::string fullName = concatString(firstName, lastName); 

    std::cout<<"Hello "<<fullName; 

    return 0; 
}

std::string concatStrings(std::string string1, std::string string2){
    return string1 + " " + string2; 
}
```
---

### Overloaded functions: functions with same name and different sets of input parameters: 

```c++
#include <iostream>

// we can have a function that has no inputs, or we can give it inputs as well 

void bakePizza();
void bakePizza(std::string topping1);

int main(){
    
    bakePizza("pepperoni","mushrooms"); 

    return 0; 
}
void bakePizza(){
    std::cout<<"Here is your pizza!\n";
}
void bakePizza(std::string topping1){
    std::cout<< "Here is your "<<topping1 << "pizza\n"; 
}
void bakePizza(std::string topping1, std::string topping2){
    std::cout<< "Here is your "<<topping1<< " and "<<topping2<< " pizza\n"; 
}
```
---

```c++
#include <iostream>

int myNum = 3; 
void printNum();

int main(){
    
    // Local variables = declared inside a function or block {}
    // Global variables = declared outside of all functions 
    int myNum = 1; 
    printNum(); 
    std::cout<<::myNum<<'\n'; 
    // ::myNum means it uses global version of myNum 

    return 0; 
}
void printNum(){
    int myNum = 2; 
    std::cout<<myNum; 
}
```
---

```c++
#include <iostream>
#include <iomanip> // setting some precision for floating numbers 
// banking program 
void showBalance(double balance);
double deposit(); 
double withdraw(double balance);

int main(){
    
    double balance = 0; 
    int choice = 0; 
    do{
        std::cout<<"********************"; 
        std::cout<<"Enter your choice:\n";
        std::cout<<"********************"; 
        std::cout<<"1. Show Balance\n";
        std::cout<<"2. Deposit Money\n"; 
        std::cout<<"3. Withdraw Money\n"; 
        std::cout<<"4. Exit\n"; 
        std::cin>> choice;

        std::cin.clear(); // reseting any error flags
        // it's for when cin is not a number from 1 to 4
        fflush(stdin);

        switch(choice){
            case 1: ShowBalance(balance);
                    break; 
            case 2: balance += deposit();
                    ShowBalance(balance);
                    break; 
            case 3: balance -= withdraw(balance); 
                    ShowBalance(balance);
                    break; 
            case 4: std::cout<<"Thanks for visiting!"; 
                    break; 
            default: std::cout<<"Invalid choice"; 
        }
    }while(choice != 4);

    return 0; 
}

void showBalance(double balance){
    std::cout<<"Your balance is: $"<< std::setprecision(2)<< std::fixed <<balance<<'\n'; 
    // showing  2 decimal places for precision 
}

double deposit(){
    double amount = 0; 
    std::cout<<"Enter amount to be deposited: "; 
    std::cin>>amount; 
    if(amount > 0){
        return amount; 
    }
    else{
        std::cout<<"That's not a valid amount: "; 
        return 0; 
    }
}

double withdraw(double balance){
    double amount = 0; 
    std::cout<<"Enter amount to be withdrawn: ";
    std::cin>>amount; 
    if(amount > balance){
        std::cout<<"Insufficient funds\n"; 
        return 0; 
    }
    else if(amount < 0){
        std::cout<<"That's not a valid amount\n";
        return 0; 
    }
    else{
        return amount; 
    }
}
```

---


### rock paper scissors game 
```c++

#include <iostream>
#include <ctime>

char getUserChoice(); 
char getComputerChoice(); 
void showChoice(char choice);
void chooseWinner(char player,char computer); 

int main(){
    
    char player; 
    char computer;
    player = getUserChoice(); 
    std::cout<<"Your choice: "; 
    showChoice(player);
    computer = getComputerChoice();
    std::cout<<"Computer's choice: ";
    showChoice(computer);
    chooseWinner(player,computer);

    return 0; 
}

char getUserChoice(){

    char player; 
    std::cout<< "Rock-Paper-Scissors Game!\n";

    do{
        std::cout<< "Choose one of the following options:\n";
        std::cout<< "*************************\n";
        std::cout<<"'r' for rock\n";
        std::cout<<"'p' for paper\n";
        std::cout<<"'s' for scissors\n";
        std::cin>>player;
    }while(player != 'r' && player != 'p' && player != 's'); 

    return player; 
}


char getComputerChoice(){
    
    srand(time(0)); 
    int num = rand() % 3 + 1; // 1,2,3
    switch(num){
        case 1: return 'r'; // rock
        case 2: return 'p'; // paper
        case 3: return 's'; // scissors
    }

    return 0;
} 

void showChoice(char choice){

    switch(choice){
        case 'r':
            std::cout<< "Rock\n";
            break;
        case 'p':
            std::cout<< "Paper\n";
            break;
        case 's':
            std::cout<< "Scissors\n";
            break;
    }
}

void chooseWinner(char player,char computer){
    switch(player){
        case 'r': 
            if(computer == 'r'){
                std::cout<< "It's a tie!\n";
            }
            else if(computer == 'p'){
                std::cout<< "You lose!\n";
            }
            else{
                std::cout<< "You win!\n";
            }
            break; 
        case 'p': 
            if(computer == 'r'){
                std::cout<< "You win!\n";
            }
            else if(computer == 'p'){
                std::cout<< "It's a tie!\n";
            }
            else{
                std::cout<< "You lose!\n";
            }
            break;
        case 's':
            if(computer == 'r'){
                std::cout<< "You lose!\n";
            }
            else if(computer == 'p'){
                std::cout<< "You win!\n";
            }
            else{
                std::cout<< "It's a tie!\n";
            }
            break;
    }
} 
```

---


```c++
#include <iostream>

// Array = it's a data structure that can hold multiple values 
// Values are accessed by an index number 
// kind of like a variable that holds multiple values 

int main(){
    
    std::string cars[] = {"Corvette","Mustang","Camery"}; // array of strings

    std::cout << cars[0]<<'\n'; // c++ starts with 0 index  
    std::cout << cars[1]<<'\n'; 
    std::cout << cars[2]<<'\n';
    
    return 0; 
}
```

---


```c++
#include <iostream>

int main(){
    
    double prices[] = {100, 200, 300, 400, 500};
    std::cout<< prices[0]<<'\n';
    std::cout<< prices[1]<<'\n';
    std::cout<< prices[2]<<'\n';
    std::cout<< prices[3]<<'\n';
    std::cout<< prices[4]<<'\n'; 

    return 0; 
}
```

---

```c++
#include <iostream>

// sizeof() = determine the size in bytes of a: 
// 1. variable
// 2. data type
// 3. object
// 4. class
// etc

int main(){
    
    double gpa = 2.5; 
    std::cout<<sizeof(gpa)<<"bytes\n"; // 8 bytes

    std::string name = "Bro";
    std::cout<<sizeof(name)<<"bytes\n"; // 32 bytes

    char grade = 'A';
    std::cout<<sizeof(grade)<<"bytes\n"; // 1 byte

    bool student = true;
    std::cout<<sizeof(student)<<"bytes\n"; // 1 byte

    char grades[] = {'A', 'B', 'C', 'D', 'E'};
    std::cout<<sizeof(grades)<<"bytes\n"; // 5 bytes

    std::string students[] = {"Bro", "Sister", "Mother", "Father"};
    std::cout<<sizeof(students)/sizeof(std::string)<<"elements\n"; // 4 elements


    return 0; 
}
```

---


```c++
#include <iostream>

int main(){

    std::string students[] = {"spongebob", "patrick", "sandy"}; 
    std::cout<<students[0]; 

    for(int i = 0; i < sizeof(students)/sizeof(std::string); i++){
        std::cout<<students[i]<<'\n';
    }

    char grades[] = {'A', 'B', 'C', 'D', 'F'};
    for(int i = 0; i < sizeof(grades)/sizeof(char); i++){
        std::cout<<grades[i]<<'\n';
    }
    
    return 0; 
}
```

---


```c++
#include <iostream>

// foreach loop = loop that eases the traversal over an iterable dataset 

int main(){

    std::string students[] = {"John", "Jane", "Doe"};
    for(std::string student : students){
        std::cout << student << std::endl;
    }

    int grades[] = {90, 85, 78};
    for(int grade : grades){
        std::cout << grade << std::endl;
    }

    return 0; 
}
```

---

```c++
#include <iostream>

// passing array to a function 
double getTotal(double prices[],int size);

int main(){

    double prices[] = {100.01, 200.5, 300.33, 400.1, 500};
    int size = sizeof(prices)/sizeof(prices[0]);
    double total = getTotal(prices,size); 

    std::cout<<"$"<<total;

    return 0; 
}
double getTotal(double prices[],int size){

    double total = 0;
    for(int i = 0; i < size;i++){
        total += prices[i]; 
    } 

    return total; 
}
```

---

```c++
#include <iostream>

int searchArray(std::string array[], int size, std::string element);

int main(){

    std::string foods[] = {"pizza","hamberger","hotdog","sushi","tacos","salad","steak","chicken","fish","pasta"};
    int size = sizeof(foods) / sizeof(foods[0]);
    int index; 
    std::string myFood;  

    std::cout << "Enter element to search for: "<<'\n';
    std::cin >> myFood;
    index = searchArray(foods, size, myFood);

    if(index != -1){
        std::cout<<myFood<<"is at index" << index; 
    }
    else{
        std::cout<<myFood<<"not found in array";
    }

    return 0; 
}

int searchArray(std::string array[], int size, std::string element){

    for(int i = 0; i < size; i++){
        if(array[i] == element){
            return i;
        }
    }

    return -1; // Element not found
}
```


---


```c++
#include <iostream>

// sorting an array 
// for example we have 10,4,5,7,3,2,6,8,9,1, and we wanna sort it 
// this is bouble sort 

void sort(int array[], int size);

int main(){

    int array[] = {10,1,9,2,8,3,7,4,6,5};
    int size = sizeof(array)/sizeof(array[0]);
    sort(array,size); 

    for(int element : array){
        std::cout<<element<<" "; 
    }

    return 0; 
}

void sort(int array[], int size){

    int temp; 
    for(int i = 0; i < size - 1; i++){
        for(int j = 0; j < size - i - 1; j++){
            if(array[j] > array[j + 1]){  // if we use if(array[j] < array[j + 1]), it'll be descending order
                temp = array[j];
                array[j] = array[j + 1];
                array[j+1] = temp; 
            }
        }
    }
}

// size = 4; 
// i = 0 -> j = 0 to 3        i = 1; j = 0 to 2       i = 2; j = 0 to 1       i = 3; j = 0 to 0 

// i = 0 -> j = 0 -> if a[1] > a[0] -> ....
//          j = 1 -> if a[2] > a[1] -> ....
//          j = 2 -> if a[3] > a[2] -> ....
//          j = 3 -> if a[4] > a[3] -> .... 

// i = 1 -> j = 0 -> if a[1] > a[0] -> .... 
//          j = 1 -> if a[2] > a[1] -> ....
//          j = 2 -> if a[3] > a[2] -> ....

// i = 2 -> j = 0 -> if a[1] > a[0] -> .... 
//          j = 1 -> if a[2] > a[1] -> ....

// i = 3 -> j = 0 -> if a[1] > a[0] -> .... 

```

---



```c++

#include <iostream>

// fill() = fills a range of elements with a specific value
// fill(begin, end, value)

int main(){

    std::string foods[10] = {"pizza", "pizza", "pizza", "pizza", "pizza",
                             "pizza", "pizza", "pizza", "pizza", "pizza"};
    for(std::string food: foods){
        std::cout << food << std::endl;
    }
    std::cout<<"------------------------" << std::endl;
    // instead of doing this, we can use fill function
    const int size = 100; 
    std::string Foods[size]; 
    fill(Foods, Foods + size, "pizza");
    for(std::string food: Foods){
        std::cout << food << std::endl;
    }             
    std::cout<<"------------------------" << std::endl;
    // or it could be first half filled with pizza and second half filled with burger
    std::string Foods2[size];
    fill(Foods2, Foods2 + size/2, "pizza");
    fill(Foods2 + size/2, Foods2 + size, "burger");
    for(std::string food: Foods2){
        std::cout << food << std::endl;
    }
    std::cout<<"------------------------" << std::endl;
    // or it could be first third filled with pizza and second third filled with burger and third third filled with sandwich
    const int size2 = 99; 
    std::string Foods3[size2];
    fill(Foods3, Foods3 + size2/3, "pizza");
    fill(Foods3 + size2/3, Foods3 + 2*size2/3, "burger");
    fill(Foods3 + 2*size2/3, Foods3 + size2, "sandwich");
    for(std::string food: Foods3){
        std::cout << food << std::endl;
    }

    return 0; 
}
```

---

```c++
#include <iostream>

int main(){

    std::string foods[5]; // size of array is static structure 
    int size = sizeof(foods)/sizeof(foods[0]);
    std::string temp; 
    for(int i = 0; i < size; i++){
        std::cout << "Enter food you like or 'q' to quit" << i + 1<< ": ";
        std::getline(std::cin, temp); // getline is for having 'space' in typing 
        if(temp == "q"){
            break; 
        }
        else{
            foods[i] = temp; // store the food in the array 
        }
    }
    std::cout << "You like the folling food: " << std::endl;
    for(int i = 0; !foods[i].empty(); i++){
        std::cout << foods[i] << std::endl;
    }

    return 0; 
}
```

---


```c++
#include <iostream>

int main(){

    std::string cars[][3] = {{"Mustang", "Escape", "F-150"},
                            {"Corvette", "Equinaox", "Silverado"},
                            {"Challenger", "Durango", "Ram 1500"}};
   
    int rows = sizeof(cars) / sizeof(cars[0]);
    int cols = sizeof(cars[0]) / sizeof(cars[0][0]);
    for(int i = 0; i < rows; i++){
        for(int j = 0; j < cols; j++){
            std::cout << cars[i][j] << " ";
        }
        std::cout << std::endl;
    }

    return 0; 
}
```
---

```c++
#include <iostream>

int main(){

    std::string questions[] = {"1. What year was c++ created? ",
                               "2. who invented c++? ",
                               "3. what is the predecessor of c++? ",
                               "4. Is the earth flat? "};

    std::string options[][4] = {{"A. 1969","B. 1975","C. 1985","D. 1989"},
                               {"A. Guido van Rossum","B. Bjarne Stroustrup","C. John Carmack","Mark Zuckerburg"},
                               {"A. C","B. C+","C. C--","D. B++"},
                               {"A. Yes","B. No","C. Maybe","D. I don't know"}};

    char answerKey[] = {'C','B','A','B'};

    int size = sizeof(questions)/sizeof(questions[0]);
    char guess; 
    int score;

    for(int i = 0; i < size; i++){

        std::cout<<"************************\n";
        std::cout << questions[i] << std::endl;
        std::cout<<"************************\n";

        for(int j = 0; j < sizeof(options[i])/sizeof(options[i][0]); j++){
            std::cout << options[i][j] << std::endl;
        }
        std::cout << "Enter your answer: ";
        std::cin >> guess;
        guess = toupper(guess); // geuss must be captial letter 

        if(guess == answerKey[i]){
            score++;
            std::cout << "Correct!" << std::endl;
        }
        else{
            std::cout << "Wrong! The correct answer is " << answerKey[i] << std::endl;
        }
    }

    std::cout<<"*******************************\n";
    std::cout<<"*           Results           *\n";
    std::cout<<"*******************************\n";

    std::cout<<"Correct Guesses: "<<score<<std::endl;
    std::cout<<"# of Questions: "<< size<<std::endl;
    std::cout<<"Your Score: "<< (score/(double)size)*100 << "%" << std::endl;


    return 0; 
}
```

---

```c++

#include <iostream>

int main(){

    // Memory address = a location in memory where data is stored 
    // a memory address can accessed with & (address of operator)

    std::string name = "Bro"; 
    int age = 21; 
    bool student = true; 

    std::cout<< &name <<'\n'; // address of name (0x16bd1ed10) everytime we run the program, it will change
    //if we convert the address from hexadecimal to decimal, it is for example: 814066169344
    std::cout<< &age <<'\n'; // address of age
    std::cout<< &student <<'\n'; // address of student

    // for string, we allocate 4 bytes of memory 
    // for int, we allocate 4 bytes of memory
    // for bool, we allocate 1 byte of memory


    return 0; 
}
```

---

```c++
#include <iostream>

void swap(std::string &x, std::string &y);

int main(){

    // pass by value and pass by referene 
    std::string x = "Kool-Aid"; 
    std::string y = "Water"; 

    swap(x,y); // pass by reference 

    std::cout<<"X: "<<x<<std::endl;
    std::cout<<"Y: "<<y<<std::endl;


    return 0; 
}

void swap(std::string &x, std::string &y){ // &x and &y are pass by reference 
    // if we use only x,y, this will be pass by value and 
    // since we are using a function, x,y are copy of original x,y and code won't work 
    std::string temp;  
    temp = x; 
    x = y; 
    y = temp; 
}
```
---


```c++

#include <iostream>

void printInfo(const std::string name, const int age);

int main(){

    // const parameter = parameter that is effectively read only. 
    // code is more secure and conveys intent useful for references and pointers 
    // we can also set the reference to be constant (i.e., &name, &age)
    std::string name = "Bro"; 
    int age = 21; 
    printInfo(name,age); 

    return 0; 
}

void printInfo(const std::string name, const int age){
    
    std::cout<<name<<'\n';
    std::cout<<age<<'\n';
}
```

---

We want to evalueate weather a credit card is valid or not. 

### Luhn algorithm: 

1. Double every second digit from right to left 
    If doubled number is 2 digits, split them 

2. Add all single digis from step 1

3. Add all odd numbered digits from right to left 

4. Sum results from steps 2 & 3

5. If step 4 is divisble by 10, # is valid 

For example: 

6011000990139424

6011    0009    9013    9424

6 1     0 0     9 1     9 2

12 2    0 0     18 2    18 4

1 2 2   0 0     1 8 2   1 8 4

sum1 = 29 

adding all odd numbered digits (pisitions) from right to left (from original numbers) = 

0 1     0 9     0 3     4 4

sum2 = 1 + 9 + 3 + 4 + 4 = 21

sum1 + sum2 = 29 + 21 = 50 

step 5: 50 % 10 = valid

---

```c++
#include <iostream>

int getDigit(const int number); 
int sumOddDigits(const std::string cardNumber);
int sumEvenDigits(const std::string cardNumber);

int main(){

    std::string cardNumber; 
    int result = 0; 
    std::cout << "Enter the credit card number: ";
    std::cin >> cardNumber;
    result = sumEvenDigits(cardNumber) + sumOddDigits(cardNumber);

    if(result % 10 == 0){
        std::cout<<"Valid Credit Card Number\n";
    }
    else{
        std::cout<<"Invalid Credit Card Number\n";
    }

    return 0; 
}

int getDigit(const int number){
    return number % 10 + (number / 10 % 10); // 18 -> 1 8 -> 1 + 8 = 9
} 

int sumOddDigits(const std::string cardNumber){

    int sum = 0; 
    for(int i = cardNumber.size() - 1; i >= 0; i-=2){
        sum += cardNumber[i] - '0';
    }
    return sum; 
    
}

int sumEvenDigits(const std::string cardNumber){
    int sum = 0; 
    for(int i = cardNumber.size() - 2; i >= 0; i-=2){
        sum += getDigit((cardNumber[i] - '0')*2);
    }
    return sum; 
}
```

---

## Pointers: 

```c++

#include <iostream>

// pointer = variable that stores a momery address of another variable 
// sometimes it's easier to work with an address than the variable itself

// & address-of operator
// * dereference operator

int main(){

    std::string name = "Bro"; 
    std::string *pName = &name; // pointer to name (pName = pointer name)
    std::cout << pName << std::endl; 

    int age = 27; 
    int *pAge = &age; // pointer to age
    std::cout << pAge << std::endl;

    std::string freePizzas[5] = {"pepperoni", "cheese", "veggie", "sausage", "chicken"}; 
    // the array itself (freePizzas) is already a memory address 
    std::string *pFreePizzas = freePizzas; // pointer to freePizzas
    std::cout << pFreePizzas << std::endl;

    return 0; 
}

```

---

```c++
#include <iostream>

// Null value = a special value that means something has no value 
// when a pointer is holding a null value, it means it is not pointing to any object

// nullptr = keyword represents a null pointer literal 

// nullptrs are helpful when determining if an address was successfully assigned to a pointer 

// when using pointers, be carefull that your code isn't derefrencing null or pointing to free memory
// this'll cause undefined behavior 

int main(){

    int *pointer = nullptr; 
    int x = 123; 
    pointer = &x; 

    if(pointer == nullptr){
        std::cout << "Pointer is null" << std::endl; 
    } else {
        std::cout << "address was assigned \n";
        std::cout << *pointer;
    }

    return 0; 
}
```

---


## Tic Tac Toe 

it's actually duzz game 

[0]     [1]     [2]

[3]     [4]     [5]

[6]     [7]     [8]




```c++
#include <iostream>
// Tic Tac Toe Game (duzz)
#include <ctime>

void drawBoard(char *spaces); //spaces is 1-dim array that keeps track of all the markers 
void playerMove(char *spaces, char player); //player is either 'X' or 'O'
void computerMove(char *spaces, char player); //computer is either 'X' or 'O'
bool checkWinner(char *spaces, char player, char computer); 
bool checkTie(char *spaces);  // if there is no space alvailable 

int main(){

    char spaces[9] = {' ', ' ', ' ', ' ', ' ', ' ', ' ', ' ', ' '}; // 1-dim array to keep track of the board
    char player = 'X';
    char computer = 'O'; 
    bool running = true; 

    drawBoard(spaces); 

    while(running){ // while running is true 
        playerMove(spaces, player); 
        drawBoard(spaces);
        if(checkWinner(spaces, player, computer)){
            running = false; 
            break; 
        }
        else if(checkTie(spaces)){
            running = false; 
            break;
        }
        computerMove(spaces, computer);
        drawBoard(spaces); 
        if(checkWinner(spaces, player, computer)){
            running = false; 
            break; 
        }
        else if(checkTie(spaces)){
            running = false; 
            break;
        }
    }
    std::cout<<"Thanks for playing! \n";

    return 0; 
}

void drawBoard(char *spaces){
    std::cout<<'\n';
    std::cout<<"     |     |     "<<'\n';
    std::cout<<"  "<<spaces[0]<<"  |  "<<spaces[1]<<"  |  "<<spaces[2]<<"  "<<'\n';
    std::cout<<"_____|_____|_____"<<'\n';
    std::cout<<"     |     |     "<<'\n';
    std::cout<<"  "<<spaces[3]<<"  |  "<<spaces[4]<<"  |  "<<spaces[5]<<"  "<<'\n';
    std::cout<<"_____|_____|_____"<<'\n';
    std::cout<<"     |     |     "<<'\n';
    std::cout<<"  "<<spaces[6]<<"  |  "<<spaces[7]<<"  |  "<<spaces[8]<<"  "<<'\n';
    std::cout<<"     |     |     "<<'\n'; 
    std::cout<<'\n'; 
}

void playerMove(char *spaces, char player){
    int number; 
    do{
        std::cout<<"Enter a number between (1 - 9): ";
        std::cin>>number; 
        number--; // to match the index of the array (starts with 0) 
        if(spaces[number] == ' '){
            spaces[number] = player; 
            break; 
        }
    }while(!number > 0 || !number < 8);

}

void computerMove(char *spaces, char player){
        int number; 
        srand(time(0)); // seed the random number generator
        while(true){
            number = rand() % 9; // generate a random number between 0 and 8
            if(spaces[number] == ' '){
                spaces[number] = player; 
                break; 
            }
        }
}

bool checkWinner(char *spaces, char player, char computer){

    if(spaces[0] != ' ' && spaces[0] == spaces[1] && spaces[1] == spaces[2]){ // if the player occupies the first row: 
        spaces[0] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else if(spaces[3] != ' ' && spaces[3] == spaces[4] && spaces[4] == spaces[5]){ // checking second row: 
        spaces[3] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else if(spaces[6] != ' ' && spaces[6] == spaces[7] && spaces[7] == spaces[8]){ // checking third row: 
        spaces[6] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else if(spaces[0] != ' ' && spaces[0] == spaces[3] && spaces[3] == spaces[6]){ // checking first column:
        spaces[0] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else if(spaces[1] != ' ' && spaces[1] == spaces[4] && spaces[4] == spaces[7]){ // checking second column:
        spaces[1] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else if(spaces[2] != ' ' && spaces[2] == spaces[5] && spaces[5] == spaces[8]){ // checking third column:
        spaces[2] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else if(spaces[0] != ' ' && spaces[0] == spaces[4] && spaces[4] == spaces[8]){ // checking diagonal 
        spaces[0] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else if(spaces[2] != ' ' && spaces[2] == spaces[4] && spaces[4] == spaces[6]){ // checking first column:
        spaces[2] == player ? std::cout<<"You win! \n" : std::cout<<"You Lose! \n";
    }
    else{
        return false; 
    }

    return true; 
} 

bool checkTie(char *spaces){
    for(int i = 0; i < 9; i++){
        if(spaces[i] == ' '){
            return false; 
        }
    }
    std::cout<<"It's a tie! \n";
    return true; 
} 
```

---


## Dynamic Memory 

Memory: 

- Heap

- Stack

- Global/Static 

- Text (code) 

---

### 1. **Heap**

* **Purpose**: Used for **dynamic memory allocation**.
* **Managed by**: The **programmer or runtime**, via functions like `malloc`, `new`, `free`, or `delete`.
* **Lifetime**: Data stays until **explicitly deallocated** or program ends.
* **Example**:

  ```cpp
  int* ptr = new int;  // allocated on the heap
  ```

---

### 2. **Stack**

* **Purpose**: Stores **function call frames**, including:

  * Local variables
  * Function parameters
  * Return addresses
* **Managed by**: **Compiler and CPU** — automatically grows/shrinks as functions are called/returned.
* **Lifetime**: Data is destroyed when the function **returns**.
* **Fast access**, but limited in size.
* **Example**:

  ```cpp
  void foo() {
      int x = 10;  // x lives on the stack
  }
  ```

---

### 3. **Global / Static Segment**

* **Purpose**: Holds:

  * **Global variables**
  * **Static local variables**
  * **Constants** with static duration
* **Lifetime**: Exists **for the entire program runtime**.
* **Example**:

  ```cpp
  int globalVar = 5;  // global
  void bar() {
      static int counter = 0;  // static local
  }
  ```

---

### 4. **Code / Text Segment**

* **Purpose**: Stores the **compiled machine code** (instructions to be executed).
* **Usually read-only**, to prevent accidental modification (or security vulnerabilities).
* **Example**: The instructions for your `main()` or any other functions reside here.

---


```
+---------------------+
|     Code (Text)     |  <- Executable instructions
+---------------------+
|  Global/Static Data |  <- Global/static variables
+---------------------+
|       Heap          |  <- Grows upwards
|    (dynamic alloc)  |
+---------------------+
|       Stack         |  <- Grows downwards
|   (function calls)  |
+---------------------+
```


---


```c++

#include <iostream>

// dynamic memory = memory that is allocated after the program is already compiled and running 
// Use the 'new' operator to allocate memory in the heap rather than the stack 

// Usefull when we don't know how much memory we will need. 
// Makes our programs more flexible, expecially when accepting user input. 

int main(){

    int *pNum = NULL; 
    pNum = new int; // allocate memory for an integer on the heap (pointing to memory location)
    *pNum = 21; 
    std::cout<<"address: "<<pNum<<std::endl; // address of the variable in the heap 
    std::cout<<"value: "<<*pNum<<std::endl; // value of the variable

    // at the end of the program we delete our pointer 
    delete pNum; // free the memory allocated to the pointer
    // we free the memory to avoid memory leaks

    return 0; 
}
```

---



```c++
#include <iostream>

int main(){

    char *pGrades = NULL; 
    int size; 
    std::cout<<"How many grades to enter in? "; 
    std::cin>>size; 
    pGrades = new char[size];  
    for(int i = 0; i<size; i++){
        std::cout<<"Enter grade #"<<i+1<<": "; 
        std::cin>>pGrades[i]; // enter char like A, B, C, F
    }
    for(int i = 0; i<size; i++){
        std::cout<<pGrades[i] <<" ";
    }
    delete[] pGrades;

    return 0; 
}
```

---


### Recursion

```c++

#include <iostream>

// recursion = a programming technique where a function invokes itself from within 

// Breaking a complex concept into a repeatable single steps 

// (iterative vs recursive)

// advantages = less code and is cleaner 
// useful for sorting and searching algorithms 

// disadvantages = uses more memory, slower 

void walk(int steps);

void walk2(int steps); 

int main(){

    walk(5); // this is iterative case

    std::cout<<"------------------------\n";

    walk2(5); // this is recursive case

    return 0; 
}

void walk(int steps){
    for(int i = 0; i < steps; i++){ // this is iterative case 
        std::cout<<"Just you take a step!\n"; 
    }
}

void walk2(int steps){
    if(steps > 0){
        std::cout<<"Just you take a step!\n"; 
        walk2(steps - 1); // this is recursive case (using more memory and processing time)
    } else {
        std::cout<<"You are done walking!\n";
    }
}
```

---


```c++
#include <iostream>

// factorial function iteratively and recursively 

int factorial1(int num); // iterative
int factorail2(int num); // recursive

int main(){

    std::cout<<factorial1(5)<<std::endl; 

    std::cout<<factorail2(5);

    return 0; 
}

int factorial1(int num){
    int result = 1; 
    for(int i = 1; i <= num; i++){
        result *= i; 
    }
    return result;
}

int factorail2(int num){
    if(num > 1){
        return num * factorail2(num - 1);  
    }
    else{
        return 1; 
    }
}
```
---

## Some Recursive Function Examples: 


### **Fibonacci Numbers**

Computes `F(n) = F(n-1) + F(n-2)` with `F(0) = 0`, `F(1) = 1`

```cpp
int fibonacci(int n) {
    if (n <= 1) return n;               // Base cases
    return fibonacci(n - 1) + fibonacci(n - 2);  // Recursive case
}
```

---

### **Sum of First N Natural Numbers**

```cpp
int sum(int n) {
    if (n == 0) return 0;           // Base case
    return n + sum(n - 1);          // Recursive case
}
```

---


### **Print Numbers from N to 1**

```cpp
void printReverse(int n) {
    if (n == 0) return;             // Base case
    std::cout << n << " ";
    printReverse(n - 1);            // Recursive case
}
```
---

### **Power Function: a^b**

```cpp
int power(int a, int b) {
    if (b == 0) return 1;           // Base case: a^0 = 1
    return a * power(a, b - 1);     // Recursive case
}
```

---

### **Palindrome Check (String)**

```cpp
#include <iostream>
#include <string>

bool isPalindrome(const std::string& str, int start, int end){
    if (start >= end) return true;
    if (str[start] != str[end]) return false;
    return isPalindrome(str, start + 1, end - 1);
}

int main() {
    std::string word = "racecar";

    if (isPalindrome(word, 0, word.size() - 1)) {
        std::cout << word << " is a palindrome\n";
    } else {
        std::cout << word << " is not a palindrome\n";
    }

    return 0;
}
```

---


## Function Templates


```c++

#include <iostream>

// function trmplates: describes what a function looks like
// Can be used to generate as many overloaded functions as needed, each using different datatypes 

int max(int x, int y){
    return (x > y) ? x : y; // is x > y, if so (?), return x, else (:), vreturn y
}
// this function is for int only. 
// If we want it to be compatible with doubles, we can repeat it with double 
double max(double x, double y){
    return (x > y) ? x : y; 
}
char max(char x, char y){
    return (x > y) ? x : y; 
}
//  these are overloaded functions
// we can create a function that accepts any datatypes. 
// This is called a function template: for the data type (int, double, etc), we use 'T' as a placeholder

template <typename T> 

T MAX(T x, T y){ // notethat both x, y are of the same datatype
    return (x > y) ? x : y; 
}

// to define two template datatypes: 

template <typename T, typename U>
auto MAX_2(T x, U y){ // notethat both x, y are of the same datatype
    return (x > y) ? x : y; 
}


int main(){

    std::cout<<max(1,2)<<std::endl; // 1 and 2 are passed to the function max
    std::cout<<"-------------------\n"; 
    std::cout<<MAX(1,2)<<std::endl;
    std::cout<<"-------------------\n";
    std::cout<<MAX_2(1,2.5); 

    return 0; 
}
```

---



## Structures 

```c++

#include <iostream>

// struct = A structure that groups related variables under one name struct that 
// can contain many different datatypes (string, int, double, etc.) 
// Variables in a struct are knwon as "members"
// members can be access with "Class Member Access Operator"

struct student{
    std::string name; 
    double gpa; 
    bool enrolled;
    // bool enrolled = true; // we can set this to true by default 
};

int main(){

    student student1; // create a student object
    student1.name = "Spongebob"; // set the name member
    student1.gpa = 3.5;
    student1.enrolled = true; 

    std::cout<<student1.name<<std::endl; 
    std::cout<<student1.gpa<<std::endl;
    std::cout<<student1.enrolled<<std::endl; 

    student student2; // create a student object
    student2.name = "Patric"; // set the name member
    student2.gpa = 2.1;
    student2.enrolled = true; 

    std::cout<<student2.name<<std::endl; 
    std::cout<<student2.gpa<<std::endl;
    std::cout<<student2.enrolled<<std::endl; 


    return 0; 
}
```

---

### Passing struct to a function: 


```c++
#include <iostream>

struct Car{
    std::string model; 
    int year; 
    std::string color; 
};

void printCar(Car car);
void printCar_original(Car &car);
void paintCar(Car &car, std::string color);

int main(){

    Car car1;
    Car car2; 

    car1.model = "Mustang"; 
    car1.year = 2025;
    car1.color = "black"; 

    car2.model = "Corvette";
    car2.year = 2023;
    car2.color = "blue";

    paintCar(car2, "gold"); // we wanna change the original color of the car. So we must pass it by reference (address) 

    std::cout<< "Original memory address of car: "<<&car1 << std::endl; 
    // when we pass the struct to a function, its address will be different. 
    // so passing by value will create a copy of the struct.
    printCar(car1); 
    printCar_original(car1); // this will not create a copy of the struct.

    printCar_original(car2);

    return 0; 
}

void printCar(Car car){
    std::cout << "Address of car: " << &car << std::endl; // this will print the address of the struct.
    std::cout << "Model: " << car.model << std::endl;
    std::cout << "Year: " << car.year << std::endl;
    std::cout << "Color: " << car.color << std::endl;
}

void printCar_original(Car &car){
    std::cout << "Address of car: " << &car << std::endl; // this will print the address of the struct.
    std::cout << "Model: " << car.model << std::endl;
    std::cout << "Year: " << car.year << std::endl;
    std::cout << "Color: " << car.color << std::endl;
}

void paintCar(Car &car, std::string color){
    car.color = color; 
    std::cout << "Car painted to: " << car.color << std::endl;
}
```

---

## enums

```c++

#include <iostream>

// enums = a user-defined datatype that consists of paired named-integer constants.
// Great if you have a set of potential options  

enum Day{sunday = 0, monday = 1,tuesday = 2, wednesday = 3, thursday = 4, friday = 5,saturday = 6};
// if we don't specify the values, they will be assigned automatically starting from 0.
 
int main(){

    // std::string today = "sunday"; 

    // we can't use strings with switches. so we'get error for this: 

    // switch(today){
    //     case "sunday": std::cout<<"It is Sunday!\n"; 
    //                    break;
    //     case "monday": std::cout<<"It is Monday!\n";
    //                    break;
    //     case "tuesday": std::cout<<"It is Tuesday!\n";
    //                     break;
    //     case "wednesday": std::cout<<"It is Wednesday!\n";
    //                       break;
    //     case "thursday": std::cout<<"It is Thursday!\n";
    //                      break;
    //     case "friday": std::cout<<"It is Friday!\n";    
    //                    break;
    // }

    // instead we can use enums.

    Day today = sunday; // enum takes only 1 value of the set 

    switch(today){
        case sunday: std::cout<<"It is Sunday!\n"; 
                       break;
        case monday: std::cout<<"It is Monday!\n";
                       break;
        case tuesday: std::cout<<"It is Tuesday!\n";
                        break;
        case wednesday: std::cout<<"It is Wednesday!\n";
                          break;
        case thursday: std::cout<<"It is Thursday!\n";
                         break;
        case friday: std::cout<<"It is Friday!\n";    
                       break;
    }

    return 0; 
}
```

---

Write a program to rotate a string clockwise for k elements.

### Rotate String Clockwise: Given a string and integer k, rotate the string clockwise by k characters.


eg: ABCDEFGH, k = 2  ==> GHABCDEF

eg: ABCDEFGH, k = 3  ==> FGHABCDE


```c++
#include <iostream>
using namespace std;

int main() {
    std::string S; 
    int k; 
    std::cout << "Enter String: ";
    std::cin >> S; // Example: ABCDEFG
    std::cout << "Enter k: "; 
    std::cin >> k; // Example: 2

    std::string shifted_right, shifted_left; 
    int n = S.length(); 

    for(int i = 0; i < n; i++){
        shifted_right += S[(i - k + n) % n];  // right shift
        shifted_left  += S[(i + k) % n];      // left shift
    }

    std::cout << "Right Shifted: " << shifted_right << "\n";
    std::cout << "Left Shifted: "  << shifted_left << "\n";

    return 0;
}

// n = 7, k = 2, S = ABCDEFG -> S = A B C D E F G

// i = 0 -> S[(i - k + n) % n] = S[(0 - 2 + 7) % 7] = S[(5) % 7] = S[5] = F -> shifted = F

// i = 1 -> S[(i - k + n) % n] = S[(1 - 2 + 7) % 7] = S[(6) % 7] = S[6] = G -> shifted = FG

// i = 2 -> S[(i - k + n) % n] = S[(2 - 2 + 7) % 7] = S[(7) % 7] = S[0] = A -> shifted = FGA

// i = 3 -> S[(i - k + n) % n] = S[(3 - 2 + 7) % 7] = S[(8) % 7] = S[1] = B -> shifted = FGAB"
```

---

```c++
int removeDuplicates(int* nums, int numsSize) {
    int i, j, a, k = 1;
 
    for (i = 0; i < numsSize-1; i++) {
        for (j = i+1; j < numsSize; j++) {
            if (nums[j] > nums[i]) {
                a = nums[i+1];
                nums[i+1] = nums[j];
                nums[j] = a;
                k++;
                break;
            } else {
                if (j == numsSize-1) {
                    i = numsSize;
                }
            }
        }
    }
 
    return k;
}
```

---


# Object-Oriented Programming 


```c++
#include <iostream>

// object = A collection of attributes and methods 
// They can have characteristics and could perform actions 
// Can be used to mimic real world items (ex. phone, book, etc)
// Created from a class which acts as a "blue-print"

class Human{
    public: // public access modifier 
        std::string name; // attributes
        std::string occupation;
        int age; 
        std::string sex = "Male or Female"; // default attributes 
        void eat(){ // these function are methods 
            std::cout << "this person is eating"<< std::endl;
        }
        void drink(){
            std::cout << "this person is drinking"<< std::endl;
        }
        void sleep(){
            std::cout << "this person is sleeping"<< std::endl;
        }
};

int main(){

    Human human1; 
    human1.name = "John";
    human1.occupation = "Engineer";
    human1.age = 30;

    std::cout << "Name: " << human1.name << std::endl;
    std::cout << "Occupation: " << human1.occupation << std::endl;
    std::cout << "Age: " << human1.age << std::endl;

    human1.eat(); 
    human1.drink();
    human1.sleep();

    return 0; 
}
```

---


```c++
#include <iostream>

class Car{
    public: 
        std::string make; 
        std::string model; 
        int year; 
        std::string color; 

        void accelerate(){
            std::cout<< "You step on the gas!\n";
        }
        void brake(){
            std::cout<< "You step on the brake!\n";
        }
};

int main(){

    Car car1; 
    car1.make = "Ford"; 
    car1.model = "Mustang";
    car1.year = 2025; 
    car1.color = "Black";

    std::cout<< "Car make: " << car1.make << "\n";
    std::cout<< "Car model: " << car1.model << "\n";
    std::cout<< "Car year: " << car1.year << "\n";
    std::cout<< "Car color: " << car1.color << "\n";

    car1.accelerate();
    car1.brake();

    return 0; 
}
```

---

```c++
#include <iostream>

// constructor = special method that is automatically called when an object is instantiated 
// useful for assigning values to attributes as arguments 

class Student{
    public: 
        std::string name; 
        int age; 
        double gpa; 
    
    Student(std::string name, int age, double gpa){ // constructor 
        this->name = name;
        this->age = age;
        this->gpa = gpa; 
    }
};

class Student2{
    public: 
        std::string name; 
        int age; 
        double gpa; 
    
    Student2(std::string x, int y, double z){ 
        // if the attribute names are different than the parameter names, we don't need to use "this->"
        name = x;
        age = y;
        gpa = z; 
    }
};


int main(){

    Student student1("Hamed", 27, 4); // create an object of the class Student
    std::cout<<student1.name<<std::endl;
    std::cout<<student1.age<<std::endl;
    std::cout<<student1.gpa<<std::endl;


    return 0; 
}
```

---


```c++
#include <iostream>

class Car{
    public: 
        std::string make; 
        std::string model;
        int year;
        std::string color; 
    
    Car(std::string make, std::string model, int year, std::string color){
        this->make = make; 
        this->model = model; 
        this->year = year; 
        this->color = color; 
    }
};
int main(){

    Car car1("Checyrolet", "Camaro", 2020, "Blue");
    std::cout<<"Car 1: " << car1.make << " " << car1.model << " " << car1.year << " " << car1.color << std::endl;

    Car car2("Ford", "Mustang", 2021, "Red");
    std::cout<<"Car 2: " << car2.make << " " << car2.model << " " << car2.year << " " << car2.color << std::endl;

    return 0; 
}
```

---



## Overloaded Constructores 

```c++
#include <iostream>

// Overloaded Constructores = multiple constructors with same name but different parameters 
// allows for varying arguments when instantiating an object

class Pizza{
    public:
        std::string topping1;
        std::string topping2; 
    Pizza(){
    }
    Pizza(std::string topping1){
        this->topping1 = topping1;
    }
    Pizza(std::string topping1, std::string topping2){
        this->topping1 = topping1;
        this->topping2 = topping2;
    }
};

int main(){

    Pizza pizza1("pepperoni");
    std::cout<<pizza1.topping1<<std::endl;

    Pizza pizza2("mushrooms", "green peppers"); 
    std::cout<<pizza2.topping1<<std::endl;
    std::cout<<pizza2.topping2<<std::endl;

    Pizza pizza3; 

    return 0; 
}
```

---

```c++
#include <iostream>

// Abstraction = hiding unnecessary data from outside a class
// getter = function that makes a private attribute READABLE
// setter = function that makes a private attribute WRITABLE

class Stove{
    private: 
        int power = 0; // this attribute is private and not accessible from outside the class, others cannot change it

    public: 
        int temperature = 0; // this attribute is public and accessible from outside the class, others can change it 
        Stove(int power = 0){ // constructor with default value
            setPower(power); // set the power using the setter function
        }
        int getPower(){
            return power; // getter function to make the private attribute readable
        }
        void setPower(int power){
            if(power < 0){
                this->power = 0; 
            }
            else if(power >=10){
                this->power = 10;
            }
            else{
                this->power = power;
            }
        }
};

int main(){
    Stove stove; // create an object of the class
    stove.temperature = 100; // change the temperature of the stove
    std::cout << "Stove temperature: " << stove.temperature << std::endl; // print the temperature of the stove

    std::cout<<"Stove power: " << stove.getPower() << std::endl; 

    stove.setPower(100); // change the power of the stove
    std::cout << "Stove power: " << stove.getPower() << std::endl; // print the power of the stove

    return 0; 
}

```

---


## Inheritance

```c++

#include <iostream>

// Inheritance = A class can receive attributes and methods from another class.
// Sub classes inherit from a base class.
// Helps to reuse similar code found within multiple classes 

class Animal{
    public:
        bool alive = true; 
        void eat(){
            std::cout << "Animal is eating" << std::endl;
        }
};

class Dog : public Animal{
    public:
        void bark(){
            std::cout << "Dog is barking" << std::endl;
        }
        void eat(){
            std::cout << "Dog is eating" << std::endl;
        }
};

class Cat : public Animal{
    public:
        void meow(){
            std::cout << "Cat is meowing" << std::endl;
        }
        void eat(){
            std::cout << "Cat is eating" << std::endl;
        }
};

int main(){

    Dog dog;
    dog.eat(); 
    Cat cat; 
    cat.eat();
    dog.bark();
    cat.meow();

    return 0; 
}
```


---

```c++
#include <iostream>

class Shape{
    public:
        double area = 0;
        double volume = 0;
};

class Cube : public Shape{
    public:
        double side;
        Cube(double side){
            this->side;
            this->area = 6 * side * side;
            this->volume = side * side * side;
        }
};

class Sphere : public Shape{
    public:
        double radius;
        Sphere(double radius){
            this->area = 4 * 3.14159 * radius * radius;
            this->volume = (4.0/3.0) * 3.14159 * radius * radius * radius; 
            //4.0 and 3.0 must be double so that the result is double and not int 
        }
};


int main(){

    Cube cube(10); 
    std::cout << "Cube area: " << cube.area <<"cm\n"<< std::endl;
    std::cout << "Cube volume: " << cube.volume <<"cm^3\n"<< std::endl;

    Sphere sphere(10);
    std::cout << "Sphere area: " << sphere.area <<"cm\n"<< std::endl;
    std::cout << "Sphere volume: " << sphere.volume <<"cm^3\n"<< std::endl;

    return 0; 
}
```



---

# Multithreading in modern C++ 

source: https://www.youtube.com/watch?v=xPqnoB2hjjA 

Multithreading is the ability of multiple parts of one program to be executed at the same time 

There are two ways to achieve this. 

First way is multitasking which is switching between tasks so fast that it becomes unnoticable to human eye, so it seams like a parallel execution. This is not multithreading. This is just multi-tasking. 

The seond way is real multi-threading. It means we write and divide our program in such a way that individual part of it can be executed at the same time. For example, first core of CPU takes the first thread and second core takes the second thread and both of the work at the same time. 


---

```c++
#include <iostream>
#include<thread> 

void function1(){
    for(int i = 0; i < 200; i++){
        std::cout<<"+"; 
    }
};

void function2(){
    for(int i = 0; i < 200; i++){
        std::cout<<"-"; 
    }
};

int main(){

    std::thread worker1(function1); 
    std::thread worker2(function2);

    // Wait for both threads to finish
    worker1.join();
    worker2.join(); 
    // each time we run this, the result would be different 

    return 0; 
}
```


The thread that is faster will output first and then the thread that is slower will output second. we can't predict how long the faster thread will be able to write its data before that second data jumps in and starts writing its data. 

So we must divide our program in such way that each thread knows what is its job. Otherwise, we will have race conditions and thread locks. 

Suppose we wanna keep getting data from API that is farway and this takes few seconds each time in the middle of programming. To aoiv this problem: 

We can create a thread that will work in the background and its job is to get the data from API and store it in computer memory. So it'll create a cache, then its job is also refreshing the data every mins or every couple of seconds. 

In this case when user asks that data, we don't send its request to the API, we take that info from the data that is already available in our cache. This happens instantly and there will be no delay. 


---
```c++
#include <iostream>
#include <thread> 
#include <map>
#include <string> 
#include <chrono>
using namespace std::chrono_literals;

void Refreshforcast(std::map<std::string, int> forcastMap){
    while(true){ //infinite loop 
        for(auto& item: forcastMap){
            item.second++;  // temperature
            std::cout<<item.first<<" - "<<item.second<<std::endl; 
        }
        std::this_thread::sleep_for(2000ms); // refreshing every 2 sec
    }
};

int main(){

    std::map<std::string, int> forcastMap = {
        {"New York", 15},
        {"Mumbai", 20},
        {"Burlin", 18}
    }; 

    std::thread bgWorker(Refreshforcast,forcastMap);
    bgWorker.join();


    return 0; 
}
```


---

# Mutex

### mutex = mutual exclusion 

### A way to ensure that inside a multi-threaded application, two threads cannot access the same code at the same time. 

---

```c++
#include <iostream>
#include <thread> 
#include <chrono> 

void driveCar(std::string driverName){
    std::cout<<driverName<<" is driving"<<std::endl;
    std::this_thread::sleep_for(std::chrono::seconds(2));
    std::cout<<driverName<< " is done driving"<< std::endl; 
};

int main(){
    std::thread t1(driveCar, "Saldina"); 
    std::thread t2(driveCar, "Elon"); 
    t1.join(); // before this program end, both these threads finished their job 
    t2.join(); 


    return 0; 
}
```
---


So it can't be possible that 2 person (saldina and elon) are driving the same car at the same time. To solve this problem we use mutex. we can understand mutex as a lock. It locks certain part of the code while one thread is executing it and then once that thread finishes it, it will unlock that code so that other thread can access it. 

the part of the code that is locked is called critical section.

---

```c++

#include <iostream>
#include <thread> 
#include <chrono> 
#include <mutex> 

std::mutex carMutex; 

void driveCar(std::string driverName){

    std::unique_lock<std::mutex> carLock(carMutex); 

    std::cout<<driverName<<" is driving"<<std::endl;
    std::this_thread::sleep_for(std::chrono::seconds(2));
    std::cout<<driverName<< " is done driving"<< std::endl; 

    carLock.unlock(); 
};

// another way is to: 

void driveCar2(std::string driverName){
    
    std::lock_guard<std::mutex> carLock(carMutex); 
    // simpler and easier. It is gonna unlock automatically at the end of the function.
    // it can't be unlocked manually.  

    std::cout<<driverName<<" is driving"<<std::endl;
    std::this_thread::sleep_for(std::chrono::seconds(2));
    std::cout<<driverName<< " is done driving"<< std::endl; 
};


int main(){
    std::thread t1(driveCar, "Saldina"); 
    std::thread t2(driveCar, "Elon"); 
    t1.join(); // before this program end, both these threads finished their job 
    t2.join();
     
    return 0; 
}

```

---





### 1. `mutex`
- **`std::mutex`** stands for **mutual exclusion**.
- It is used to **protect shared data** when **multiple threads** are running at the same time (multi-threading).
- **Only one thread** can lock the mutex at a time. Others must wait.

Example:

```cpp
#include <mutex>

std::mutex mtx;

void updateSharedData() {
    mtx.lock();
    // critical section: safely modify shared variables
    mtx.unlock();
}
```
(Usually, we prefer `std::lock_guard<std::mutex>` for automatic locking/unlocking.)

➔ **Purpose**: avoid race conditions in multi-threaded programs.

---

### 2. `malloc`
- **`malloc`** stands for **memory allocation**.
- It's a **C-style** function to **allocate raw memory** on the heap.
- In **modern C++**, **we prefer `new` and `delete`** instead of `malloc`/`free`.

Example (C-style, NOT recommended in C++):
```cpp
#include <cstdlib> // for malloc, free

int* p = (int*)malloc(5 * sizeof(int)); // allocate array of 5 integers
if (p) {
    // use p
    free(p); // must free manually
}
```

C++-style is better:
```cpp
int* p = new int[5];
// use p
delete[] p;
```

➔ **Purpose**: dynamic memory management.

---

### 3. `mutable`
- **`mutable`** is a **keyword** in C++.
- It allows **changing a member variable** **even inside a `const` method**.
- Normally, `const` methods are not allowed to modify members — but `mutable` breaks that restriction.

Example:
```cpp
class Example {
    mutable int counter = 0;
public:
    void get() const {
        counter++;  // allowed because counter is mutable
    }
};
```

➔ **Purpose**: allow specific variables to change even when the object is "logically" constant (e.g., caching, counters).

---


## Plotting in C++ 

```c++
#include <iostream>
#include "gnuplot-iostream.h"

int main() {
    Gnuplot gp;

    std::vector<std::pair<double, double>> xy_pts;
    for(double x = -2; x <= 2; x += 0.01) {
        xy_pts.emplace_back(x, x*x);  // y = x^2
    }

    gp << "plot '-' with lines title 'y = x^2'\n";
    gp.send1d(xy_pts);
}
```


# Some general practice/review 

---
```c++
#include <iostream>
#include <vector>
#include <cmath>
#include <map>
#include <tuple>
#include <string>

int main() {
    // Arrays and tuples
    std::vector<int> arr = {1, 2, 3, 4, 5};
    std::vector<std::vector<int>> arr3 = {
        {1, 2, 3},
        {4, 5, 6},
        {7, 8, 9}
    };

    std::tuple<int, double, char> t = {1, 2.4, 'a'};
    std::tuple<int, double, std::string> p = {1, 2.3, "Hello"};

    // linspace
    std::vector<double> t_vec(100);
    for (int i = 0; i < 100; ++i) t_vec[i] = i / 99.0;

    // arange
    std::vector<double> t;
    for(double i = 0; i<10; i += 0.1) t.push_back(i);
    for(double val : t){
        std::cout<< val << " "; 
    }
    std::cout<< std::endl;

    // Loops
    for (int i = 0; i < 5; ++i) std::cout << i << "\n";

    std::vector<int> nums = {10, 20, 30};
    for (int num : nums) std::cout << num << "\n";

    for (size_t i = 0; i < nums.size(); ++i)
        std::cout << i << " " << nums[i] << "\n";

    std::map<std::string, int> d = {{"a", 1}, {"b", 2}};
    for (const auto& [key, value] : d)
        std::cout << key << ": " << value << "\n";

    std::vector<int> a = {1, 2, 3}, b = {4, 5, 6};
    for (size_t i = 0; i < a.size(); ++i)
        std::cout << a[i] << " " << b[i] << "\n";

    // Fill a matrix
    double R[3][3];
    for (int i = 0; i < 3; ++i)
        for (int j = 0; j < 3; ++j)
            R[i][j] = i*i + j*j;

    // Sinusoids
    std::vector<double> y, y2(100);
    for (int i = 0; i < 100; ++i) {
        y.push_back(sin(2 * M_PI * t_vec[i]));
        y2[i] = sin(2 * M_PI * t_vec[i]);
    }

    // Right and left circular shift
    std::string S = "ABCDEFG";
    int k = 2, n = S.length();
    std::string shifted_right, shifted_left;
    for (int i = 0; i < n; ++i) {
        shifted_right += S[(i - k + n) % n];
        shifted_left  += S[(i + k) % n];
    }

    std::cout << "Right shifted: " << shifted_right << "\n";
    std::cout << "Left shifted: " << shifted_left << "\n";

    return 0;
}
```

---

## Linspace Function: 

```c++
#include <iostream>
#include <vector>
#include <cmath>
#include <map>
#include <tuple>
#include <string>

std::vector<double> linspace(double x0, double x_end, int len) {
    std::vector<double> result(len);
    for (int i = 0; i < len; ++i) {
        result[i] = x0 + ((x_end - x0)/(len - 1.0)) * i;
    }
    return result;
};

int main() {

    std::vector<double> x = linspace(0.0, 100.0, 10);

    for (double val : x) {
        std::cout << val << " ";
    }
    std::cout << std::endl;    

    return 0;
}

```


---

```c++
#include <iostream>
#include <vector>
#include <memory>
#include <cmath>
#include <string>

class Shape {
public:
    double area;
    std::string name;

    virtual void update_area() = 0; // pure virtual function
    virtual ~Shape() = default;
};

class Square : public Shape {
private:
    double side;
public:
    Square(double s) : side(s) {
        name = "Square";
        update_area();
    }

    void update_area() override {
        area = side * side;
    }
};

class Rectangle : public Shape {
private:
    double side1, side2;
public:
    Rectangle(double s1, double s2) : side1(s1), side2(s2) {
        name = "Rectangle";
        update_area();
    }

    void update_area() override {
        area = side1 * side2;
    }
};

class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) {
        name = "Circle";
        update_area();
    }

    void update_area() override {
        area = M_PI * radius * radius;
    }
};

int main() {
    std::vector<std::unique_ptr<Shape>> shapes;

    shapes.push_back(std::make_unique<Square>(4));
    shapes.push_back(std::make_unique<Rectangle>(4, 5));
    shapes.push_back(std::make_unique<Circle>(3));

    for (const auto& shape : shapes) {
        shape->update_area();
        std::cout << "Area of " << shape->name << ": " << shape->area << std::endl;
    }

    return 0;
}
```

---

```c++
#include <iostream>
#include <vector>
#include <memory>
#include <string>

class Vehicle {
public:
    std::string brand;
    std::string model;
    int year;

    Vehicle(const std::string& b, const std::string& m, int y)
        : brand(b), model(m), year(y) {}

    virtual void start() const {
        std::cout << "Engine started" << std::endl;
    }

    virtual void stop() const {
        std::cout << "Engine stopped" << std::endl;
    }

    virtual ~Vehicle() = default;
};

class Car : public Vehicle {
public:
    int number_of_doors;

    Car(const std::string& b, const std::string& m, int y, int doors)
        : Vehicle(b, m, y), number_of_doors(doors) {}

    void start() const override {
        std::cout << "Car is starting" << std::endl;
    }

    void stop() const override {
        std::cout << "Car is stopping" << std::endl;
    }
};

class Motorcycle : public Vehicle {
public:
    Motorcycle(const std::string& b, const std::string& m, int y)
        : Vehicle(b, m, y) {}

    void start() const override {
        std::cout << "Motorcycle is starting" << std::endl;
    }

    void stop() const override {
        std::cout << "Motorcycle is stopping" << std::endl;
    }
};

int main() {
    std::vector<std::unique_ptr<Vehicle>> vehicles;
    vehicles.push_back(std::make_unique<Car>("Toyota", "Corolla", 2020, 4));
    vehicles.push_back(std::make_unique<Motorcycle>("Honda", "CBR", 2021));

    for (const auto& vehicle : vehicles) {
        std::cout << "Inspecting " << vehicle->brand << " " << vehicle->model
                  << " (" << typeid(*vehicle).name() << ")" << std::endl;
        vehicle->start();
        vehicle->stop();
    }

    return 0;
}

```

---

# Some Examples: 


### Reverse a word in string: Reverse the order of words in a sentence.

e.g., 

`string s = "the sky is blue";`

`"blue is sky the"`


```c++
#include <iostream>
#include <sstream>
#include <vector>
#include <algorithm>

std::string reverseWords(std::string s) {
    std::istringstream iss(s);
    std::string word;
    std::vector<std::string> words;

    // Split string into words
    while (iss >> word) {
        words.push_back(word);
    }

    // Reverse the words
    std::reverse(words.begin(), words.end());

    // Join back into a string
    std::ostringstream oss;
    for (size_t i = 0; i < words.size(); ++i) {
        if (i > 0) oss << " ";
        oss << words[i];
    }

    return oss.str();
}

int main() {
    std::string s = "the sky is blue";
    std::string result = reverseWords(s);
    std::cout << result << std::endl;  // Output: "blue is sky the"
    return 0;
}
```

---

### Count Frequency of Characters: Count how many times each character appears in a string.


```c++
#include <iostream>
#include <unordered_map>
#include <string>

int main() {
    std::string s = "apple";
    std::unordered_map<char, int> freq;

    for (char c : s) {
        freq[c]++;
    }

    for (const auto& pair : freq) {
        std::cout << pair.first << ": " << pair.second << std::endl;
    }

    return 0;
}
```

---

### Rotate Array Right: Rotate an array to the right by k positions.

```c++
class Solution{
    public: 
        std::vector<int> rotate(std::vector<int>& nums, int k){
            int n = nums.size();
            std::vector<int> rotated = nums; 
            for(int i = 0; i < n;i++){
                rotated[i] = nums[(i - k + n)% n];
            }
            return rotated; 
        }
};

int main() {

    std::vector<int> nums = {1,2,3,4,5};
    int k = 2; 
    Solution sol; 
    std::vector<int> result = sol.rotate(nums, k);
    for (int num : result) {
        std::cout << num << " ";
    }

    return 0;
}
```

---

### Sorting array in ascending order.

```c++
class Solution{
    public: 
        std::vector<int> sorted(std::vector<int> arr){
            int n = arr.size();
            int temp;
            for(int i = 0; i < n-1; i++){
                for(int j = i+1; j < n; j++){
                    if(arr[i] > arr[j]){
                        temp = arr[i];
                        arr[i] = arr[j]; 
                        arr[j] = temp; 
                    }
                }
            }
            return arr; 
        }    
};

int main() {

    std::vector<int> arr = {1,3,53,6,8,2}; 
    Solution sol; 
    std::vector<int> sorted = sol.sorted(arr); 
    for(int ar : sorted){
        std::cout<<ar<<" "; 
    }

    return 0;
}
```

---

---

# What is `->` in C++?

The `->` **arrow operator** is used to access **members of a struct/class/union** through a **pointer**.

```cpp
ptr->member
```

is equivalent to:

```cpp
(*ptr).member
```

The arrow operator:

* **Dereferences the pointer** (`*ptr`)
* **Accesses the member** (`.member`)
  in one clean step.


### Example 1: Accessing struct members via pointer

```cpp
#include <iostream>

struct Person {
    std::string name;
    int age;
};

int main() {
    Person p = {"Alice", 30};
    Person* ptr = &p;

    // Using -> to access members through pointer
    std::cout << ptr->name << " is " << ptr->age << " years old.\n";

    // Equivalent to:
    std::cout << (*ptr).name << " is " << (*ptr).age << " years old.\n";

    return 0;
}
```

---

### Example 2: Class member function via pointer

```cpp
#include <iostream>

class Animal {
public:
    void speak() {
        std::cout << "Woof!\n";
    }
};

int main() {
    Animal dog;
    Animal* ptr = &dog;

    ptr->speak();  // Calls speak() using pointer
    return 0;
}
```

---

### Example 3: Dynamic allocation

```cpp
class Car {
public:
    void start() {
        std::cout << "Engine started!\n";
    }
};

int main() {
    Car* myCar = new Car();  // dynamically allocated object
    myCar->start();          // access method using ->
    delete myCar;            // don't forget to free memory
}
```

---

* `.` is used with objects.
* `->` is used with **pointers to objects**.

---


---


# Data Structures and Algorithms: 

- Arrays / Strings 
- HashMaps
- Sets 
- Two Pointers
- Sliding Window
- Linked Lists
- Trees (BFS / DFS)
- Binary Search
- Heaps / Priority Queues
- Stack / Queue
- Simple Dynamic Programming



---

## Arrays / Strings 

```c++
std::vector<int> nums = {1, 2, 3, 4};
int maxVal = nums[0];
for (int num : nums) maxVal = std::max(maxVal, num);
std::cout << "Max: " << maxVal;
```

---

## HashMaps

> HashMap: Stores key-value pairs for fast lookup, insertion, and deletion. (also known as unordered_map)

> Use case: Finding duplicates, frequency counting, constant-time lookups.

---

```c++
#include <unordered_map>
#include <string>
int main(){

    std::unordered_map<std::string, int> wordCount; 
    wordCount["apple"]++;
    wordCount["banana"]++; 
    wordCount["apple"]++;
    for(const auto& pair : wordCount){
        std::cout<<pair.first<< ": " << pair.second<< "\n"; 
    }

    // another example: 
    std::unordered_map<int, std::string> studentMap; 
    studentMap[101] = "Alice"; 
    studentMap[102] = "Bob"; 
    std::cout<<"student 102: " << studentMap[102]<< "\n"; 

    return 0; 
}
```

---

```c++
#include <unordered_map>
#include <vector>

// check for duplicates: 
bool hasDuplicate(const std::vector<int> nums){
    std::unordered_map<int,bool> seen; 
    for(int num : nums){
        if(seen[num] == true) {
            return true
        }else{
            seen[num] = true; 
        }
    }else{
        return false; 
    }
};

int main(){

    std::vector<int> nums = {1,2,3,4,1}; 
    std::cout<<(hasduplicate(nums) ? "Duplicate found" : "No duplicates")<<"\n";

    return 0; 
}
```
---

```c++
#include <iostream>
#include <string>
#include <unordered_map>
int main(){
    std::string s = "hello"; 
    std::unordered_map<char,int> charCount; 
    for(char c : s){
        charCount[c]++; 
    }
    for(auto& p : charCount){
        std::cout<< p.first<<" : "<< p.second<<"\n";
    }

    reuturn 0; 
}
```

--- 

```c++
#include <iostream>
#include <vector>
#include <unordered_map>

//Two Sum: 
std::vector<int> twoSum(std::vector<int>& nums, int target){
    std::unordered_map<int, int> map; // number and its index
    for(int i = 0; i < nums.size; i++){
        int complement = target - nums[i]; 
        // We want: nums[i] + complement == target, So we check: has the complement been seen before?
        if(map.count(complement)){
            // If complement exists in the map, we’ve already seen a number that would add with nums[i] to give target.
            return {map[complement],i}; 
        }
        map[nums[i]] = i; // If complement not found, store the current number and its index.
    }
    return {}; // if no solution found 
}

int main(){

    std::vector<int> nums = {2,7,11,15}; 
    int target = 9; 
    std::vector<int> result = twoSum(nums,target); 
    std::cout<<result[0]<<" , "<<result[1] << "\n"; 

    return 0; 
}
```

---

```c++
#include <iostream>
#include <vector>
#include <unordered_map>
#include <queue>

std::vector<int> topKFrequent(std::vector<int>& nums, int k) {
    std::unordered_map<int, int> freq;
    for (int num : nums) {
        freq[num]++;
    }

    // Min-heap to keep top k
    using P = std::pair<int, int>; // frequency, number
    auto cmp = [](P a, P b) { return a.first > b.first; };
    std::priority_queue<P, std::vector<P>, decltype(cmp)> pq(cmp);

    for (const auto& [num, count] : freq) {
        pq.push({count, num});
        if (pq.size() > k) pq.pop();
    }

    std::vector<int> result;
    while (!pq.empty()) {
        result.push_back(pq.top().second);
        pq.pop();
    }
    return result;
}

int main() {
    std::vector<int> nums = {1, 1, 1, 2, 2, 3};
    int k = 2;

    std::vector<int> res = topKFrequent(nums, k);
    for (int n : res) std::cout << n << " ";  // Output: 1 2
}

```



---


## Sets 

> Set: A std::set stores unique elements in sorted order (Red-Black Tree).

> A std::unordered_set stores unique elements in no particular order (Hash Table).


```c++
#include <unordered_set>

std::string s = "abcde"; 
std::unordered_set<char> seen; 
for(char c : s){
    if(seen.count(c)) std::cout<<"duplicate" << c; 
    seen.insert(c);
}
```
---

```c++
#include <iostream>
#include <set>

int main() {
    std::set<int> s;

    s.insert(5);
    s.insert(3);
    s.insert(8);
    s.insert(3);  // duplicate, ignored

    for (int val : s) {
        std::cout << val << " ";  // Output: 3 5 8 (sorted)
    }

    return 0;
}
```

---

```c++
#include <iostream>
#include <unordered_set>

int main() {
    std::unordered_set<std::string> names;

    names.insert("Alice");
    names.insert("Bob");
    names.insert("Alice");  // ignored, already exists

    if (names.count("Alice")) {
        std::cout << "Alice is in the set\n";
    }

    if (!names.count("Charlie")) {
        std::cout << "Charlie not found\n";
    }

    return 0;
}
```

---

```c++
// check for duplicates using sets 

#include <iostream>
#include <vector>
#include <set>

bool hasDuplicate(const std::vector<int>& nums) {
    std::set<int> seen;
    for (int num : nums) {
        if (seen.count(num)) return true;
        seen.insert(num);
    }
    return false;
}

int main() {
    std::vector<int> nums = {1, 2, 3, 4, 1};
    std::cout << (hasDuplicate(nums) ? "Duplicate found" : "No duplicates") << "\n";
}
```

---

```c++
// Set Operations: Union, Intersection, Difference
#include <iostream>
#include <set>
#include <algorithm>

int main() {
    std::set<int> A = {1, 2, 3, 4};
    std::set<int> B = {3, 4, 5, 6};
    std::set<int> result;

    // Intersection
    std::set_intersection(A.begin(), A.end(), B.begin(), B.end(),
                          std::inserter(result, result.begin()));

    for (int x : result) std::cout << x << " ";  // Output: 3 4
}
```


---

## Two Pointers 

> Two pointers move toward each other or in parallel to process data (often sorted arrays).

> Use case: Problems like finding subarrays with a sum, longest substring without repeating characters.

```c++
#include <iostream>
#include <vector>
#include <algorithm>

bool hasPairWithSum(std::vector<int>& nums, int target) {
    std::sort(nums.begin(), nums.end());  // must be sorted
    int left = 0, right = nums.size() - 1;

    while (left < right) {
        int sum = nums[left] + nums[right];
        if (sum == target) return true;
        else if (sum < target) left++;
        else right--;
    }

    return false;
}

int main() {
    std::vector<int> nums = {1, 4, 6, 8, 10};
    std::cout << (hasPairWithSum(nums, 14) ? "Found" : "Not found") << "\n";  // Found
}
```

```c++
// Remove Duplicates from Sorted Array (in-place)
#include <iostream>
#include <vector>

int removeDuplicates(std::vector<int>& nums) {
    if (nums.empty()) return 0;
    int slow = 0;

    for (int fast = 1; fast < nums.size(); ++fast) {
        if (nums[fast] != nums[slow]) {
            slow++;
            nums[slow] = nums[fast];
        }
    }

    return slow + 1;  // new length
}

int main() {
    std::vector<int> nums = {1, 1, 2, 2, 3};
    int len = removeDuplicates(nums);

    for (int i = 0; i < len; ++i)
        std::cout << nums[i] << " ";  // Output: 1 2 3
}
```

---

```c++
// Container With Most Water (LeetCode)
#include <vector>
#include <algorithm>

int maxArea(std::vector<int>& height) {
    int left = 0, right = height.size() - 1;
    int max_water = 0;

    while (left < right) {
        int h = std::min(height[left], height[right]);
        int width = right - left;
        max_water = std::max(max_water, h * width);

        if (height[left] < height[right]) left++;
        else right--;
    }

    return max_water;
}
```



---

## Sliding Window

> Sliding window uses a window of elements to process subarrays efficiently.

> Use case: Problems like finding subarrays with a sum, longest substring without repeating characters.


```c++
#include <iostream>
#include <vector>
// Maximum Sum of Subarray of Size K
int maxSumSubarrayK(const std::vector<int>& nums, int k) {
    int max_sum = 0, window_sum = 0;

    for (int i = 0; i < nums.size(); ++i) {
        window_sum += nums[i];

        if (i >= k - 1) {
            max_sum = std::max(max_sum, window_sum);
            window_sum -= nums[i - k + 1];
        }
    }

    return max_sum;
}

int main() {
    std::vector<int> nums = {2, 1, 5, 1, 3, 2};
    int k = 3;
    std::cout << "Max sum of size " << k << ": " << maxSumSubarrayK(nums, k) << "\n";  // Output: 9
}
```

---

```c++
// Maximum Element in Every Window of Size K
#include <iostream>
#include <deque>
#include <vector>

std::vector<int> maxSlidingWindow(std::vector<int>& nums, int k) {
    std::deque<int> dq;  // store indices
    std::vector<int> result;

    for (int i = 0; i < nums.size(); ++i) {
        // Remove indices out of current window
        if (!dq.empty() && dq.front() <= i - k) dq.pop_front();

        // Remove indices of smaller elements
        while (!dq.empty() && nums[dq.back()] < nums[i]) dq.pop_back();

        dq.push_back(i);

        if (i >= k - 1)
            result.push_back(nums[dq.front()]);
    }

    return result;
}

int main() {
    std::vector<int> nums = {1,3,-1,-3,5,3,6,7};
    int k = 3;
    auto res = maxSlidingWindow(nums, k);

    for (int val : res) std::cout << val << " ";  // Output: 3 3 5 5 6 7
}
```


---

## Linked Lists

> Data structure where each node points to the next. Unlike arrays, memory is not contiguous.

> Use case: Efficient insertions/deletions, reversing, merging sorted lists, cycle detection.

A linked list is a linear data structure where each element (node) contains:

    - Data

    - A pointer to the next node

Types:

    - Singly Linked List → one direction

    - Doubly Linked List → next and previous pointers

    - Circular Linked List → last node points back to head


```c++
// Node Structure (Singly Linked List)
struct ListNode {
    int val;
    ListNode* next;

    ListNode(int x) : val(x), next(nullptr) {}
};
```

---

```c++
// Print a Linked List
void printList(ListNode* head) {
    while (head != nullptr) {
        std::cout << head->val << " ";
        head = head->next;
    }
}
```

---

```c++
// Insert at the End
void insertAtEnd(ListNode*& head, int value) {
    ListNode* newNode = new ListNode(value);
    if (!head) {
        head = newNode;
        return;
    }
    ListNode* temp = head;
    while (temp->next) temp = temp->next;
    temp->next = newNode;
}
```

---

```c++
// Reverse a Linked List
ListNode* reverseList(ListNode* head) {
    ListNode* prev = nullptr;
    while (head) {
        ListNode* nextNode = head->next;
        head->next = prev;
        prev = head;
        head = nextNode;
    }
    return prev;
}
```

---

```c++
// Detect Cycle (Floyd’s Tortoise & Hare)
bool hasCycle(ListNode* head) {
    ListNode* slow = head;
    ListNode* fast = head;

    while (fast && fast->next) {
        slow = slow->next;
        fast = fast->next->next;
        if (slow == fast) return true;
    }
    return false;
}
```

---


```c++
// Merge Two Sorted Lists
ListNode* mergeTwoLists(ListNode* l1, ListNode* l2) {
    if (!l1) return l2;
    if (!l2) return l1;

    if (l1->val < l2->val) {
        l1->next = mergeTwoLists(l1->next, l2);
        return l1;
    } else {
        l2->next = mergeTwoLists(l1, l2->next);
        return l2;
    }
}
```

---

```c++
// Delete a Node (given just the node, not head)
void deleteNode(ListNode* node) {
    if (node && node->next) {
        node->val = node->next->val;
        ListNode* temp = node->next;
        node->next = node->next->next;
        delete temp;
    }
}
```

---

```c++
struct ListNode{ 
    int val; 
    ListNode* next; 
    ListNode(int x) : val(x), next(nullptr) {}
};

ListNode* reversal(ListNode* head){
    ListNode* prev = nullptr; 
    while(head){
        ListNode* next = head->next;
        head->next = prev;
        prev = head;
        head = next;
    }
    return prev; 
}
```

---

```c++
// Find middle node 
ListNode* middleNode(ListNode* head) {
    ListNode* slow = head;
    ListNode* fast = head;

    while (fast && fast->next) {
        slow = slow->next;
        fast = fast->next->next;
    }

    return slow;
}
```

---


 ## Trees (BFS / DFS)

> DFS (Depth-First Search): Traverse as far down a branch as possible before backtracking.

> BFS (Breadth-First Search): Visit nodes level by level.

> Use case: Navigating hierarchical data, pathfinding, serialization, recursion-based logic.

A **tree** is a special type of **graph** that:

* Has **no cycles**
* Has a **single root node**
* Each child has **only one parent**
* It’s often used to model hierarchical data (like file systems, XML, parse trees)

---

### Tree Traversal Methods

There are two major ways to traverse a tree:

#### **DFS (Depth-First Search)**

* Go **deep** into one branch before backtracking
* Types:

  * **Preorder** (root → left → right)
  * **Inorder** (left → root → right)
  * **Postorder** (left → right → root)

#### **BFS (Breadth-First Search)**

* Explore the tree **level by level**
* Uses a **queue** instead of recursion


### 4 Classic Tree Problems with DFS/BFS:

#### 1. **Maximum Depth of Binary Tree**

> DFS – post-order

```cpp
int maxDepth(TreeNode* root) {
    if (!root) return 0;
    return 1 + max(maxDepth(root->left), maxDepth(root->right));
}
```

---

#### 2. **Level Order Traversal (BFS)**

> BFS – queue based

```cpp
vector<vector<int>> levelOrder(TreeNode* root) {
    vector<vector<int>> result;
    if (!root) return result;
    queue<TreeNode*> q;
    q.push(root);

    while (!q.empty()) {
        int size = q.size();
        vector<int> level;
        for (int i = 0; i < size; ++i) {
            TreeNode* node = q.front(); q.pop();
            level.push_back(node->val);
            if (node->left) q.push(node->left);
            if (node->right) q.push(node->right);
        }
        result.push_back(level);
    }
    return result;
}
```

---

#### 3. **Path Sum**

> DFS – try all root-to-leaf paths

```cpp
bool hasPathSum(TreeNode* root, int targetSum) {
    if (!root) return false;
    if (!root->left && !root->right)
        return targetSum == root->val;
    return hasPathSum(root->left, targetSum - root->val) ||
           hasPathSum(root->right, targetSum - root->val);
}
```

---

#### 4. **Invert a Binary Tree**

> DFS – post-order or BFS – level-by-level swap

```cpp
TreeNode* invertTree(TreeNode* root) {
    if (!root) return nullptr;
    TreeNode* left = invertTree(root->left);
    TreeNode* right = invertTree(root->right);
    root->left = right;
    root->right = left;
    return root;
}
```

---

## Binary Search 

**Binary Search** is a powerful algorithm used to find elements in a **sorted array** in **O(log n)** time.

> Efficiently finds an element in a sorted array by repeatedly dividing the search interval in half.

> Use case: Finding targets, first/last occurrences, square roots, peak elements, etc.

* The array (or search space) is **sorted**
* You want to find:

  * An element’s **index**
  * The **first/last occurrence** of a value
  * A **boundary/condition** (e.g. smallest value that meets a condition)

### Binary Search Template:

```cpp
int binarySearch(vector<int>& nums, int target) {
    int left = 0, right = nums.size() - 1;

    while (left <= right) {
        int mid = left + (right - left) / 2; // prevent overflow
        if (nums[mid] == target)
            return mid;
        else if (nums[mid] < target)
            left = mid + 1;
        else
            right = mid - 1;
    }
    return -1; // not found
}
```

---

### Classic Binary Search Problems:

#### 1. **Find Target in Sorted Array**

```cpp
// Input: [1,2,4,6,9], target = 4 → Output: 2
```


---

#### 2. **Find First Occurrence of a Number**

```cpp
int firstOccurrence(vector<int>& nums, int target) {
    int left = 0, right = nums.size() - 1, ans = -1;
    while (left <= right) {
        int mid = left + (right - left)/2;
        if (nums[mid] >= target) {
            if (nums[mid] == target) ans = mid;
            right = mid - 1;
        } else {
            left = mid + 1;
        }
    }
    return ans;
}
```

---

#### 3. **Square Root of a Number (integer)**

```cpp
int mySqrt(int x) {
    int left = 0, right = x, ans = 0;
    while (left <= right) {
        long long mid = left + (right - left)/2;
        if (mid*mid <= x) {
            ans = mid;
            left = mid + 1;
        } else {
            right = mid - 1;
        }
    }
    return ans;
}
```

---

#### 4. **Search in Rotated Sorted Array**

```cpp
int search(vector<int>& nums, int target) {
    int left = 0, right = nums.size() - 1;
    while (left <= right) {
        int mid = left + (right - left)/2;
        if (nums[mid] == target) return mid;

        // Left half is sorted
        if (nums[left] <= nums[mid]) {
            if (nums[left] <= target && target < nums[mid])
                right = mid - 1;
            else
                left = mid + 1;
        } 
        // Right half is sorted
        else {
            if (nums[mid] < target && target <= nums[right])
                left = mid + 1;
            else
                right = mid - 1;
        }
    }
    return -1;
}
```

---


## Heaps / Priority Queues

A **heap** is a special **binary tree** used to implement **priority queues**, and it supports fast access to the **min or max element**.

> Use case: Always retrieving the smallest/largest item quickly (e.g., top K elements, scheduling tasks).


## Types of Heaps

| Type         | Property                             | Root |
| ------------ | ------------------------------------ | ---- |
| **Min-Heap** | Parent ≤ children → smallest at root | Min  |
| **Max-Heap** | Parent ≥ children → largest at root  | Max  |


## C++ Priority Queue (Default = Max Heap)

```cpp
#include <queue>

priority_queue<int> maxHeap;
priority_queue<int, vector<int>, greater<int>> minHeap;
```

---

### Classic Problems Using Heaps:

#### 1. **Find K Largest Elements**

```cpp
vector<int> findKLargest(vector<int>& nums, int k) {
    priority_queue<int, vector<int>, greater<int>> minHeap;
    for (int num : nums) {
        minHeap.push(num);
        if (minHeap.size() > k)
            minHeap.pop();
    }

    vector<int> result;
    while (!minHeap.empty()) {
        result.push_back(minHeap.top());
        minHeap.pop();
    }
    return result;
}
```

---

#### 2. **Kth Largest Element in a Stream**

```cpp
class KthLargest {
    priority_queue<int, vector<int>, greater<int>> minHeap;
    int k;
public:
    KthLargest(int k, vector<int>& nums) : k(k) {
        for (int num : nums) {
            add(num);
        }
    }

    int add(int val) {
        minHeap.push(val);
        if (minHeap.size() > k)
            minHeap.pop();
        return minHeap.top();
    }
};
```

---

#### 3. **Merge K Sorted Lists (or Arrays)**

```cpp
struct compare {
    bool operator()(ListNode* a, ListNode* b) {
        return a->val > b->val;  // min-heap
    }
};

ListNode* mergeKLists(vector<ListNode*>& lists) {
    priority_queue<ListNode*, vector<ListNode*>, compare> minHeap;

    for (auto node : lists)
        if (node) minHeap.push(node);

    ListNode dummy(0), *tail = &dummy;

    while (!minHeap.empty()) {
        ListNode* node = minHeap.top(); minHeap.pop();
        tail->next = node;
        tail = tail->next;
        if (node->next) minHeap.push(node->next);
    }
    return dummy.next;
}
```

---

#### 4. **Top K Frequent Elements**

```cpp
vector<int> topKFrequent(vector<int>& nums, int k) {
    unordered_map<int, int> freq;
    for (int num : nums) freq[num]++;

    priority_queue<pair<int, int>, vector<pair<int, int>>, greater<>> minHeap;

    for (auto& [num, count] : freq) {
        minHeap.push({count, num});
        if (minHeap.size() > k) minHeap.pop();
    }

    vector<int> result;
    while (!minHeap.empty()) {
        result.push_back(minHeap.top().second);
        minHeap.pop();
    }
    return result;
}
```
---

| Operation       | Min Heap | Max Heap |
| --------------- | -------- | -------- |
| Insert          | `log n`  | `log n`  |
| Get top element | `O(1)`   | `O(1)`   |
| Remove top      | `log n`  | `log n`  |


---




## Stack / Queue

> Stack: Last-In-First-Out (LIFO)

> Queue: First-In-First-Out (FIFO)

> Use case: Parsing expressions, undo operations (stack), task processing (queue), BFS (queue), DFS (stack).

Both **stack** and **queue** are linear data structures, but they differ in how elements are **added** and **removed**.


## Stack

A **stack** is **Last In, First Out (LIFO)**.
Think: a pile of plates — add/remove from the top.

### Operations:

* `push(x)` → add to top
* `pop()` → remove from top
* `top()` → peek at top
* `empty()` → check if stack is empty

```cpp
#include <stack>

stack<int> stk;
stk.push(10);
stk.pop();
int x = stk.top();
```

---

## Queue

A **queue** is **First In, First Out (FIFO)**.
Think: people in a line — first in is served first.

### Operations:

* `push(x)` → add to back
* `pop()` → remove from front
* `front()` → peek at front
* `empty()` → check if queue is empty

```cpp
#include <queue>

queue<int> q;
q.push(10);
q.pop();
int y = q.front();
```

---

### Classic Problems Using Stack / Queue:


#### 1. **Valid Parentheses**

> Use stack to check balanced `(), {}, []`

```cpp
bool isValid(string s) {
    stack<char> stk;
    for (char c : s) {
        if (c == '(' || c == '{' || c == '[') stk.push(c);
        else {
            if (stk.empty()) return false;
            char t = stk.top(); stk.pop();
            if ((c == ')' && t != '(') || 
                (c == '}' && t != '{') ||
                (c == ']' && t != '[')) return false;
        }
    }
    return stk.empty();
}
```

---

#### 2. **Min Stack**

> Support `getMin()` in constant time using a helper stack

```cpp
class MinStack {
    stack<int> stk, minStk;
public:
    void push(int val) {
        stk.push(val);
        if (minStk.empty() || val <= minStk.top()) minStk.push(val);
    }

    void pop() {
        if (stk.top() == minStk.top()) minStk.pop();
        stk.pop();
    }

    int top() { return stk.top(); }
    int getMin() { return minStk.top(); }
};
```

---

#### 3. **Implement Queue Using Stacks**

> Use two stacks to simulate queue behavior

```cpp
class MyQueue {
    stack<int> s1, s2;

    void move() {
        while (!s1.empty()) {
            s2.push(s1.top());
            s1.pop();
        }
    }
public:
    void push(int x) { s1.push(x); }

    int pop() {
        if (s2.empty()) move();
        int x = s2.top(); s2.pop();
        return x;
    }

    int peek() {
        if (s2.empty()) move();
        return s2.top();
    }

    bool empty() { return s1.empty() && s2.empty(); }
};
```

---

#### 4. **Sliding Window Maximum**

> Use deque to track max in current window

```cpp
vector<int> maxSlidingWindow(vector<int>& nums, int k) {
    deque<int> dq;
    vector<int> result;

    for (int i = 0; i < nums.size(); ++i) {
        // remove out-of-window
        if (!dq.empty() && dq.front() <= i - k) dq.pop_front();
        // remove smaller elements
        while (!dq.empty() && nums[dq.back()] < nums[i]) dq.pop_back();

        dq.push_back(i);
        if (i >= k - 1) result.push_back(nums[dq.front()]);
    }

    return result;
}
```

---


## Simple Dynamic Programming


**Dynamic Programming (DP)** is an optimization technique used to solve problems by breaking them down into **overlapping subproblems** and **saving the results** to avoid recomputation.

> Use case: Fibonacci, climbing stairs, coin change, knapsack — where brute-force recursion is inefficient.


### When to Use DP

Ask yourself:

> "Can I break this problem into smaller subproblems, and do I repeat the same calculations multiple times?"

If yes → DP is likely the right choice.

---

### Two Common DP Techniques

| Technique     | Description                                 |
| ------------- | ------------------------------------------- |
| **Top-down**  | Use recursion + memoization                 |
| **Bottom-up** | Use a table to build the answer iteratively |

---

### Simple Dynamic Programming Problems


#### 1. **Fibonacci Number**

#### Bottom-Up DP:

```cpp
int fib(int n) {
    if (n <= 1) return n;
    vector<int> dp(n+1);
    dp[0] = 0; dp[1] = 1;
    for (int i = 2; i <= n; ++i)
        dp[i] = dp[i-1] + dp[i-2];
    return dp[n];
}
```

#### Space Optimized:

```cpp
int fib(int n) {
    if (n <= 1) return n;
    int a = 0, b = 1;
    for (int i = 2; i <= n; ++i) {
        int temp = a + b;
        a = b;
        b = temp;
    }
    return b;
}
```

---

#### 2. **Climbing Stairs**

> You can climb 1 or 2 steps at a time. How many distinct ways to reach the top?

```cpp
int climbStairs(int n) {
    if (n <= 2) return n;
    int a = 1, b = 2;
    for (int i = 3; i <= n; ++i) {
        int temp = a + b;
        a = b;
        b = temp;
    }
    return b;
}
```

---

#### 3. **House Robber**

> Can't rob two adjacent houses. Max money you can rob?

```cpp
int rob(vector<int>& nums) {
    if (nums.empty()) return 0;
    if (nums.size() == 1) return nums[0];

    int prev2 = 0, prev1 = nums[0];
    for (int i = 1; i < nums.size(); ++i) {
        int curr = max(prev1, prev2 + nums[i]);
        prev2 = prev1;
        prev1 = curr;
    }
    return prev1;
}
```

---

#### 4. **0/1 Knapsack (Classic DP Table)**

```cpp
int knapsack(int W, vector<int>& wt, vector<int>& val, int n) {
    vector<vector<int>> dp(n+1, vector<int>(W+1, 0));

    for (int i = 1; i <= n; ++i) {
        for (int w = 0; w <= W; ++w) {
            if (wt[i-1] <= w)
                dp[i][w] = max(dp[i-1][w], val[i-1] + dp[i-1][w - wt[i-1]]);
            else
                dp[i][w] = dp[i-1][w];
        }
    }
    return dp[n][W];
}
```

---

## Patterns in Simple DP:

| Problem Type      | Technique     | Example            |
| ----------------- | ------------- | ------------------ |
| Count paths/ways  | Bottom-up     | Climb stairs       |
| Max/min value     | Rolling state | Robbery, knapsack  |
| Subsequence match | 2D DP table   | LCS, Edit Distance |

---
---
---

## Future topics: 

- Greedy Algorithms
- Backtracking
- Trie
- Bit Manipulation
- Divide and Conquer
- Design Patterns
- Intervals
- Matrix
- Kadane’s Algorithm

---
---
