# JenkinsLab3
Jenkins integration with Git
Lab 3: Integrating Jenkins with GitHub

Step 1: Install Git Plugin

Go to Manage Jenkins → Manage Plugins → Available Plugins.

Search for Git Plugin and install it.

Step 2: Connect Jenkins to GitHub

Create a new repository on GitHub.

Clone it locally and add a Jenkinsfile:

git clone https://github.com/yourusername/jenkins-project.git
cd jenkins-project
echo "pipeline { agent any; stages { stage('Build') { steps { echo 'Building from GitHub' } } } }" > Jenkinsfile
git add .
git commit -m "Added Jenkinsfile"
git push origin main

In Jenkins, create a Pipeline Job, select Pipeline from SCM, and enter the GitHub repo URL.

Click Save and run the build.
