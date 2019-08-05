## install git without xcode



1. git download and install (http://git-scm.com/download/mac.)
2. Run terminal
3. Add its directory to your path 

```java
echo "PATH=/usr/local/git/bin:\$PATH" >> ~/.bash_profile
source ~/.bash_profile
```

4. Install command line tools

```java
xcode-select --install
```

