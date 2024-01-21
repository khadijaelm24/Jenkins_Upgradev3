# Hello World Plugin Demo
Build a simple "Hello, World" plugin using a template.


# Install Java and Maven 
-- Java is Already Installed


## Install Maven
Download Maven Tar from https://maven.apache.org/download.cgi
Unzip tar - tar -xvzf <file_name>
move to /opt -- mv apache-maven****** /opt/


# Add the following lines to the user profile file (.profile).
M2_HOME='/opt/apache-maven-******' /opt/apache-maven-3.9.4
PATH="$M2_HOME/bin:$PATH"
export PATH

Relaunch the terminal or execute source .profile to apply the changes.
Execute mvn -version command


# Create a local folder for the source code:
(if the environment is well set up, we want to start from this step)
mkdir -p hello-world
cd hello-world


# Create a plugin from the Jenkins templates:
(the main command of plugin's creation)
mvn -U archetype:generate -Dfilter="io.jenkins.archetypes:"

mvn verify
mvn package

Move .hpi file from targets to Jenkins Plugin Directory
Retstart the Jenkins Service

LogIn Jenkins and follow below steps -

- New freestyle job
- Add "Hello World" build step
- Run, check console
