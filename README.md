
## Description 

  * https://issues.apache.org/jira/browse/MNG-7944 Execution default of goal org.apache.maven.plugins:maven-assembly-plugin:3.6.0:single failed: Index 2 out of bounds for length 2

### Maven 4.0.0-alpha-7
 * https://archive.apache.org/dist/maven/maven-4/4.0.0-alpha-7/binaries/
 
```
❯ /opt/maven/apache-maven-4.0.0-alpha-7/bin/mvn -q clean package
```

### Maven 4.0.0-alpha-8

 * https://archive.apache.org/dist/maven/maven-4/4.0.0-alpha-8/binaries/

```
❯ /opt/maven/apache-maven-4.0.0-alpha-8/bin/mvn -q clean package
[ERROR] Failed to execute goal org.apache.maven.plugins:maven-assembly-plugin:3.6.0:single (default) on project MNG-7944-reproducer: Execution default of goal org.apache.maven.plugins:maven-assembly-plugin:3.6.0:single failed: Index 2 out of bounds for length 2 -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the '-e' switch
[ERROR] Re-run Maven using the '-X' switch to enable verbose output
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/PluginExecutionException
```

With debug:
```
❯ /opt/maven/apache-maven-4.0.0-alpha-8/bin/mvn -X package > maven-4.0.0-alpha-8.log
```
