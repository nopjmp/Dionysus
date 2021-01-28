# Cauldron

Fork of 1.12.2 [Paper](https://github.com/PaperMC/Paper) aimed at improving server performance for anarchy servers.

## Contact

TBD

## How To (Server Admins)

Cauldron uses the same paperclip jar system that Paper uses.

You can download the latest build of Cauldron by going here: TBD

You can also [build it yourself](https://github.com/nopjmp/Cauldron#building)

## How To (Plugin developers)

In order to use Cauldron as a dependency you must [build it yourself](https://github.com/nopjmp/Cauldron#building).
Each time you want to update your dependency you must re-build cauldron.

Cauldron-API maven dependency:

```xml
<dependency>
    <groupId>dev.pomf.cauldron</groupId>
    <artifactId>cauldron-api</artifactId>
    <version>1.12.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
 </dependency>
```

Cauldron-Server maven dependency:

```xml
<dependency>
    <groupId>dev.pomf.cauldron</groupId>
    <artifactId>cauldron</artifactId>
    <version>1.12.2-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
```

There is no repository required since the artifacts should be locally installed
via building cauldron.

## Building

Requirements:

- You need `git` installed, with a configured user name and email.
  On windows you need to run from git bash.
- You need `maven` installed
- You need `jdk` 8+ installed to compile (and `jre` 8+ to run)
- Anything else that `paper` requires to build

If all you want is a paperclip server jar, just run `./cauldron jar`

Otherwise, to setup the `Cauldron-API` and `Cauldron-Server` repo, just run the following command
in your project root `./cauldron patch` additionally, after you run `./cauldron patch` you can run `./cauldron build` to build the
respective api and server jars.

`./cauldron patch` should initialize the repo such that you can now start modifying and creating
patches. The folder `Cauldron-API` is the api repo and the `Cauldron-Server` folder
is the server repo and will contain the source files you will modify.

#### Creating a patch

Patches are effectively just commits in either `Cauldron-API` or `Cauldron-Server`.
To create one, just add a commit to either repo and run `./cauldron rb`, and a
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
