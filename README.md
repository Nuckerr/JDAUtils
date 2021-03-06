# JDAUtils
A Utils libary for JDA

Example:

```java
public static void main(String[] args) throws LoginException {
        JDA bot = JDABuilder.createDefault("TokenGoesHere").build();
        CommandManager manager = new CommandManager(bot, "-");
        manager.registerCommand("example", new ExampleCommand());
    }
```
And `ExampleCommand()`
```java
public class ExampleCommand extends Command {

    @Override
    public void onCommand(Message message, Guild guild, TextChannel channel, String[] args) {
        channel.sendMessage("Example command").queue();
    }
}
```

##  Import using gradle:
```gradle
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

```gradle
	dependencies {
	        implementation 'com.github.Nuckerr:JDAUtils:[VERSION // CHECK LATEST RELEASE TAG]'
	}
```


## Import using maven:
```maven
	<repositories>
		<repository>
		    <id>jitpack.io</id>
		    <url>https://jitpack.io</url>
		</repository>
	</repositories>
```
```maven
	<dependency>
	    <groupId>com.github.Nuckerr</groupId>
	    <artifactId>JDAUtils</artifactId>
	    <version>[VERSION // CHECK LATEST RELEASE TAG]</version>
	</dependency>
```
