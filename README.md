# Arthur: A Java Profanity-Checking Library (Coming Soon)

**Arthur** is a Java-based profanity-checking library inspired by the popular **profanity-check** Python library. Designed for real-time content moderation, **Arthur** efficiently detects offensive language in text inputs or messages within Java applications.

## Features

- **Real-time Profanity Detection**: Check if a text message contains profanity as it is received.
- **Customizable Word List**: Easily add or modify profane words and phrases.
- **Pattern Matching**: Supports detection of obfuscated words (e.g., "f@ck", "sh1t").
- **Machine Learning Model Support**: Optionally extend the library to use machine learning models for more advanced detection.

## Installation

### Using Maven

You can include **Arthur** in your Java project by adding it as a dependency in your `pom.xml`:

```xml
<dependency>
    <groupId>com.nextdevv</groupId>
    <artifactId>arthur</artifactId>
    <version>1.0.0</version>
</dependency>
```

### Using Gradle

Alternatively, if you're using Gradle:

```gradle
dependencies {
    implementation 'com.nextdevv:arthur:1.0.0'
}
```

## Usage

### Basic Example

```java
import com.nextdevv.arthur.ProfanityFilter;

public class Main {
    public static void main(String[] args) {
        String testMessage = "This is a message with f@cking bad words.";
        
        if (ProfanityFilter.containsProfanity(testMessage)) {
            System.out.println("Profanity detected!");
        } else {
            System.out.println("No profanity detected.");
        }
    }
}
```

### Customizing the Profanity List

Arthur uses a basic word list to detect profanity, but you can easily customize it by adding your own words:

```java
ProfanityFilter.addProfaneWord("exampleword");
```

### Regular Expression Support

Arthur supports regular expressions to detect obfuscated profane words, such as "f@ck" or "sh1t". Customize the regex patterns to fit your needs.

## Advanced Usage (Machine Learning)

If you want to integrate machine learning models for more accurate detection, you can train your own model using a machine learning framework like **Weka** or **TensorFlow Java**. Once trained, load your model and use it in **Arthur** for predictions.

## Contributing

If you'd like to contribute to **Arthur**, feel free to submit a pull request or open an issue. We'd love to see improvements, bug fixes, or new features!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
