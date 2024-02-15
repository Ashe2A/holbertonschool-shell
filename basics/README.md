This project is exhibiting basics of Shell scripts (bash) :

# General notices before tasks
* The ```#!/bin/bash``` header, also known as "shabang" (= sharp (#) + bang (!)), is used to define the file as a bash script, and not a binary file. Scripts are executable by using the ```./file_name``` syntax;
* Due to incompatibility between the ```echo``` command and the shabang header, it is essential to use a file editor, such as ```emacs``` or ```vi```/```vim```;
* Due to these very editors automatically implementing an empty line upon saving a file, there is no need to add one;
* Due to owner of the file not necessarily corresponding to the user of the testing machine, there is a need to give an execution permission to users in the scripts' files. This is all done with the following command (there is no need to understand that command for now) : ```chmod u+x N-file_name```.


# 0. Where am I?
The ```0-current_working_directory``` script displays the absolute path of the current directory upon execution.

~~~
#!/bin/bash
pwd
~~~

* The ```pwd``` (Print Working Directory) command prints the current working directory of the active shell client.


# 1. What's in there?
The ```1-listit``` script lists the files and directories of the current directory it's launched in.

~~~
#!/bin/bash
ls
~~~

* The ```ls``` (LiSt) command, without any parameters, lists the files and directories contained in the working directory.
   

# 2. There is no place like home
The ```2-bring_me_home``` script redirects the current directory to the home directory, usually accessible with the variable ```$HOME```.

~~~
#!/bin/bash
cd
~~~
   
* The ```cd``` (Change Directory) command, without any parameters, change the working directory to the default home one.


# 3. The long format
The ```3-bring_me_home``` details the files and directories of the current directory it's launched in. It is called "long format".

~~~
#!/bin/bash
ls -l
~~~

* The ```-l``` (Long) option in the ```ls``` command specifies details on the listed files and directories;
* ```-l``` can be replaced by ```-long```.


# 4. Hidden files
The ```4-listmorefiles``` details the files and directories, including hidden ones, of the current directory it's launched in.

~~~
#!/bin/bash
ls -la
~~~

* The ```-a``` option in the ```ls``` command includes hidden files and directories;
* Options can be combined into one (```-la```/```-al```), or separate (```-a -l```/```-l -a```) parts.

# 5. I love numbers
The ```5-listfilesdigitonly``` details the files and directories, including hidden ones, of the current directory it's launched in. User and group IDs of the content's owner are displayed numerically.

~~~
#!/bin/bash
ls -na
~~~

* The ```-n``` (Numerics) option in the ```ls``` command converts user and group IDs to numerical;
* As ```-n``` needs long format to be effective, it already makes ```-l```'s work. Hence, the latter's use is optional;
