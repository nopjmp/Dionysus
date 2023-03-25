<!-- SPDX-License-Identifier: MIT -->
# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

## [0.1.16] - 2023-03-25

* remove two patches around hoppers
* fix missing code in lag compensated eating patch
* Backport ArrowDMG fix
* Add possible fix for TP exploit
* override paper 1.12.2's download mechanism
* Remove unused variable now....
* Switch from ConcurrentQueue to synchronized list for plugin compat
* Trim map after clear test...
* Fix Patch
* PlayerItemHeldEvent Add Slot
* Clean up Dionysus Config
* remove unnecessary lines
* rename patch
* Clean up linear region file patch
* start on linear files
* Update README.md
* Prevent IndexOutOfBound in window packet
* Add few helpful patches
* Prevent recursive chunk loading for join chunks
* Improve do not load chunks for light checks patch
* Few improvements
* Update java information
* Set chunk coord int pair patch author to original author
* Merge branch 'dev' of https://github.com/nopjmp/Dionysus into dev
* Improve fire spread patch
* Drop revert xray (#49)
* Add Alternate Current redstone implementation (#48)
* Further improve light queue and improve other methods as well
* Temporarily drop map chunk load patch
* Prevent vehicle move while awaiting teleport confirm
* Tuinity Optimise ActivationRange#activateChunkEntities
* Fixup stats system with new long change
* Fix backwards compat with long change
* Migrate stats to long and improve stats map performance
* Migrate stats to long and improve stats map performance
* Use fastutil for entity tracker
* Add faster NBT compare options and improve guessSize patch
* Use FastThreadLocalThread for netty IO threads (#43)
* Prepare guessSize patch for future code for patches
* Add crash comment to config
* Fix a bug in disabling mojang server communication (#42)
* Add very dirty async world tick patch
* Fixup previous patch
* Backport Purpur's Alternative Keepalive Handling (#41)
* Add option to disable communication with mojang servers in offline mode (#40)
* Tiny cleanup of donkey patch
* Add option to disable duplicate log
* Fix banner color changing
* [ci skip] add nightly link
* Improve position iterator performance
* Port some other patches and improve performance (#39)
* Improve NeonPaper chest patch
* Improve fire spread checks
* Add slime setSize patch
* Improve guesssize method
* Optimize passenger list with fastutil
* Guava to caffeine
* Add dependency on caffeine
* Add a few extra patches
* Remove not needed tab change for update dependencies
* Fix-MC-161754
* Remove CHM patch
* Sort patches differently and delete comments from one patch
* Backport newer config system
* Add client sign limit
* Add jitpack way earlier
* Fix zstd dependency
* Add annotations to dependency commit
* Delete 0125-Dont-Tick-Dead-Players.patch
* Port even more patches
* Port few extra patches from FlamePaper, TacoSpigot and Reaper
* Port first few patches from NeonPaper
* Drop flare patch in API as well
* Drop flare profiler
* Paper Backport: Lag compensate eating
* Update sentry and allow concurrent book meta access
* Add a bit better handling for ZSTD config
* Fixup bukkit API in cases where data would still be written to the internal object
* Update Sentry and add pufferfish credits (#31)
* Port patches from Airplane and Pufferfish (#25)

## [0.1.15] - 2022-06-18

### Changes
* Improve merge checks
* Fix book meta speed for enchantments
* Fix build
* Add option to disable chunk loading past the world border
* Disable JNDI lookups in the default log config
* Improve performance of book meta pages

By only converting the pages when we need them, we save a lot of computing power for 99% of cases where pages are not needed and people just access the methods of ItemMeta.

* Improve performance of patch in more cases
* Fix small typos
* Fix error

## [0.1.14] - 2022-02-12

### Fixed
* Performance problem with the NBT size check

## [0.1.13] - 2022-02-05

### Added
* Add optimize armour stands from RemainingToast

## [0.1.12] - 2022-01-28

### Fixed
* CVE-2021-44832 - Apache Log4j2 updated to 2.17.1 (only affects JDBC Appender users)
* AntiBook Crash prevention caused issue with cloning books

## [0.1.11] - 2021-12-20

### Fixed
* CVE-2021-45105 - Apache Log4j2 updated to 2.17.0

### Removed
* Trove4J - outdated library that is slower than fastutils

## [0.1.10] - 2021-12-15

### Fixed

* Typos
* Don't count some map decorations
* TileEntity config didn't completely work

## [0.1.9] - 2021-12-14

### Fixed

* CVE-2021-45046 - Apache Log4j2 updated to 2.16.0

## [0.1.8] - 2021-12-12

### Fixed

* Log4j exploit by updating to 2.15.0
* O(N^2) Advancement Daya Player Interaction to be O(N)

### Added 
* configurable chunk dupe

## [0.1.7] - 2021-03-13

Hotfix for Structure generation

### Fixed

* Removed Xorshift on World.random
  * This is tied to structure generation for some reason in 1.12.2.
  * Will add a shared global random and do testing on moving entity and block behavior to a faster random source.

## [0.1.6] - 2021-03-12

### Added

* Add the ability to redact player ip addresses and coords
  * Banning a player by ip will still work, just not display in the logs.
  * Further customization should come later

### Fixed

* Fixed players getting kicked due to improper change for World.random
  * This was only in the dev builds but still was given out to some users

### Removed

* Networking System based on Velocity and Yatopia
  * This unfortunately touched a few areas that a version agnostic packet manipulation framework was using.
* Shapeless crafting from Airplane backport
  * This was only in dev builds and was a bad, broken port

## [0.1.5] - 2021-03-07

### Added

* Fair natural spawning
  * Searches around the players to avoid their locations for spawning in monsters if they are hitting the limit.
* Load Chunks for login asyncronously
* Removed EnumSet allocations in crafting checks
* Lighting system optimizations
  * currently around lambda allocations being removed, need to work on the algorithm and making it more async
* Added a dionysus commands reload and version

### Changed

* Change logging levels in PlayerConnection on spammy messages

## [0.1.4] - 2021-02-13

### Added

* Velocity Native compression/crypto from Tuinity!
* NBT Compression Levels (Chunks use NBT)
* New Networking System based on Yatopia and Velocity

### Changed

* Paperclip was updated to the latest version

## [0.1.3] - 2021-02-10

### Fixed

* Dispenser Shulker Box Crash

## [0.1.2] - 2021-02-10

### Removed

* AntiPhysics crash
  * this was half baked and not fully tested, needs more work.

## [0.1.0] - 2021-02-09

### New Features 

* TileEntity Limit Optimization
* AntiBook crash implementation
* AntiPhysics crash implementation
* CompactSineLUT
  * taken from Lithium by CaffeineMC/Jellysquid
* Switched out Math.sin and Math.cos implementations for MathHelper versions
* Switched non-seeded random to use XorShift Random class
* Limit AI Checks
    * Credit to: John200410

### Backports

Credit goes to Paper or Tuinity unless specified in the patch.

* Faster redstone torch rapid clock removal!
* Optimize redstone algorithm aka Eigencraft redstone algorithm
* Optimize Network Manager
* Buffer joins to world
* ItemInHand crash
* Cache EnumDirection adjacent positions
* Optimize time updates
* Reduce memory footprint of NBTTagCompound
* Avoid containsKey -> get() pattern for getTileEntity
* waitForAsyncTasksShutdown on shutdown
* cap per-thread NIO cache size when not specified by the server owner

### Removed Paper or Vanilla Features

* Anti-Xray
* LegacyPingHandler

### Fixed Vanilla Bugs

* MC-47080 - Spectators count as "players" for purposes of sleeping in SMP
