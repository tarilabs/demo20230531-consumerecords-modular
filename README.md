like demo20230530-consumerecords but modular

per https://docs.drools.org/8.39.0.Final/drools-docs/docs-website/drools/getting-started/index.html

- set maven.compiler.release=17
- replacing class with record for consumption/pattern match

```sh
javap -v demo20230531-consumerecords/target/classes/org/drools/demo/Measurement.class
javap -v demo20230531-consumerecords/target/classes/org/drools/demo/Rule
```

confirms even when using jdk18

```
demo20230531-consumerecords-modular $ mvn --version
Apache Maven 3.8.6 (84538c9988a25aec085021c365c560670ad80f63)
Maven home: /usr/local/Cellar/maven/3.8.6/libexec
Java version: 18.0.1.1, vendor: Homebrew, runtime: /usr/local/Cellar/openjdk/18.0.1.1/libexec/openjdk.jdk/Contents/Home
Default locale: en_IT, platform encoding: UTF-8
OS name: "mac os x", version: "13.4", arch: "x86_64", family: "mac"
demo20230531-consumerecords-modular $ javap -v demo20230531-consumerecords/target/classes/org/drools/demo/Rulesd5202542da0547c3bb4ebe209cbf2768.class 
Classfile /Users/mmortari/git/demo20230531-consumerecords-modular/demo20230531-consumerecords/target/classes/org/drools/demo/Rulesd5202542da0547c3bb4ebe209cbf2768.class
  Last modified May 31, 2023; size 2756 bytes
  SHA-256 checksum 8060482a331602479408c5578496d6ec4437dd01c8325e9febd29bf8f22c07bd
  Compiled from "Rulesd5202542da0547c3bb4ebe209cbf2768.java"
public class org.drools.demo.Rulesd5202542da0547c3bb4ebe209cbf2768 implements org.drools.model.Model
  minor version: 0
  major version: 61
```
