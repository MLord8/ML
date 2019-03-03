All of the optimization algorithms are performed using the software package, ABAGAIL.

ABAGAIL can be found here: https://github.com/pushkar/ABAGAIL

The dataset can be found here: https://github.com/MLord8/ML/tree/master/assignment2/ABAGAIL/src/prj2/datasets

Installing ABAGAIL:
- Install Java 8 SDK from here http://www.oracle.com/technetwork/java/javase/downloads/index.html
- Install Ant http://ant.apache.org/
- Clone or download source files from Git
- Go with command line to where the build.xml file is and run: ant (note: the ant executable should be in your path somehow if you installed ant correctly.. so will java and javac)
- Now run your scripts

Running the code:
- Go to the ABAGAIL folder in a command line program
- Type 'ant' to compile the project

(For Part 1 experiments)
- Run this command: 'java -cp ABAGAIL.jar prj2.SpambaseTest', then choosing the parameters for optimization algorithm to use and the parameters needed (this can be found in SpambaseTest.java in the prj2 file)
- The output of the experiment will be written to $AlgorithmName$.csv

(For Part 2 experiments)
- Select a test file from src/opt/test
- Run this command: 'java -cp ABAGAIL.jar opt.test.SomeTest', or whatever the file you want to run is
- The output of the file will be written to $SomeTest$.csv