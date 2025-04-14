[![Maven Central](https://maven-badges.herokuapp.com/maven-central/net.jqwik/jqwik/badge.svg)](https://maven-badges.herokuapp.com/maven-central/net.jqwik/jqwik)
[![Javadocs](http://javadoc.io/badge/net.jqwik/jqwik-api.svg)](https://jqwik.net/docs/current/javadoc/index.html)
[![CI Status](https://github.com/jqwik-team/jqwik/workflows/CI/badge.svg?branch=main)](https://github.com/jqwik-team/jqwik/actions)

# jqwikOG

**jqwikOG** is a modified version of [jqwik](http://jqwik.net), an alternative [test engine for the JUnit 5 platform](https://junit.org/junit5/docs/current/user-guide/#launcher-api-engines-custom) that focuses on Property-Based Testing. This version integrates an object generator based on method sequence generation inspired by [Randoop](https://randoop.github.io/randoop/).

## Website & Documentation
See the [jqwik website](http://jqwik.net) for original documentation and usage examples.

## Quick Start
- **Java Version**: openjdk 11.0.22 (2024-01-16)
- **Build Project**:
  ```bash
  ./gradlew build -x engine:test -x kotlin:test
  ```

## Example Properties
Examples using the modified jqwikOG engine are located in:
```
engine/src/test/java/experiments/randoopTest
```

### Run a Single or Multiple Property-Based Tests
To run individual or specific test cases, use:
```bash
./gradlew :engine:test --tests experiments.randoopTest.RandoopTest.testName
```
You can also use wildcards to run multiple tests:
```bash
./gradlew :engine:test --tests "experiments.randoopTest.*"
```

## Docker Support
You can use Docker to build and run jqwikOG without installing dependencies directly.

### Build Docker Image
```bash
docker build -t myproject .
```

### Run Docker Container Interactively
```bash
docker run -it myproject
```

## Contributing
Feel free to fork the repository, open issues, or submit pull requests to contribute to the project.

## License
This project is based on jqwik and distributed under the same license unless otherwise specified.
