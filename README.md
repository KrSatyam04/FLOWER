# FLOWER
In this repo, I'm updating all the work progress and errors which I face and the solutions that I got.
I am going to work on the FLOWER project on my new MACBOOK PRO M1. I hope M1 chip don't cause some compatibility issue along the way.


# PROGRESS
## 30 April 2022
import flower as fl

## ERRORS

### 1. this operation could not be completed unable to locate a java runtime which support apt
  Solution: Install java SDK from java.com compatible with the processor (Arm64) in my case. Still I have concerns that it may cause some issue because probably it still not support m1 natively.
  
### 2. After installing Java, Still same problem
  Add path in .zshrc in home directory(or .profile, .bash_profile, .bashrc) {still not sure which comes in which case, my files has other .zsh files so I knew it .zshrc for me}
  
  add the following line in .zshrc file
  
  export JAVA_HOME=$(/usr/libexec/java_home)
  
  Confirm installation by echo $JAVA_HOME
  Expected result: /Library/Java/JavaVirtualMachines/jdk-18.0.1.jdk/Contents/Home
  
  
# 01 May 2022

## Install Tensorflow with command
  pip install tensorflow
  
## ERROR:

### ERROR: Could not find a version that satisfies the requirement tensorflow (from versions: none)
ERROR: No matching distribution found for tensorflow

Solution: Run the following command
pip3 install –-upgrade https://storage.googleapis.com/tensorflow/mac/cpu/tensorflow-1.0.0-py3-none-any.whl

Also check if python installed is 64 bit because tensorflow doesn't support 32 bit python
  
