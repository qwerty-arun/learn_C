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
 } */
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

