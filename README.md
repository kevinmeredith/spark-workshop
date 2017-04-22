# spark-workshop


# Working on Windows

https://gist.github.com/kevinmeredith/25a9ade2982c89c6f925e5a02ed97fb7

```
$mkdir spark_sandbox
$cd spark_sandbox
$cat build.sbt 
scalaVersion := "2.11.8"

libraryDependencies += "org.apache.spark" % "spark-core_2.11" % "2.1.0"
$sbt console
scala> import org.apache.spark.SparkConf
scala> import org.apache.spark.SparkContext
scala> val config = new SparkConf().setAppName("cust data").setMaster("local[*]")
config: org.apache.spark.SparkConf = org.apache.spark.SparkConf@13b23911
scala>val sc = new SparkContext(sc)
```
