# Installing PySpark on a Raspberry Pi 4

This guide will walk you through the steps required to install PySpark on a Raspberry Pi 4 running the Raspberry Pi OS.
## Step 1: Install Java
PySpark requires a Java runtime environment (JRE) to be installed on your Raspberry Pi 4. If you don't already have Java installed, you can install it by running the following command in a terminal:

`sudo apt-get install default-jdk`


To set the JAVA_HOME environment variable on a Raspberry Pi 4, you can follow these steps:

1. Check if Java is already installed on your Raspberry Pi by running the command `java -version`. If Java is installed, you will see the version information printed on the console. If Java is not installed, you can install it by running the command `sudo apt-get install default-jdk`.

2. Once Java is installed, determine the path to the Java installation directory by running the command `sudo update-alternatives --config java`. This will display a list of available Java installations on your system along with their paths. Note down the path to the Java installation that you want to use.

3. Open the `.bashrc` file in a text editor by running the command `nano ~/.bashrc`.

4. Add the following lines at the end of the file:
`export JAVA_HOME=/path/to/java/installation`
`export PATH=$JAVA_HOME/bin:$PATH`

Replace `/path/to/java/installation` with the path to the Java installation directory that you noted down in step 2.

5. Save the changes and exit the text editor.

6. Reload the `.bashrc` file by running the command `source ~/.bashrc` or by opening a new terminal window.

7. Verify that the JAVA_HOME environment variable is set correctly by running the command `echo $JAVA_HOME`. The command should print the path to the Java installation directory that you set in step 

After you have set the JAVA_HOME environment variable, you should be able to run your PySpark application on your Raspberry Pi 4 without encountering the "JAVA_HOME is not set" error.

## Step 2 Create a Virtual Environment using “virtualenv”

### Installing “virtualenv”
Now go to your project directory and open a terminal 
Install virtualenv using command `pip install virtualenv`
### Create virtualenv
Once it is installed successfully, a virtual environment with name pyspark (you can use any name that you want)
To create a virtual environment in the current directory, type `virtualenv pyspark` in the terminal
### Activating virtualenv
To activate the env that you just created type `source activate pyspark/bin/activate` in the terminal

## Step4 Installing PySpark l
To install pyspark type `pip istall pyspark` in the terminal

## Step4 Installing jupyter-lab
To install jupyter-lab type `pip install jupyterlab` in the terminal 

## Step5 Launching jupyeter lab
Type jupyterlab ina the terminal




