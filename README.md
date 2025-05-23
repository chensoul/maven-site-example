# maven-site-example

## Instructions

### Build

### Build

```bash
mvn clean package
```

### Test

```bash
mvn clean verify
```

### Site

Upload sites to gitHub pages:

```bash
mvn clean site site:stage scm-publish:publish-scm 
```

### Release

Update Release version:

```bash
mvn versions:set -DprocessAllModules=true -DgenerateBackupPoms=false -DnewVersion=0.0.1
```

Publish to Central:

```bash
mvn -DskipTests -Prelease deploy
```

### Sonar

```bash
mvn verify -Pcoverage javadoc:javadoc
mvn sonar:sonar -Dsonar.token=$SONAR_TOKEN
```

## References

- https://github.com/s4u/parent
