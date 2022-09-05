# Dionysus

[![Discord](https://img.shields.io/discord/819436478865997874?label=discord)](https://discord.gg/dV7rp5F4uA)
[![GitHub all releases](https://img.shields.io/github/downloads/nopjmp/Dionysus/total)](https://github.com/nopjmp/Dionysus/releases)
[![GitHub contributors](https://img.shields.io/github/contributors/nopjmp/dionysus)](https://github.com/nopjmp/Dionysus/graphs/contributors) 
[![GitHub issues](https://img.shields.io/github/issues/nopjmp/Dionysus)](https://github.com/nopjmp/Dionysus/issues)

###### Maintained by contributors. Owner Discord: nopjmp#1337 

----

#### 1.12.2 [Paper](https://github.com/PaperMC/Paper) fork aimed at improving server performance for anarchy servers. [Latest Dev Build*](https://nightly.link/nopjmp/Dionysus/workflows/dev/dev/Dionysus-JDK17.zip)
###### Note: This fork is based off [Aikar's EMC Framework](https://github.com/starlis/empirecraft)

----

## Contributing

*Anyone can contribute. Just follow the below steps!* 

1. [Fork Dionysus](https://github.com/nopjmp/Dionysus/fork)
2. [Build Dionysus](https://github.com/nopjmp/Dionysus#building)
3. [Create Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request-from-a-fork)

Assistant will be given to get pull requests working correctly.

## Server Admins

Dionysus uses the same paperclip jar system that Paper uses.  
You can download the latest release of Dionysus [here](https://github.com/nopjmp/Dionysus/releases/latest).   
You can also [build it yourself](https://github.com/nopjmp/Dionysus#building)

## Plugin Developers
###### *With each Dionysus update you must update your dependency.*

In order to use Dionysus as a dependency you must [build it yourself](https://github.com/nopjmp/Dionysus#building)      
This will add it to your local maven repository folder. Then add the following to your `pom.xml`:

#### Dionysus-API Maven Dependency:
```xml
<dependency>
    <groupId>dev.pomf.dionysus</groupId>
    <artifactId>dionysus-api</artifactId>
    <version>1.12.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```
#### Dionysus-Server Maven Dependency:
```xml
<dependency>
    <groupId>dev.pomf.dionysus</groupId>
    <artifactId>dionysus</artifactId>
    <version>1.12.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

#### Local Maven Repository:

Windows: `C:\Users\<UserName>\.m2`
Linux: `/home/<UserName>/.m2`
Mac: `/Users/<UserName>/.m2`

```xml
<repository>
    <id>project.local</id>
    <name>project</name>
    <url>file:/Users/User/.m2/repository/</url>
</repository>
```

## Building

**Requirements:**

- You need `git` installed, with a configured user name and email.
  On windows you need to run from git bash.
- You need `maven` installed
- You need `jdk 1.8` to decompile and `jdk` 17+ installed to compile (and `jre` 17+ to run)
- Anything else that `paper` requires to build

**If all you want is a paperclip server jar run `./dionysus jar`**

#### Setting up `Dionysus-API` and `Dionysus-Server`

1. Run `./dionysus patch` in your project root.
2. Run `./dionysus build` to build the respective api and server jars.

#### Creating a patch

Patches are effectively just commits in either `Dionysus-API` or `Dionysus-Server`.

1. Create commit in `Dionysus-API` or `Dionysus-Server`.
2. Run `./dionysus rb` in your project root.`
3. Commit patch to `Dionysus` repo.

*Modifying commits will also modify its corresponding patch file.*

### License

The PATCHES-LICENSE file describes the license for api & server patches,
found in `./patches` and its subdirectories except when noted otherwise.

Everything else is licensed under the MIT license, except when note otherwise.
See [empirecraft](https://github.com/starlis/empirecraft) and [byof](https://github.com/electronicboy/byof)
for the license of material used/modified by this project.
