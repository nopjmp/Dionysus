<!-- SPDX-License-Identifier: MIT -->
# Changelog

All notable changes to this project will be documented in this file.

## [Unreleased]

### Added

### Changed

### Deprecated

### Removed

### Fixed

### Security

## [0.1.3] - 2020-02-10

### Fixed

* Dispenser Shulker Box Crash

## [0.1.2] - 2020-02-10

### Removed

* AntiPhysics crash
  * this was half baked and not fully tested, needs more work.

## [0.1.0] - 2020-02-09

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
