# DATE: 4/12/22
So, i [had installed](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#2-install-wsl) ubuntu a few months back. </br>
Now that i am learning C language, i wanted to make sure the right packages are installed in linux for C language so that i can practice better. </br>
So i typed `sudo apt-get update` on my command prompt to install packages that were missing. </br>
Once that was done, `sudo apt-get install build-essential` to install additional packages and to upgrade a few old ones. </br>
gcc -v and g++ -v, gcc: GNU Cross Compiler, g++ GNU C++ Compiler. GNU: GNU's not UNIX. We got to know that these compilers were already built in. </br>


1. While writing a program in C, you must write it in a file with extension ".c". 
2. To compile the file in linux, type `gcc <filename>.c`
3. This will create a executable file called a.out if there is no error in program. Actually <filename>.c is a non-executable file. a.out is the executable file in binary form.
4. To run a.out file type `./a.out`. This will run the file and display whatever the program has to.
5. What if I type `./<filename>.c` , well that's an error bcoz it is a non-executable file. 
6. If you ever get a error, it will be in this format: main.c:4:1: warning: return type defaults to ‘int’.
  </br>
  
# DATE: 11/12/22
