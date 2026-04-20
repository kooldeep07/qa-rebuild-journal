Java

JDK- consists of classes, methods, tools, compiler, debuggers, runtime env(JRE)
JRE- only for running the code

<img width="998" height="816" alt="image" src="https://github.com/user-attachments/assets/15f58c2e-8b14-490c-bdfc-183baf75a565" />


Run in Terminal to check isntalled Java: java -version

Oracle:
1. paid JDK: commercial
2. OpenJDK: open source

Set up the System variable in Windows- these tells the external programs like Docker, Jenksins(based on Java) to indicate where Java is installed.
1. JAVA_HOME
2. Path

What if you only have JRE installed but not JDK?


Test.java(Source Code) --> compilation(javac) --> bytecode/intermediate(.class file) --> JVM converts it to binary code
JVM is OS/platform dependent, diff JVM for different OSes, hence different JDK installers downloads for different OSes.

<img width="843" height="554" alt="Screenshot 2026-01-16 at 10 32 08 AM" src="https://github.com/user-attachments/assets/cd2d4ae2-e662-4d38-a882-651ec51ee4a0" />

.class files can run on any client machine. They can be found in bin folder. 
Compile time is the phase where the source code is translated into bytecode, while runtime is the phase where the bytecode is executed by the Java Virtual Machine (JVM).
Python, Java script are runtime languages as it does not have a compiler.
Advantage of compilation: 80% checks are done at compile-time (before we run the program).

<img width="608" height="467" alt="Screenshot 2026-01-16 at 10 58 16 AM" src="https://github.com/user-attachments/assets/e9ef50c0-2ca8-4874-b0a0-3f69c1476625" />

<img width="2028" height="222" alt="image" src="https://github.com/user-attachments/assets/b0b26991-e896-4a37-afa3-5b14c9bbab35" />
<img width="1013" height="114" alt="Screenshot 2026-01-16 at 11 00 59 AM" src="https://github.com/user-attachments/assets/2224c84e-9959-4599-80fe-4db08bc9c893" />

.jar file- a bundle of .class files, so that's WORA too.

How to convert .class files back to .java?

Data Types- Primitives

Eclipse- Java Project

Every variable is stored on RAM.

true, false = literals

memory occupied by Non-primitive types can be destryed(garbage).
















