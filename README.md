Set up a CI/CD pipeline with Jenkins and an EC2 instance. The website needs to
be launched via the EC2 public IP. Name: R.Vedha Dharshini
Roll No: 21ISR054
Steps:
1. Creating an AWS EC2 INSTANCE:
 Sign up to Aws console Login
 After signing up go to EC2 dashboard
 Click “Launch Instance”
Connect to the Ec2 Instances:
 Open command Prompt in which you have pem files
 Give the pem file with *
 Give the entire ssh command
Step: 3 After connecting ec2 instance Go to the Jenkins.io and redhat.io
 At First Install the Java Version.
Now Install The Jenkins Using The command sudo yum install Jenkins
After Installing the Jenkins start the Jenkins Command:
Copy The public Ipv4 Address of your Instance You Will Get this Page as an
output:
After Giving The Jenkins Password it will ask for customize Jenkins
After Installing Jenkins It Will user Forms
After Filling This Form it shows the url and ask for save and finish.
After Installing The Jenkins We need to a setup a CICD pipeline.  Go The Jenkins Dashboard page Using your Username and Password:
 Click the New Item from the selected list select the Freestyle Project
Add Git hub Link to the source code Management:
Click on Build Tab and select build step as ‘Invoke top-level Maven targets‘.
After Clicking Ivoke top-level Maven targets:
Now go back to Configure and visit the ‘Post Build Actions‘ tab. Click the drop- down and select ‘Archive the Artifacts‘ from the options. In the field, write down
‘**/*.war‘ as shown in the image below. It will fetch all the directories and get the
war file wherever it is present. Click again on Build Now button, and you will now
see the Artifacts in the Jenkins dashboard.
Click on the Available tab and search for the ‘Deploy to Container‘ plugin. Select
the plugin and click on the ‘Install without restart‘ button.
Step 16) Now click on the ‘Add Container‘ button and select the ‘Tomcat 9.x
Remote‘ as we are using version 9 of the Tomcat. Fill in the URL of the same
virtual machine with the new port number 8090. On the credentials drop-down
button, select Jenkins.
In this window, fill in the username and password that we have used in the
‘tomcat-users.xml‘ file (in Step 10). Fill in the ID, description and click on the
button ‘Add‘.
Final Web Page Output is:
