# DATE: 4/12/22
So, i [had installed](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#2-install-wsl) ubuntu a few months back. </br>
Now that i am learning C language, i wanted to make sure the right packages are installed in linux for C language so that i can practice better. </br>
So i typed `sudo apt-get update` on my command prompt to install packages that were missing. </br>
Once that was done, `sudo apt-get install build-essential` to install additional packages and to upgrade a few old ones. </br>
gcc -v and g++ -v, gcc: GNU Cross Compiler, g++ GNU C++ Compiler. GNU: GNU's not UNIX. We got to know that these compilers were already built in. </br>


1. While writing a program in C, you must write it in a file with extension ".c". 
2. To compile the file in linux, type `gcc <filename>.c`
3. This will create a executable file called a.out if there is no error in program. Actually <filename>.c is a non-executable file. a.out is the executable file in binary form which the computer can understand easily.
4. To run a.out file type `./a.out`. This will run the file and display whatever the program has to.
5. What if I type `./<filename>.c` ? well that's an error bcoz it is a non-executable file. 
6. If you ever get a error, it will be in this format: main.c:4:1: warning: return type defaults to ‘int’.
  </br>
  
# DATE: 11/12/22
1. When you type `ls` in the terminal, texts appear in different colours. Blue indicates that it is a directory, white indicates that it is a file. Apart from this, how do you identify whether it is a file or a directory if you are given a black and white display screen? Type `ls -la` in your terminal. Now a detailed list will appear with each column representing something. </br>
![screenshot_45](https://user-images.githubusercontent.com/114285027/207869899-807c6ae5-ac40-461c-9470-d4a38e3735f6.png)
Now 'd' actually stands for "directory", 'r' for read, 'w' for write, 'x' for execute and '-' for file.
2. Now suppose, I get an error in my code in a particular line, how do I open my file to go to that exact line? Type `vim <filename> +<line number>`. 
3. Suppose, I want some default changes whenever I open a file like, adding line no.s, changing color of text etc. Type `vim ~./vimrc` and write whatever commands you like. This will write the changes and whenever you open any file, these changes will already take place.
</br>


# DATE: 13/12/22 (in college)
1. Basic structure of a program:- 
   /* Documentation Section */</br>
   /* Link Section */</br>
   /* Global Declaration */</br>
   Main Function()</br>
   {</br>
   Declaration statements; </br>
   Executable statements;</br>
  }</br>
  User-defined functions()</br>
  {</br>
 ......</br>
 }</br>
 
 2. Header files contain many functions which if not included, you will not be able to use the function. So, before using a function, you have to include the respective header file. And, for that we use the syntax: `# include` . '#' is called the pre-processor. 
 3. In C, scanf is the reading statement and printf is the writing statement. Accepting values from the keyboard is called reading the values. 
 4. 
