Hi all!

As promised, apart from the repository we shared in the beginning of the bootcamp [[0][0]], here follow some resources for revising what we have seen so far along with brand new concepts.

Today's presentation was based on instruction material Software Carpentry volunteers have prepared, which is shared in the wiki page [[1][1]]. An older version [[2][2]] covers more ground in video as well as in slides and prose. Nevertheless, Software Carpentry's FAQ [[3][3]] provides a lot of information when it comes to its mission, how it works and even how you can contribute.

THE ultimate Bash shell scripting guide [[4][4]] covers literally everything you might need when writing advanced scripts.

Please don't hate me for that, but if you feel like advancing in the philosophy of UNIX, Wikipedia has a great article on that [[5][5]].

Software Carpentry also recommends reading material in the relative page [[6][6]].

Finally, there is the LinkSCEEM General User Meeting Etherpad [[7][7]] with notes taken throughout the bootcamp.

More to come tomorrow with a new way of sharing and collaborating in programming with Source Version Control.

Thank you,  
misaakidis

<hr />


## KEY POINTS
### Files and Directories
  * The filesystem is responsible for keeping directories and files on the disk.
  * Information is stored in files, which are stored in directories, forming a directory tree structure.
  * / when in the beginning of a path, represents the root directory and makes the path absolute and unique no mater which is the current working directory.
  * When a path is not starting with / the path is relative and specifies a location starting from the current working directory.
  * There are special references for the working directory (.), its parent directory (..) and the user's home directory (~).
  * UNIX does not have a trash bin, files deleted with rm cannot be recovered.

### Pipes and filters
  * *command > file* redirects a command's output to a file
  * *first command | second command* is a pipeline: the output of the first command is used as the input to the second.
  * Filters are commands (like *sort*) that manipulate a file content but do not alternate the file itself.
  * The use of pipes and filters fits well with the general idea in UNIX of programs doing simple tasks combined together for complex problem solving.

### Shell Scripts
  * A sequence of commands can be stored in a file (using the .sh file extension is a good practice) and then can be executed as a script.
  * Commands accept options (flags); usually a letter following the - symbol.
  * In order to access a variable, the dollar symbol is used (*$variable*).
  * Variables passed to a script can be accessed as $1, $2 etc.
  * One can refer to all the shell script's command-line parameters with $*

### General advice
  * Using shell is a great solution when it comes to automating repetitive tasks or working from remote machines.
  * It's a useful habit to avoid spaces, special characters like * and ? (which act as wildcard characters) in file names. When including the date in the filename, following the YEAR-MONTH-DAY format (*2014-06-25*) helps with sorting files later on.
  * Use friendly names for variables and include comments in your scripts, it will be a great help when reading them after some time, or sharing them with others.
  * Using *echo $variable* within a loop can help you spot problems before actually executing it.
  * Also quoting variables in a script (*"$variable"*) can protect your scripts from filenames which include spaces and so on.
  * The up arrow key brings the previous commands in the shell. Control-R (^R) is also a way to search in your command history.

## COMMANDS
With great power comes great responsibility. Use them wisely :)

    whoami      returns the logged in user
    pwd         print working directory
    cd          change directory
    ls          listing (show files and directories)
    mkdir       create directory
    cp          copy (files or directories)
    mv          move files or directories
    rm          remove a file (PERMANENT!) (-r for recursive deletion)
    cat         concatenate files and print on the standard output
    wc          print newline, word, and byte counts for each file
    sort        sort lines of text files
    head        output the first part of files
    tail        output the last part of files
    echo        display a line of text
    history     displays the command history of the shell
    grep        search in text (print lines matching a pattern)
    find        search for files in a directory hierarchy


<br>
Remember **man** shows the manual page of a command, with a brief explanation of how it works, list of arguments and examples of use.

    man [command]
    
is the way to use it.

<br>
The use of wildcard characters can match many files. Such characters are:

    *           match any sequence of characters
    ?           match a single character

<br>
Repetitive tasks can be automated with for loops:

    for variable in *.txt
    do
        echo $variable
    done

    


## LINKS  
[0]: https://github.com/misaakidis/swc-shell-git
[1]: http://software-carpentry.org/v5/
[2]: http://software-carpentry.org/v4/
[3]: http://software-carpentry.org/faq.html
[4]: http://www.tldp.org/LDP/abs/html/
[5]: https://en.wikipedia.org/wiki/Unix_philosophy
[6]: http://software-carpentry.org/v5/bib.html
[7]: https://linksceemgum.etherpad.mozilla.org/1
  * \[0] https://github.com/misaakidis/swc-shell-git
  * \[1] http://software-carpentry.org/v5/
  * \[2] http://software-carpentry.org/v4/
  * \[3] http://software-carpentry.org/faq.html
  * \[4] http://www.tldp.org/LDP/abs/html/
  * \[5] https://en.wikipedia.org/wiki/Unix_philosophy
  * \[6] http://software-carpentry.org/v5/bib.html
  * \[7] https://linksceemgum.etherpad.mozilla.org/1