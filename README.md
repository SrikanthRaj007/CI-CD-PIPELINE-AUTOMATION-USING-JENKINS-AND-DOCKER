CI CD PIPELINE AUTOMATION USING DOCKER AND JENKINS!

PROCEDURE:
  Step 1: Create a Project directory
  For exmple:  I created a project directory in ubuntu called 'Jenker' which is jenkins+docker ! 😊
  
  Step 2: Add files for your application
  For example: I create a basic python-flask code
  
  Step 3: Initialize git and add the remote for your github repository
  command: 
          git init (to initialize git)
          git add <filename> or git add . (to add the files)
          git commit -m "your update or commit status" (to save the files with a save-message)
          git push <remote-name> <branch-name>
          
  Step 4: Install jenkins on ubuntu 
  Here I pulled a jenkins image to docker and create a container for the jenkins image

  command: 
  
  docker run -d \
  -p 8080:8080 \
  -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  --name jenkins \
  jenkins/jenkins:lts

  the above command will run a jenkins container

  Step 5: Now run the jenkins website
  command: 
  docker run -d \
  -p 8080:8080 \
  -p 50000:50000 \
  -v jenkins_home:/var/jenkins_home \
  --name jenkins \
  jenkins/jenkins:lts

Step 7: Now got to "https://localhost:8080"
Create new username and password

Step 8: Now go to jenkins-> New item-> Enter a item name-> Select pipeline-> Now create item

Step 9: After creating the item select the 'Pipeline Script'

Here there are two methods to enter your pipeline script either manually type your script there (or) create a Jenkinsfile on your project directory itself

Step 10: Finaly build your job in jenkins
Check console output for the success message 

Step 11: If it shows any error 

add a docker group in jenkins and create a credentials for docker also.

Finally your job is completed successfully.
