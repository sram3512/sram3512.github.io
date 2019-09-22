---
layout: post
title:  "Getting Started with Apache Spark"
date:   2019-09-21 12:00:00 +0530
categories: jekyll update
---

# Introduction
Apache Spark is an In-memory Cluster Computing Framework. It's used to perform traditional Map-Reduce jobs as well as other complex operations.
The latest version of Spark can be downloaded from [here](https://spark.apache.org/downloads.html). A specific version of Spark can be downloaded from the [archived section](https://archive.apache.org/dist/spark/). Ensure you downloaded the appropriate tar file, many of them don't contain the required resources.

## Build from Source
Extract the contents of the tar file to the destination location where you want Spark to reside. The untared file contains the binarys and configuration files. The binaries included are **spark-submit**, **spark-shell**, **start-servers** and **pyspark**.

```bash
tar -xzvf spark-2.3.3-bin-hadoop2.6.tgz
mv spark-2.3.3-bin-hadoop2.6 /usr/local/spark
export PATH=$PATH:/usr/local/spark/bin:/usr/local/spark/sbin
# Can be set in your ~/.bashrc or ~/.zshrc
```
## MacOS
```bash
brew install apache-spark
```
This will install the latest version of Spark.
## Confirm Installation
Execute the following commands and verify the following output.
```bash
spark-shell                                                 
2019-09-21 22:07:01 WARN  NativeCodeLoader:62 - Unable to load native-hadoop library for your platform... using builtin-java classes where applicable
Setting default log level to "WARN".
To adjust logging level use sc.setLogLevel(newLevel). For SparkR, use setLogLevel(newLevel).
Spark context Web UI available at http://10.24.44.203:4040
Spark context available as 'sc' (master = local[*], app id = local-1569128825914).
Spark session available as 'spark'.
Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 2.3.3
      /_/
         
Using Scala version 2.11.8 (OpenJDK 64-Bit Server VM, Java 1.8.0_222)
Type in expressions to have them evaluated.
Type :help for more information.

scala>
```
## Trouble Shooting
Incase spark-shell fails to run and several error messages pop up,add the following environment variables.
SPARK_HOME = "location where Spark has been extracted to eg- /usr/local/spark"
PYSPARK_PYTHON= "Location of the python binary used by spark"
JAVA_HOME="Location of java binary"

If the execution of **spark-submit <file_name>.py**, returns a FileNotFound error for file:/<path_to_python_file>.py. Ensure that the path doesn't contain white spaces. Scala doesn't handle whitespaces in directory names well.
