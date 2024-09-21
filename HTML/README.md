HOW images can be used with files in the repository or how images rendering with file context ?

To use images with file , first make sure use proper syntax to copy or move images within a directory , after that use logical implementation for example 

step 1. clonning remote repository where you want to place images and go there 
       git clone https://github.com/username/repository.git
        cd repository

step 2. create folder /directory where actually images takes place 
       mkdir html 

step 3. copy image path from local directory to remote directory 
    cp /path/to/your/image.png html/
   or cp /path/to/your/image.png .
step 4. recheck that image copied or not , now create index.html 
      touch html/index.html
      vim html/index.html
step 5. Add image tag <img> in htmlfile like below 
    <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Display</title>
</head>
<body>
    <h1>My Image</h1>
    <img src="image.png" alt="Description of the image">
  OR  
    <img src="../image.png" alt="Description of the image">  ,when image available in different directory and index.html file present in diff. directory but both files available in same main directory 
</body>
</html>
step 6. now add these changes and push the changes 
   git add html/  or git add .
   git commit -m "Add HTML file and image"
   git push origin main
step 7. now try logical implementation works or not 
   manually open html directory goto index.html double -click it ,so image rendering on web-page 
   or open html directory with bash now try to operate with start html/index.html  or start index.html 

