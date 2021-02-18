# Git Automated Deployment using the Git Hooks
Follow this steps to use the post-receive hook:  
 1. Copy the ```post-receive``` file and paste it in the Hooks directory in your bare repo.  
 **Note:** you should not change the file name.  

 2. Edit the file as follows in line 8:   
 * Change the value of the ```git --work-tree``` environmental variable to match your working directory:  
 * Change the valve of the ```git-dir``` environmental varible to match the bare repo's directory.  

 3. Make the file executable:  
 ```bash
 chmod +x post-receive
 ```
 
 4. Test the hook  
 * Modify a file e.g a ```index.html``` file in your working directory.  
 * Add the file to the staging area and commit the changes

 ```bash
 git add <filename>
 git commit -m "some message"
 ```
 * Push the changes to the bare repo in the server.  
 ```bash
 git push <remote> <branch>
 ```
 * Visit your web server ip address in your browser  to see the changes you made to the ```index.html``` file.