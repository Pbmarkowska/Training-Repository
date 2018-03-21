## Command line is a text interface for the computer.

1. Root
2. Directory - katalog
3. Folder
4. File
5. *- wildcard
6. $ - shell prompt
7. I/O - input/output

### Basic commands ###

 - **pwd** - print working directory == gdzie aktualnie jestem<br>
 - **cd** - change directory + path == mogę zmienić directory podając konkretną ścieżkę<br>
 - **ls** - mogę wylistować wszystkie pliki w directory<br>
 - **cd ..** - mogę przenieść się do directory o jeden poziom wyżej + mogę jednocześnie zmienić directory podając konkretną ścieżkę, mogę też się przenieść dowolną ilość poziomów wyżej: cd ../../ itd. <br>
 - **mkdir** - make directory <br>
 - **touch** - tworzy nowy plik w aktualnym katalogu
 - **ls -a** mogę wylistować nawet pliki ukryte, oznaczone kropką **.** <br>
 - **ls -l** mogę wylistować w długim formacie w formie tabelki, w tabelce są informacje o dostępie do pliku, liczbie podkatalogów (dzieci), właścicielu pliku <br>
 - **ls -t** mogę wylistować pliki i katalogi uszeregowane według daty <br>
 - **ls -alt** mogę wylistować pliki i katalogi w długim formacie w formie tabelki uszeregowane według daty <br>
 - **cp** mogę kopiować pliki i katalogi, mogę kopiować pliki i katalogi i umieszczać je w danej lokalizacji: <br>
 ```cp katalog1/nazwa.txt /katalog2```<br>

 - **cp * /lokalizacja** mogę skopiować wszystkie pliki w danej lokalizacji i umieścić je w danej lokalizacji <br>
 - **cp m*.txt /lokalizacja** mogę skopiować wszystkie pliki zaczynąjące się na m i umieścić jej w danej lokalizacji <br>
 - **mv plik.txt lokalizacja/** mogę przenosić pliki do danej lokalizacji<br>
 - **mv plik.txt innyplik.txt** mogę zmienić nazwę pliku przenosząc jeden plik do drugiego<br>
 - **rm** mogę usunąć pliki i katalogi<br>
 - **rm -r** mogę usunąć pliki i katalogi oraz ich dzieci, **r** od recursive

 ### I/O input/output redirection ###
 Through redirection you can direct the input and output of a command to and from other files and programs, and chain commands together in a pipeline

 1.**standard input**, abbreviated as stdin, is information inputted into the terminal through the keyboard or input device. <br>
 2.**standard output**, abbreviated as stdout, is the information outputted after a process is run. <br>
 3.**standard error**, abbreviated as stderr, is an error message outputted by a failed process. <br>

### Redirection commands ###
Example:<br>
```$ echo "Hello" > hello.txt``` <br>
 - The **>** command redirects the standard output to a file. <br>
```cat hello.txt``` <br>
The **cat** command outputs the contents of a file to the terminal.<br>
 - **>>** takes the standard output of the command on the left and appends (adds) it to the file on the right.<br>
 - **<** takes the standard input from the file on the right and inputs it into the program on the left.<br>
 - **|** is a "pipe". The | takes the standard output of the command on the left, and pipes it as standard input to the command on the right. You can think of this as "command to command" redirection.<br>
 - **sort** takes the standard input and orders it alphabetically for the standard output<br>
 - **uniq** stands for "unique" and filters out adjacent, duplicate lines in a file<br>
 - **grep** stands for "global regular expression print". It searches files for lines that match a pattern and returns the results. It is also case sensitive.<br>
 - **grep -i** enables the command to be case insensitive. <br>
 - **grep -R** searches all files in a directory and outputs filenames and lines containing matched results. -R stands for "recursive".<br>

 Example: <br>
```$ grep -R Arctic /home/ccuser/workspace/geography```<br>

 - **grep -Rl** searches all files in a directory and outputs only filenames with matched results. -R stands for "recursive" and l stands for "files with matches". <br>
 - **sed** stands for "stream editor". It accepts standard input and modifies it based on an expression, before displaying it as output data. It is similar to "find and replace".<br>

 Example: <br>
```$ sed 's/snow/rain/' forests.txt```

- **s**: stands for "substitution". it is always used when using sed for substitution.
- **snow**: the search string, the text to find.
- **rain**: the replacement string, the text to add in place.

In this case, sed searches forests.txt for the word "snow" and replaces it with "rain." Importantly, the above command will only replace the first instance of "snow" on a line.

### Environment settings ### <br>
**~/.bash_profile*** is the name of file used to store environment settings. It is commonly called the "bash profile". When a session starts, it will load the contents of the bash profile before executing commands.

The ~ represents the user's home directory.<br>
The . indicates a hidden file.<br>
The name ~/.bash_profile is important, since this is how the command line recognizes the bash profile.<br>

The command source **~/.bash_profile** activates the changes in ~/.bash_profile for the current session.

### Aliases ### <br>
What happens when you store this alias in ~/.bash_profile? <br>
```alias pd="pwd"```<br>

The alias command allows you to create keyboard shortcuts, or aliases, for commonly used commands.

### Environment variables
Environment variables are variables that can be used across commands and programs and hold information about the environment.<br>
```export PS1=">> "```<br>
```export $USER="My name"```<br>

The **env** command stands for "environment", and returns a list of the environment variables for the current user.
