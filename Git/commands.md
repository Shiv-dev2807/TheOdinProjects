1. First Time (New Project + New GitHub Repository)

    git init

    git add .

    git commit -m ".........."

    git remote add origin git@github.com:YOUR_USERNAME/my-project.git

    git branch -M main

    git push -u origin main
    

2. Continuing Existing Project

    git add . && git commit -m "update" && git push


==============================================================

->Commands related to a remote repository:{
    git clone git@github.com:USER-NAME/REPOSITORY-NAME.git
    git push or git push origin main (Both accomplish the same goal in this context)
}

->Commands related to the workflow:{
    git add .
    git commit -m "A message describing what you have done to make this snapshot different" 
    or 
    git commit -> (This opens an editor where you can write: Subject line Body description)
}

->Commands related to checking status or log history{
    git status
    git log
}

{
    git blame shows who last changed each line of a file and when.
    git rebase is used to move or rewrite commit history.
}
==============================================================