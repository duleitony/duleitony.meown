---
layout:     post
title:      "JVM - Class Loader Subsystem"
subtitle:   "Java-JVM-loader"
date:       2017-11-15 11:00:00
author:     "Tony"
catalog: true
tag: [Java]
header-img: "img/blog-bg.jpg"
---

> Java JVM Class Loader Subsystem  

## Loading 
Classes will be loaded by this component. Boot Strap class Loader, Extension class Loader, and Application class Loader are the three class loader which will help in achieving it.

Boot Strap ClassLoader – Responsible for loading classes from the bootstrap classpath, nothing but rt.jar. Highest priority will be given to this loader.
Extension ClassLoader – Responsible for loading classes which are inside ext folder (jre\lib).
Application ClassLoader –Responsible for loading Application Level Classpath, path mentioned Environment Variable etc.
The above Class Loaders will follow Delegation Hierarchy Algorithm while loading the class files.

##  Linking
Verify – Bytecode verifier will verify whether the generated bytecode is proper or not if verification fails we will get the verification error.
Prepare – For all static variables memory will be allocated and assigned with default values.
Resolve – All symbolic memory references are replaced with the original references from Method Area.

##  Initialization
This is the final phase of Class Loading, here all static variables will be assigned with the original values, and the static block will be executed. 