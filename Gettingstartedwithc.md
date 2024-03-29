# DATE: 4/12/22
So, i [had installed](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#2-install-wsl) ubuntu a few months back. </br>
Now that i am learning C language, i wanted to make sure the right packages are installed in linux for C language so that i can practice better. </br>
So i typed `sudo apt-get update` on my command prompt to install packages that were missing. </br>
Once that was done, `sudo apt-get install build-essential` to install additional packages and to upgrade a few old ones. </br>
gcc -v and g++ -v, gcc: GNU Cross Compiler, g++ GNU C++ Compiler. GNU: GNU's not UNIX. We got to know that these compilers were already built in. </br>


1. While writing a program in C, you must write it in a file with extension ".c". 
2. To compile the file in linux, type `gcc <filename>.c`
3. This will create a executable file called a.out if there is no error in program. Actually <filename>.c is a non-executable file. a.out is the executable file in binary form which the computer can understand easily. In windows, it is actually a .exe file which is executable.
4. To run a.out file type `./a.out`. This will run the file and display whatever the program has to.
5. What if I type `./<filename>.c` ? well that's an error bcoz it is a non-executable file. 
6. If you ever get a error, it will be in this format: main.c:4:1: warning: return type defaults to ‘int’.
  </br>
  
# DATE: 11/12/22
1. When you type `ls` in the terminal, texts appear in different colours. Blue indicates that it is a directory, white indicates that it is a file. Apart from this, how do you identify whether it is a file or a directory if you are given a black and white display screen? Type `ls -la` in your terminal. Now a detailed list will appear with each column representing something. </br>
![screenshot_45](https://user-images.githubusercontent.com/114285027/207869899-807c6ae5-ac40-461c-9470-d4a38e3735f6.png) </br>
Now 'd' actually stands for "directory", 'r' for read, 'w' for write, 'x' for execute and '-' for file.
</br>
2. Now suppose, I get an error in my code in a particular line, how do I open my file to go to that exact line? Type `vim <filename> +<line number>`. 
</br>
3. Suppose, I want some default changes whenever I open a file like, adding line no.s, changing color of text etc. Type `vim ~./vimrc` and write whatever commands you like. This will write the changes and whenever you open any file, these changes will already take place.
</br>


# DATE: 13/12/22
1. Basic structure of a program:- 
```C
   /* Documentation Section */
   /* Link Section */
   /* Global Declaration */
   Main Function()
   {
   Declaration statements; 
   Executable statements;
   }
  User-defined functions()
   {
 ......
   }      
 ```
2. Header files contain many functions which if not included, you will not be able to use the function. So, before using a function, you have to include the respective header file. And, for that we use the syntax: `# include` . '#' is called the pre-processor. 
</br>
3. In C, scanf is the reading statement and printf is the writing statement. Accepting values from the keyboard is called reading the values. 
</br>
4. My second program "Adding 2 no.s" .</br>
 
   ```C
   # include <stdio.h> 
   int main()   
   {   
   int x,y,sum;    
   printf("Enter 2 no.s");   
   scanf("%d%d",&x,&y);   
   sum=x+y;   
   printf("Sum=%d", sum);   
   }   
   ```
   5. What is this '%d' that i have written here? It is basically a format specifier/ conversion code to accept integer values. Similarly for decimal values, '%f' is used and for character, '%c' is used. '&' is an address operator, it allots memory to variables. 
   6. Program to compute simple interest:-
   ```C
   # include <stdio.h> 
   int main()
   {
   float p,r,t,si;
   printf("Enter principle amount, time and rate of interest\n");
   scanf("%f%f%f",&p,&r,&t);
   si=p*r*t*0.01;
   printf("Simple interest=%f",si);
   }
   ``` 
   </br>
   
   # DATE : 20/12/22
   1. c = 5*(f-32)/9; Here we can't multiply by 5/9 because in C, integer division truncates(fractional part is discarde). 5/9 would be truncated to 0. A decimal point indicates it is floating point. Therefore, 5.0/9.0 won't be truncated to 0. Here, if 'f' is float, then 32 will be automatically converted to 32.0 . </br>
   2. printf("%3d%6d\n",a,b); This statement prints first no. of each line in a field three digits wide and the second in a field six digits wide, like: 
        0       -17  </br>
       20        -6 </br>
       40         4 </br>
      100        37  </br>
  Now, suppose 6.0 was 6.1, this would print even 1st digit after the decimal point with at least 6 characters wide. </br>
  
  3. %d : print as decimal integer </br>
     %6d : print as decimal integer, at least 6 characters wide.</br>
     %f : print as floating point.</br>
     .3f : print as floating point, 3 characters after decimal point, but width is not constrained. </br>
    printf also recognises %o for octal, %x for hexadecimal, %c for character, %s for character string and %% for % itself.
   
   4. SYMBOLIC CONSTANTS : </br>
            
        #define line defines a symbolic name or symbolic constant to be a particular string of characters.  `# define Name replacement text `</br> . </br>In every occurance of Name, it will be replaced by replacement text. </br>Replacement text can be any sequence of characters, not just numbers. </br>`# define passwd 1234`. There is no semicolon at the end of # define line. </br>
     
  5. getchar() and putchar():- getchar() is used to read a character and putchar() is used to print a character.
  </br>
  
  # 27/12/22
  1. EOF = End of File and it has a value = -1 . If I replace EOF with -1, everywhere in a given prgm, the prgm will be totally valid. 
  2. A simple <ins>file copying</ins> program:- 
  ```C
# include <stdio.h>
 int main()
 {
 int c;
 while((c=getchar())!=EOF)
 putchar(c);
 }
 ```
 3. A simple <ins>character counting</ins> program:-
```C
# include <stdio.h>
int main()
{
int c,nc;
while((getchar())!=EOF)
++nc;
printf("No. of characters: %d",nc);
}
```
Using for loop:- 
```C
# include <stdio.h>
 10 int main()
 {
 int nc;
  for(nc=0;getchar()!=EOF;++nc)
  ; //this semicolon is there for a reason becoz in C, for loop should have a body and this semicolon is satisfying that
  printf("%d",nc);
 } 
 ```
 
4. A simple <ins>line counting</ins> program:- 
```C
# include <stdio.h>
int main()
{
int c,nl;
while((getchar())!=EOF)
if(c=='\n')
++nl;
printf("No. of new lines: %d",nl);
}
```
</br>

# 3/1/23
## Data-types in C:-
```mermaid
graph TD
A[DATA TYPES] --> B[INT </br> Size: </br> Max value: </br> Min value: </br>];
A --> C[DOUBLE </br> Size: </br> Max value: </br> Min value: </br>];
A --> D[CHAR </br> Size: </br> Max value: </br> Min value: </br>];
A --> E[FLOAT </br> Size: </br> Max value: </br> Min value: </br>];
A --> F[SHORT </br> Size: </br> Max value: </br> Min value: </br>];
A --> G[BOOL</br> Size: </br> Max value: </br> Min value: </br>]; 
```

# 8/1/23
1) Does a function have to return a value? Can you think of a function which accepts a value and doesn't return anything? scanf? printf? Well, these functions look like they don't return anything, but they do return something. Check out this line:
int count=printf("Enter a no:\n"); What value do you think the variable count stores? It stores 12 because there are 12 characters inside the printf statement. printf returns 12 to the compiler saying that a certain amount of space should be allocated for storing the characters in a character array. Similary scanf also returns something. Check out what it returns.We need to ask ourselves two questions when we come across such functions: What does the function return and why is it important?</br> 
2) We see `return 0` at the end of every main function. What is its significance? Why only 0 and not any other number? `return 0` at the end of the main file signifies that everything so far in the main function went fine and compiler assumes that the user knows what he had written in the code and therefore clears some of the memory. Suppose I return 1 or 2 or some other number, the compiler assumes that the user needs to manipulate something and knows what he is doing therefore, doesn't clear memory.</br>
3) To indent a program in liux, type `indent -kr <filename>` in the terminal. You can create your own vim plugin to autoindent your prgm. </br>
4) Scope of variables:- A variable declared inside a function has limited scope, only that function can access it and it cannot be accessed outside the function. Same goes with variables declared inside a loop. </br>
5) echo $? and operating system error codes. </br>

# 9/1/23
1) RECURSION:- When a function calls itself. </br>
## Write a program to print "Hello World!" 5 times.
```C
void printHW(int count)
{
if(count==0)
{
return 0;
}
printf("Hello World!");
printHW(count-1);
}
```
</br>
## Write a program to find sum of first n natural no.s
```C
# include <stdio.h>
int sum(int n);
int s=0;
int main()
{
printf("Sum is: %d", sum(5));
return 0;
}
int sum(int n)
{
if(n==1)
{
return 1;
}
s=n+sum(n-1);
}
```
</br>

Try for factorial of a number. </br>

2) Properties of a function:- 
- Function can return only one value at a time.</br>
- Changes to parameters in function don't change the values in calling function because a copy of argument is passed to the function. </br> 

3) Difference between Argument and Parameter:- </br> |Argument|Parameter|</br>|:-------|:-------|</br>| Values that are passed in function call | Values in function declaration and definition|</br>|Used to send< value|Used to recieve value|</br>| Actual parameters | Formal parameters |
</br>

# 10/1/23
1) String constant(String literal)-> Sequence of zero or more characters surround by double quotes. The double quotes only serve to delimit. String constant is an array of characters and has null character '\0' at end, therefore storage required is one more. 
2) Standard library function `strlen()` returns the length of its character string argument s, excluding the terminal '\0'. 
3) We must know the difference between 'x' and "x". The former is an interger and the latter is a string constant. 
4) Enumeration constant:- Enumeration is a list of constant integer values, like:- enum boolean{NO,YES}; NO has the value 0 and YES has the value 1. Suppose not all values are specified, unspecified values continue the progression from the last specified value. For example:- enum ASCII{A=65,B,C,D..........Z}; Here, B is 66, C is 67 and so on.
5) Name in different enumerations must be distinct. 
6) Values need not be distinct in the same enumeration. 
</br>

# 26/1/23
1) Write a program in C to print nth term of the fibonacci series using `for loop` . Fibonacci series: 0,1,1,2,3,5,8,13......
```C
# include <stdio.h>
int main()
{
int im2=0;
int im1=1;
int num,ith;
printf("Enter the nth term of fibonacci series to be printed: \n");
scanf("%d",num);
for(int i=3;i<num;i++)
{
ith=im2+im1;
im2=im1;
im1=ith;
}
printf("nth term of the fibonnaci series is: %d",ith);
printf("\n");
}
```
</br>

2) Write a program to print Pascal's triangle upto 'n' rows. 
 ```C
   # include <stdio.h>
   int factorial(int n);
   int f=1;
   int combinations(int n,int r,int nmr);
   int main()
   {
     int rows;
     printf("Enter no. of rows of Pascal's triangle that need to be printed:\n");
     scanf("%d",&rows);
    printf("Pascal's triangle: \n");
    for(int n=0;n<rows;n++)
    {
      for(int r=0;r<=n;r++)
      {
        int nfact=factorial(n);
        int rfact=factorial(r);
        int nminusr_fact=factorial(n-r);
        int c=combinations(nfact,rfact,nminusr_fact);
        printf("%d \t",c);
      }
      printf("\n");
    }
    int factorial(int n)
    {
    if(n==0)
    {
      return 1;
    }
    f=n x factorial(n-1);
   }
  int combinations(int n,int r,int nmr)
  {
    int ncr=n/(r x nmr);
    return ncr;
  }
  }
  ```
  
