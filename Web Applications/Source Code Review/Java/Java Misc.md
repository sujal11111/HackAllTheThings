# Java Misc
### Compilete Java File on the fly
```bash
# Compile Java File
javac -source 1.8 -target 1.8 test.java
javac exploit.java

# Convert test.class to test.jar 
mkdir META-INF
echo "Main-Class: test" > META-INF/MANIFEST.MF

# Create Jar file
jar cmvf META-INF/MANIFEST.MF test.jar test.class

# Run file for sanity check
java -jar test.jar

# Run Java file on the fly
javac Exploit.java
java Exploit
```

### Run Java interpreter on the fly
```bash
jshell --class-path /home/akenofu/libs/apache-commons-lang.jar
```