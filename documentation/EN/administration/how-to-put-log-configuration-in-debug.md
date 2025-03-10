##  How to put log configuration in debug

### 1) Introduction

Sometimes, you might need to change the default log level of the log configuration in order to have more information of LinShare behavior.
This can be achieved at different places, which leads to different behavior.
Here's a brief documentation on how to change this log level.

In this document, we will have to modify the Log4j configuration file.
With the default Debian installation process, this file is located in:
`/etc/linshare/log4j2.properties`

### 2) Changing the log level

#### 2.1) Log levels

There are different kinds of log levels, each bringing more and more logs.
This list is of the standard log levels supported by Log4j2:
* OFF
* FATAL
* ERROR
* WARN
* INFO
* DEBUG
* TRACE
* ALL

The log levels can be changed in the configuration files or dynamically.
Changing the log level in the configuration file is persistent, but need LinShare to be restarted,
in the opposite, the dynamic change is not persistent but effective immediately.

#### 2.2) Root log level in debug

Changing the root level will impact all loggers, from LinShare to all dependencies.
In order to change this log level, edit the `log4j2.properties` configuration file, and change this line:
```
rootLogger=DEBUG, ${LOG4J2_APPENDER}
```
WARNING, this configuration will produce a lot of logs, take care of the free space available on your
machine and it may slow down the app too.

You can also change globally the appender (output) of logs by updating the line above:

```
property.LOG4J2_APPENDER=${env:LOG4J2_APPENDER:-CONSOLE}
```

The available appenders are:
- `CONSOLE`: append to the default system log. it is the default value.
- `CONSOLE_JSON`:  append to the default system log, but in JSON format
- `LINSHARE`: append to a specific file, by default `/var/log/tomcat9/linshare.log`


#### 2.3) Logger log level in debug

You can specify the log level at the logger configuration itself:
```
logger.linshare = DEBUG, ${LOG4J2_APPENDER}
logger.linshare.name = org.linagora.linshare
```
This gives you a way of having more information for a single component, and is
adapted for having information such as connection to the database for example.
This sample is for LinShare code, not its dependencies. it is the most suitable
choice.


#### 2.4) Logger log level with REST API

There's an admin REST API available in LinShare in order to configure log level at runtime:
```
GET BASE_URL/loggers/org.linagora.linshare/DEBUG
```

In the previous example:
* `BASE_URL` is the base URL of your LinShare backend
* `org.linagora.linshare` is the logger name
* `DEBUG` is the log level to be set to this logger
