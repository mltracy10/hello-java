# LaunchDarkly Sample Java Application 

I leveraged the LaunchDarkly Sample App for my technical assignment using Java -Merritt

## Build instructions 

I used Atom, Github Desktop, and Gradle to edit/push/build.

1. Edit `src/main/java/Hello.java` and replace the value of `SDK_KEY` to your LaunchDarkly SDK key. The SDK of my test environment of my LaunchDarkly instance was what is in the code. Set the FEATURE_FLAG_KEY to "my-boolean-flag"

```java
  static final String SDK_KEY = "1234567890abcdef";

  static final String FEATURE_FLAG_KEY = "my-boolean-flag";
```

2. On the command line, run `./gradlew run` (or, on Windows, `gradlew run`).

You should see the message `"Feature flag '<flag key>' is <true/false> for this user"`.

3. I edited the code to not only have Sandy added as a user, but also HarryPotter. This allowed me to do targeting based on User. I had to run the code a couple of times, once with Sandy and once with HarryPotter, to create both accounts.

4. My feature flag is a boolean flag (my-boolean-flag) that, when on, states If Susan, show false; If HarryPotter, show true. You could also do the kill switch and turn off the feature flag.
