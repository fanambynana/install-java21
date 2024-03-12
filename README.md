## Install Java 21 and set JAVA_HOME
---
*For ubuntu and debian based*
---

#### Steps :

```
# -- Download the jdk --

# -- Extract --
# _ chage directory
tar xvf openjdk-21.0.2_linux-x64_bin.tar.gz
sudo mv jdk-21.0.2/ /usr/lib/jvm

# -- Edit profile --
sudo vim /etc/profile
# _ add these lines :  ---- "
#  export JAVA_HOME=/usr/lib/jvm/jdk-21.0.2
#  export PATH=$PATH:$HOME/bin:$JAVA_HOME/bin
# "
sudo . /etc/profile

# -- Update alternative --
sudo update-alternatives --install "/usr/bin/javac" "javac" /usr/lib/jvm/jdk-21.0.2/bin/javac 1
# _ and do the same, just replace all 'javac' with 'java' and 'javadoc'

# -- Configure --
sudo update-alternatives --config javac
# _ enter the number of the section with jdk-21
# _ and do the same, replace 'javac' with 'java' and 'javadoc'
```
