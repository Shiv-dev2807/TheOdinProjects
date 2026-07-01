CLI -> faster way to control your computer using text commands instead of clicking.

*$ shell is ready for commands*

1. whoami -> gives username

2. copy paste -> Ctrl + Shift + C / V

*USE Tab for completing the path*

3. Open in vc code -> code .

4. mkdir -> make directory (mkdir Desktop){
    mkdir shiv = creates shiv folder,
    ls -F = shows folders(dir)


    create multiple nested folders =
    mkdir -p ../project/data ../project/results

    -p = creates parent folders automatically if missing.
}

5. cd ~ -> takes u to starting or home directory

6. wget -> used for downloading from websites

7. sudo apt install -> installs applications using terminal

8. unzip -> unzips the zip,rar,etc folders

9. ls - Lists files and folders in current directory{
    ls -F -> Shows Type
    ls / -> directory
    ls * -> executables
    ls @ -> link
    ls -a -> shows all hidden files
    ls -l -> detailed info
    ls -h -> human readable sizes

    ==================================

    Help?

    ls --help (quick help)
    man ls (manual){
        navigation =
        
        arrows -> scroll
        /word -> search
        q -> quit
    }
}

10. pwd -> shows current location in the directory

11. cd -> changing directory{
    cd .. -> goes up one folder
    cd -> go home
    cd - -> go back to previous folder
}

*paths = Absolute Path = starts from **/** (ex = /Users/shiv/desktop), relative path = starts from **current** folder (shiv/desktop){
    ~ -> home directory
    . -> current directory
    .. -> parent directoy
}*

12. Click Tab -> auto complete files,folders, press tab twice shows all matches

13. Option and argument -> structure -> command -option argument (example = ls -F /{
    ls command, -F option, / argument -> list everything that is /(folder)
})

14. File Creation{
    nano draft.txt
    ctrl + O save
    ctrl + X exit


    using touch ->    touch my_file.txt
    creates empty file, Or updates timestamp if file exists

    check size -> ls -l my_file.txt
}

15. Moving Files and Renaming Files{
    mv thesis/data.txt thesis/d.txt (same folder)

    move files ->
    mv thesis/quotes.txt . (moves file out of the folder) mv can overwrite files without asking, SO use this -> 

    mv [source] [destination] rename and move for both same if destination doesnt exits? => rename
    if exists => move

    move =>
    mv -i draft.txt documents/
    rename =>
    mv -i draft.txt notes.txt
}

16. Copying Files{
    file = cp quotes.txt thesis/quotations.txt (source - destination) copies file quotes.txt to thesis with name quotations.txt
    directory = cp -r thesis thesis_backup (copy thesis directory as thesis_backup) 
    -r -> recursive needed for folders (recursivily copy the files inside the folder)

    copying multiple files = 
        cp f.txt b.txt backup/
}

17. Delete Files{
    rm quotes.txt

    rm -r thesis_backup 

    safer = rm -i file

    no recycle bin forever delete
}

*File system ideas = everything is tree structure | root = / | Home = /Users/username (directories inside directory)*

18. Wildcards {
    * -> matches many characters => *.txt -> gives all the txt files
    ? -> eaxtly 1 character => ex: ?.txt -> text file that has one character | (cat.txt tatt.txt lat.txt etc => ?at.txt => gives => cat.txt, lat.txt)
    one more example => *t*ane.pdb => middle t and end ane

    another example = {
        apple.txt
        banana.txt
        cat.txt
        notes.txt

        ls *a* = apple,banana,cat (!* can be 0)
    }
}