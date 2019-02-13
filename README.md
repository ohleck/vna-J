# vna-J
the JAVA way to the miniVNA


Actual Working Setup
----------------------------------------

java --version

openjdk version "11.0.2" 2019-01-15
OpenJDK Runtime Environment (build 11.0.2+9-Debian-3)
OpenJDK 64-Bit Server VM (build 11.0.2+9-Debian-3, mixed mode, sharing)

USB communication / UDEV

sudo usermod -a -G dialout USERNAME

java -jar vnaJ.3.2.10.jar

----------------------------------------
VNA-J  Library


@echo off

set JAVA="C:\Program Files\Java\jdk-10.0.2\bin\java"
set CP=./
set CP=%CP%;./vnaJ.Library.3.2.10.jar
set CP=%CP%;./AppleJavaExtensions.jar
set CP=%CP%;./commons-lang3-3.1.jar
set CP=%CP%;./commons-math-2.2.jar
set CP=%CP%;./jcommon-1.0.17.jar
set CP=%CP%;./jdom-1.1.2.jar
set CP=%CP%;./jna-4.3.0.jar
set CP=%CP%;./poi-3.7-20101029.jar
set CP=%CP%;./purejavacomm-1.0.0.jar

echo Runtime  =%JAVA%
echo Classpath=%CP%

@echo on

%JAVA% -classpath "%CP%" LibrarySampleRunner "miniVNA-pro2" "COM11"

---------------------------------------
