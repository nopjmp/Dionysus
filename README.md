# Dionysus

Fork of 1.12.2 [Paper](https://github.com/PaperMC/Paper) aimed at improving server performance for anarchy servers.

## Contact

TBD

## How To (Server Admins)

Dionysus uses the same paperclip jar system that Paper uses.

You can download the latest build of Dionysus by going [here](https://github.com/nopjmp/Dionysus/releases/latest).

You can also [build it yourself](https://github.com/nopjmp/Dionysus#building)

## How To (Plugin developers)

In order to use Dionysus as a dependency you must [build it yourself](https://github.com/nopjmp/Dionysus#building).
Each time you want to update your dependency you must re-build dionysus.

Dionysus-API maven dependency:

```xml

<dependency>
    <groupId>dev.pomf.dionysusdev.pomf.dionysus</groupId>
    <artifactId>dionysus-api</artifactId>
    <version>1.12.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

Dionysus-Server maven dependency:

```xml

<dependency>
    <groupId>dev.pomf.dionysusdev.pomf.dionysus</groupId>
    <artifactId>dionysus</artifactId>
    <version>1.12.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

There is no repository required since the artifacts should be locally installed
via building dionysus.

## Building

Requirements:

- You need `git` installed, with a configured user name and email.
  On windows you need to run from git bash.
- You need `maven` installed
- You need `jdk` 8+ installed to compile (and `jre` 8+ to run)
- Anything else that `paper` requires to build

If all you want is a paperclip server jar, just run `./dionysus jar`

Otherwise, to setup the `Dionysus-API` and `Dionysus-Server` repo, just run the following command
in your project root `./dionysus patch` additionally, after you run `./dionysus patch` you can run `./dionysus build` to build the
respective api and server jars.

`./dionysus patch` should initialize the repo such that you can now start modifying and creating
patches. The folder `Dionysus-API` is the api repo and the `Dionysus-Server` folder
is the server repo and will contain the source files you will modify.

#### Creating a patch

Patches are effectively just commits in either `Dionysus-API` or `Dionysus-Server`.
To create one, just add a commit to either repo and run `./dionysus rb`, and a
patch will be placed in the patches folder. Modifying commits will also modify its
corresponding patch file.

## License

The PATCHES-LICENSE file describes the license for api & server patches,
found in `./patches` and its subdirectories except when noted otherwise.

Everything else is licensed under the MIT license, except when note otherwise.
See https://github.com/starlis/empirecraft and https://github.com/electronicboy/byof
for the license of material used/modified by this project.

### Note

The fork is based off of aikar's EMC framework found [here](https://github.com/starlis/empirecraft)
