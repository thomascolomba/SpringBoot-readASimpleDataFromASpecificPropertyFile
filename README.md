How to read a properties from a non standard property file with Spring Boot.<br/>
<br/>
How to compile and execute :<br/>
mvn package<br/>
java -jar ./target/readASimpleDataFromASpecificPropertiesFile-0.0.1-SNAPSHOT.jar<br/>
<br/>
<br/>
---fileWithAFancyName.properties<br/>
myString=qwerty<br/>
---MyConfigurationBean.java<br/>
@PropertySource("classpath:fileWithAFancyName.properties")
...
private String myString;<br/>
+getter and setter<br/>
---The class who displays the value of the 'myString' configuration<br/>
@Autowired<br/>
MyConfigurationBean myConf;<br/>
...<br/>
System.out.println(myConf.getMyString());<br/>
<br/>
<br/>
The application will read the value 'qwerty' of the property myString in the non standard fileWithAFancyName.properties configuration file then display it in the terminal.<br/>


