# Datasource-Receiver

Datasource-Receiver is a library that allows the user to read data with [Apache Spark](https://spark.apache.org/)
from [Datasource](https://www.rabbitmq.com/).

## Requirements

This library requires Spark 1.5+, Scala 2.10+

## Using the library

There are two ways of using Datasource-Receiver library:

The first one is to add the next dependency in your pom.xml:

```
<dependency>
  <groupId>com.stratio.receiver</groupId>
  <artifactId>datasource</artifactId>
  <version>LATEST</version>
</dependency>
```

The other one is to clone the full repository and build the project:

```
git clone https://github.com/Stratio/Datasource-Receiver.git
mvn clean install
```

### Build

There are two modules to package with different versions of Spark

- To package it with Spark-1.4:

`mvn clean package -pl com.stratio.receiver:spark-rabbitmq_1.4`

- To package it with Spark-1.5 (default):

`mvn clean package -pl com.stratio.receiver:spark-rabbitmq_1.5`

### Scala API

```
val receiverStream = DatasourceUtils.createStream(sparkStreamingContext, params)
```

### Java API

```
JavaReceiverInputDStream receiverStream = DatasourceUtils.createJavaStream(javaSparkStreamingContext, params);


```

# License #

Licensed to STRATIO (C) under one or more contributor license agreements.
See the NOTICE file distributed with this work for additional information
regarding copyright ownership.  The STRATIO (C) licenses this file
to you under the Apache License, Version 2.0 (the
"License"); you may not use this file except in compliance
with the License.  You may obtain a copy of the License at

  http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing,
software distributed under the License is distributed on an
"AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
KIND, either express or implied.  See the License for the
specific language governing permissions and limitations
under the License.
