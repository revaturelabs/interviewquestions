1. What is Log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- log4j is a reliable, fast and flexible logging framework (APIs) written in Java, which is distributed under the Apache Software License.
- Log4j has been ported to the C, C++, C#, Perl, Python, Ruby, and Eiffel languages.
- Log4j is highly configurable through external configuration files at runtime. It views the logging process in terms of levels of priorities and offers mechanisms to direct logging information to a great variety of destinations, such as a database, file, console, UNIX Syslog, etc.

</blockquote>
</details>

---

2. What are the components of Log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Log4j has three main components −
- loggers: Responsible for capturing logging information.
- appenders: Responsible for publishing logging information to various preferred destinations.
- layouts: Responsible for formatting logging information in different styles.

</blockquote>
</details>

---

3.What are the support objects in Log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Level Object
- Filter Object
- Object Renderer
- Log Manager

</blockquote>
</details>

---

4. What are the features of log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following are features of log4j −
- It is thread-safe.
- It is optimized for speed.
- It is based on a named logger hierarchy.
- It supports multiple output appenders per logger.
- It supports internationalization.
- It is not restricted to a predefined set of facilities.

</blockquote>
</details>

---

5. What are Pros and Cons of Logging?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- A well-written logging code offers quick debugging, easy maintenance, and structured storage of an application’s runtime information.
- Logging does have its drawbacks also. It can slow down an application. If too verbose, it can cause scrolling blindness. To alleviate these concerns, log4j is designed to be reliable, fast and extensible.
- Since logging is rarely the main focus of an application, the log4j API strives to be simple to understand and to use.

</blockcode>
</details>

---

6. Explain why to use Apache Log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- Being open-source its completely free to use.
- You can easily save log information into either files or even databases.
- Can be used for projects of any sizes small or large.

</blockquote>
</details>

---

7. What is the purpose of Logger object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The top-level layer of log4j architecture is the Logger which provides the Logger object. The Logger object is responsible for capturing logging information and they are stored in a namespace hierarchy.

</blockquote>
</details>

---

8. What is the purpose of Layout object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- The layout  of log4j architecture provides objects which are used to format logging information in different styles. It provides support to appender objects before publishing logging information.
- Layout objects play an important role in publishing logging information in a way that is human-readable and reusable.

</blockquote>
</details>

---

9. What is the purpose of Appender object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

This is a lower-level layer of log4j architecture which provides Appender objects. The Appender object is responsible for publishing logging information to various preferred destinations such as a database, file, console, UNIX Syslog, etc.

</blockquote>
</details>

---

10. What is the purpose of Level object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Level object defines the granularity and priority of any logging information. There are seven levels of logging defined within the API: OFF, DEBUG, INFO, ERROR, WARN, FATAL, and ALL.

</blockquote>
</details>

---

11. What is the purpose of Filter object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Filter object is used to analyze logging information and make further decisions on whether that information should be logged or not. An Appender objects can have several Filter objects associated with them. If logging information is passed to a particular Appender object, all the Filter objects associated with that Appender need to approve the logging information before it can be published to the attached destination.

</blockquote>
</details>

---

12.What is the purpose of ObjectRenderer object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The ObjectRenderer object is specialized in providing a String representation of different objects passed to the logging framework. This object is used by Layout objects to prepare the final logging information.

</blockquote>
</details>

---

13. What is the purpose of LogManager object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The LogManager object manages the logging framework. It is responsible for reading the initial configuration parameters from a system-wide configuration file or a configuration class.

</blockquote>
</details>

---

14.What is the use of log4j.properties?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The log4j.properties file is a log4j configuration file which keeps properties in key-value pairs. By default, the LogManager looks for a file named log4j.properties in the CLASSPATH.

</blockquote>
</details>

---

15. What is the purpose of layout object in Appender?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Appender uses the Layout objects and the conversion pattern associated with them to format the logging information.

</blockquote>
</details>

---

16. What is the purpose of target in Appender?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The target may be a console, a file, or another item depending on the appender.

</blockquote>
</details>

---

17. What is the purpose of level in Appender?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The level is required to control the filtration of the log messages.

</blockquote>
</details>

---

18. What is the purpose of threshold in Appender?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Appender can have a threshold level associated with it independent of the logger level. The Appender ignores any logging messages that have a level lower than the threshold level.

</blockquote>
</details>

---

19. What is the purpose of filter in Appender?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The Filter objects can analyze logging information beyond level matching and decide whether logging requests should be handled by a particular Appender or ignored.

</blockquote>
</details>

---

20. How will you define a root logger with appender file using log4j.properties?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following syntax defines the root logger with appender file:
```Java
//Define the root logger with appender file
log = /usr/home/log4j
log4j.rootLogger = DEBUG, FILE
```

</blockquote>
</details>

---

21. How will you define a file appender using log4j.properties?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following syntax defines a file appender −
```Java
//Define the file appender
log4j.appender.FILE=org.apache.log4j.FileAppender
log4j.appender.FILE.File=${log}/log.out
```
</blockquote>
</details>

---


22. How will you define the layout of file appender using log4j.properties?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following syntax defines the layout of file appender −
```Java
// Define the layout for file appender
log4j.appender.FILE.layout=org.apache.log4j.PatternLayout
log4j.appender.FILE.layout.conversionPattern=%m%n
```

</blockquote>
</details>

---

23. What are the different log levels in the logger component?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- All
- Debug
- Info
- Warn
- Error
- Fatal
- Off

</blockquote>
</details>

---

24. What is purpose of DEBUG log level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

DEBUG − Designates fine-grained informational events that are most useful to debug an application.

</blockquote>
</details>

---

25. What is purpose of ERROR log level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

ERROR − Designates error events that might still allow the application to continue running.

</blockquote>
</details>

---

26. What is purpose of FATAL log level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

FATAL − Designates very severe error events that will presumably lead the application to abort.

</blockquote>
</details>

---

27. What is purpose of INFO log level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

INFO − Designates informational messages that highlight the progress of the application at coarse-grained level.

</blockquote>
</details>

---

28. What is purpose of OFF log level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

OFF − The highest possible rank and is intended to turn off logging.

</blockquote>
</details>

---

29. What is purpose of TRACE log level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

TRACE − Designates finer-grained informational events than the DEBUG.

</blockquote>
</details>

---

30.What is purpose of WARN log level?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

WARN − Designates potentially harmful situations.

</blockquote>
</details>

---

31. How do Levels Works?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

A log request of level p in a logger with level q is enabled if p >= q. This rule is at the heart of log4j. It assumes that levels are ordered. For the standard levels, we have ALL < DEBUG < INFO < WARN < ERROR < FATAL < OFF.

</blockquote>
</details>

---

32.How will you define a root logger turning DEBUG mode off?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Following syntax defines the root logger with WARN mode turning DEBUG mode off.
```Java
//Define the root logger with appender file
log = /usr/home/log4j
log4j.rootLogger = WARN, FILE
```

</blockquote>
</details>

---

33. How will you create a logger in any class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Any other named Logger object instance is obtained through the second method by passing the name of the logger. The name of the logger can be any string you can pass, usually a class or a package name as we have used in the last chapter and it is mentioned below −

```Java
static Logger log = Logger.getLogger(log4jExample.class.getName());
```
</blockquote>
</details>

---

34. How will you print a log message in debug mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`public void debug(Object message)` of Logger class prints messages with the level `Level.DEBUG`.

</blockquote>
</details>

---

35. How will you print a log message in error mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`public void error(Object message)` of Logger class prints messages with the level `Level.ERROR`.

</blockquote>
</details>

---

36. How will you print a log message in fatal mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`public void fatal(Object message)` of Logger class prints messages with the level `Level.FATAL`.

</blockquote>
</details>

---

37. How will you print a log message in info mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`public void info(Object message)` of Logger class prints messages with the level `Level.INFO`.

</blockquote>
</details>

---

38. How will you print a log message in warn mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`public void warn(Object message)` of Logger class prints messages with the level `Level.WARN`.

</blockquote>
</details>

---

39. How will you print a log message in trace mode?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

`public void trace(Object message)` of Logger class prints messages with the level `Level.TRACE`.

</blockquote>
</details>

---

40. Mention what are the different types of Appenders?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Some of the Appenders type include
- ConsoleAppender logs to standard output
- FileAppender prints logs to some file
- Rolling file appender to a file with maximum size

</blockquote>
</details>

---

41. Mention what are the two static methods for obtaining a logger object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The two static methods for obtaining a logger object are

- `Public static Logger getRootLogger()`
- `Public static Logger getLogger(String name)`

</blockquote>
</details>

---

42. How log4j file is defined?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Log4j file is defined by the name `log4j.properties`, it keeps properties in key-value pairs. By default, the log manager looks for a file name `log4j.properties` in the CLASSPATH.

</blockquote>
</details>

---

43. Explain what is the command to write your logging information into a file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

To write your logging information into a file, you would need to use a command `org.apache.log4j.FileAppender`.

</blockquote>
</details>

---

44. Mention what are the logging methods provided by logger class?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Logger class provides a variety of methods to handle logging activities.  To obtain a logger object it provides two static methods:
`Public static logger getRootLogger();`
`Public static logger getLogger(String name);`

</blockquote>
</details>

---

45. In log4j how can you log into the database?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The log4j API provides the object `org.apache.log4j.jdbc`. JDBCAppender object can put logging information in a particular database.

</blockquote>
</details>

---

46. Can you customize the log output format?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Yes, you can extend the layout class to create your own customized log format. Appenders can be parameterized to use the layout of your choice.

</blockquote>
</details>

---

47. What are the system properties checked by log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The system properties checked by log4j are
- **Log4j debug**, if true, log4j will show internal debugging messages to the console.
- **defaultInitOverride**, if true, log4j will not execute default initialization.
- **configuration**, URL for default initialization configuration file.
- **configurationClass**, Class name for configurator to execute default initialization configuration file.
- **ignoreTCL**, if true, the thread class loader will be overlooked when loading classes.

</blockquote>
</details>

---

48.  Explain how can you get multiple processes to log to the same file?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We may have each process log to a socket Appender. The receiving socket server can receive all the events and send them to a single log file.

</blockquote>
</details>

---

49. Mention what is the difference between Threshold and LevelRangeFilter in log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Both Threshold and LevelRangeFilter does the same thing. However threshold should be faster. Filters enable you to implement your own logic, and you can also link them together if required. If you need a basic threshold functionality, then **threshold** function will be enough.

</blockquote>
</details>

---

50. Mention what does `.class` mean in log4j context?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

In log4j context, `.class` is used to get the full name of your class and that string is used to configure this logger object.  
For example,
```Java
logger.getlogget (Myclass.class)
```

</blockquote>
</details>

---

51. What is the purpose of PatternLayout object?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- If we want to generate your logging information in a particular format based on a pattern, then we can use `org.apache.log4j.PatternLayout` to format your logging information.

- The PatternLayout class extends the abstract `org.apache.log4j.Layout` class and overrides the `format()` method to structure the logging information according to a supplied pattern.

</blockquote>
</details>

---

52. What is package level logging in log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Package level logging is the standard logging of log4j, with this you would determine the package and the associated level.

</blockquote>
</details>

---

53. What does WARN and TRACE level indicates in log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

Log4j level WARN gives a warning about an unpredicted event to the user. The messages coming out of this level may not stop the progress of the system.  The TRACE level provides more detailed information than the DEBUG level, and it will stay on the top of the hierarchy.

</blockquote>
</details>

---

54. What are the format characters used in log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The format characters used in log4j are
- **L**- it is used to output the line number from where the logging request was processed or issued
- **m**- It is used to output the application supplied message related with the logging event
- **p**-It is used to output the priority of the logging event
- **C**- It is used to output the class name of the caller issuing the logging request
- When any number is used along with the character it means the priority of the logging event should be justified to a width of 4 characters.

</blockquote>
</details>

---

55. What is the best way to migrate from `java.util` logging to log4j?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

The best way to migrate from `java.util`  logged to log4j is to use global file search/replace method.  It will replace with `org.apache.log4j.Logger`.

</blockquote>
</details>

---

56. Why do you get multiple copies of the message in log file sometime?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

There could be two reasons why this may happen:
- Repeated configuration of log4j.
- Attaching the same appenders to multiple loggers.

</blockquote>
</details>

---

57. How can we change the Log level for the application ?

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

By changing the Root Level within Log4j config.

</blockquote>
</details>

---

58. In following log4j configuration file, How should we change the logging level to WARN

```Java
<Configuration status="DEBUG">
<Appenders>
<RollingFile name="File" fileName="logs/xyz.log" filePattern="logs/xyz-%d{MM-dd-yyyy}.log.gz">
      <TimeBasedTriggeringPolicy />
   </RollingFile>
</Appenders>
<Loggers>
<Root level="DEBUG">
<AppenderRef ref="File" />
</Root>
</Loggers>
</Configuration>
```

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

We should change the root level from DEBUG to WARN.

</blockquote>
</details>

---

59. Can you organize following Log4j levels in hierarchy ?
WARN, DEBUG,INFO, ERROR	Log4j

![Easy](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/simple%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

- DEBUG
- INFO
- WARN
- ERROR

    - Root Log level of DEBUG will print all
    - Root Log Level of INFO will print INFO, WARN and ERROR
    - Root Log level of WARN will print WARN and ERROR
    - Root Log level of ERROR will print ERROR alone

</blockquote>
</details>

---

60. What should be the logging level while logging exceptions ?	

![Medium](https://github.com/revaturelabs/interviewquestions/blob/dev/ComplexityTags/Medium%20(2).svg)

<details> <summary> <b> Show Answer </b> </summary>
<blockquote>

It depends on how severe the exception is. If the exception is completely unexpected and breaks the request, It should be logged as ERROR or FATAL. If it's not expected but we can live with it and the application request continue in-spite of it, It should be WARN. If it's expected , it can be just INFO.

</blockquote>
</details>

---