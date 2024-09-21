# Git-tags

Q. How to place image (.png, .jpeg ,etc)inside repository ?

Answer 
step 1 . first clone repository in local directory 
         git clone https://github.com/username/repository.git
         
step 2 . inside clonned repository make sure theres a directory available that contains images otherwise by default images takes place in remote repository main directory not into specific directory where we want to list images 
         cd repository 
         or cd repository | mkdir Forimages 
            cd Forimages 
          
step 3 . from remote repository exact directory try to list available files 
         ls
         
step 4 . use copy command to copy image from local system directory to remote repository or current working directory 
           cp /path/to/your/image.png . 
           for example in c or d or e drive has images so , it should looks like 
           cp /c/Users/nameofdirectory/filename .
           or   cp /c/Users/nameofdirectory/directoryname/filename /c/Users/Directoryname/LocalDirectory-name/clonnedRepository-name/repository/
      OR 
         use move command to move image from local system directory to remote repository or current working directory 
           mv /path/to/your/image.png .
           mv /c/Users/Directory/sub-Directory/image.png /c/Users/Directory/sub-Directory/Directory/localDirectory-name/clonned-Repository/repository/

NOTE : image file with actuall extension

step 5 . recheck the remote repo directory for confirmation before staging changes 
         ls 
step 6 . try to stage the specific changes made in current working directory or try to stage over all changes directly 
         git add directory/image.png 
         or git add .
step 7. check the status of staging or changes made , commit these changes and push these changes into origin main /remote repository 
         git status 
         git commit -m"message"
         git push origin main   # replace main with branch name if required 
         
Note : we can copy or move image or files from directory to directory but not directory to file either we can replace file with new file which has .png , ,jpeg ,etc extensions 

step 8. Now check manually in remote repository or check with clonned repository whether it has images available or not ? still not working so retry same steps but carefully use the 
        absolute path for moving or copying files , recheck syntax of the directory. 
