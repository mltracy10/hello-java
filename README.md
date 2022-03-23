# LaunchDarkly Sample Java Application 

I leveraged the LaunchDarkly Sample App for my technical assignment using Java by forking the github repo -Merritt

## Build instructions 

I used Atom, Github Desktop, and Gradle to edit/push/build.

1. Edit `src/main/java/Hello.java` and replace the value of `SDK_KEY` to your LaunchDarkly SDK key. The SDK of my test environment of my LaunchDarkly instance was what was used in my code. I set the FEATURE_FLAG_KEY to "my-boolean-flag"

```java
  static final String SDK_KEY = "REPLACE-ME";

  static final String FEATURE_FLAG_KEY = "my-boolean-flag";
```

2. Create a boolean feature flag in LD and name it "my-boolean-flag". Enable the flag and save.

3. On the command line, run `./gradlew run` (or, on Windows, `gradlew run`).

You should see the message `"Feature flag '<flag key>' is <true/false> for this user"`. It will also create a user called Sandy.

4. Change the LDUser key on line 36 to "example-user-key2" and the user name from Sandy to HarryPotter.

5. On the command line, run `./gradlew run` (or, on Windows, `gradlew run`).

You should see the message `"Feature flag '<flag key>' is <true/false> for this user"`. It will also create a user called HarryPotter.

4. There should now be 2 users in the User section of the LD GUI. Creating 2 users allowed me to do targeting based on User.

5. Edit the boolean feature flag (my-boolean-flag) so that if User=HarryPotter it shows True, and if User=Susan, shows false. You could also do the kill switch and turn off the feature flag all together.
