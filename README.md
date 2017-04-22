# spark-workshop


# Working on Windows

https://gist.github.com/kevinmeredith/25a9ade2982c89c6f925e5a02ed97fb7

```
$mkdir spark_sandbox
$cd spark_sandbox
$cat build.sbt 
scalaVersion := "2.11.8"

libraryDependencies += "org.apache.spark" %% "spark-core" % "2.1.0"
libraryDependencies += "org.apache.spark" %% "spark-sql" % "2.1.0"
$sbt console

# Run the following from the Scala Console

import org.apache.spark.SparkConf
import org.apache.spark.SparkContext
val config = new SparkConf().setAppName("cust data").setMaster("local[*]")
val sc = new SparkContext(config)
val sqlContext = new org.apache.spark.sql.SQLContext(sc)
import sqlContext.implicits._
```
