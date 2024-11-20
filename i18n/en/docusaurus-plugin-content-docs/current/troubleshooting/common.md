---
description: Can't start the game? Can't log into the server or world?
---
# Solving Common Issues
Step-by-step guide to solving the most popular issues
:::info
If this guide helped you identify the cause of your issue, please do not contact our support team - we won't be able to fix the problem. Reach out to the author of the problematic mod instead!
:::

## Issues with entering the world or servers {#no-crashes}
The game doesn't crash but shows an error when trying to enter a server or single-player world?

### Check your nickname {#nickname}
Different game versions have different nickname requirements. The most universal nickname consists of **no more than 16 characters, using Latin letters, numbers, and the characters `_-.`.**  
An invalid nickname may prevent you from joining servers or even single-player games.

### Check your internet connection {#connection}
Can't connect to a server? Can't log into your account? Is the game downloading slowly? Try enabling a VPN and checking if the issue persists. If it resolves - the problem might be with your ISP (blocking issues?).
:::tip
In some cases, software designed to bypass blocks may **interfere** with the game. Try disabling proxies, VPNs, GoodbyeDPI, Zapret, and other "unblockers" or "accelerators".  
Special mention goes to SafeIP - **do not use it, as it causes game crashes and is very hard to remove!**
:::
:::note
Try connecting to a different multiplayer server. If the problem occurs **on all servers**, it is likely an issue on your PC's side, such as with antivirus software.
:::

### Antivirus Software {#av-software}
Antiviruses often cause issues.  
Is the game download stuck at a specific file count? Can't launch or update the launcher? Likely, antivirus software is interfering. Temporarily disable it or add the launcher to its exceptions.

### Crashes when installing a resource pack? {#server-resources}
Try installing the resource pack manually. Test with a different game version.

### Random server crashes? {#server-crashes}
Many servers designed for multiple game versions flood the game with errors by sending incorrect data to clients. Some game versions and mods are particularly sensitive to these errors, causing crashes. Try a different game version, mods setup, or if nothing helps - a different server.

## Issues with launching the game or crashes during gameplay {#crashes}
Game crashing? "Something went wrong"? Here's your guide!

### Game broke after installing a specific mod {#known-mod}
You already know which mod is causing the error, so please contact the mod's author.

### Check available disk space {#check-free-space}
As simple as it sounds, many forget this. The game won't work if your hard drive is running out of space.

### Verify the game version you're launching {#check-version}
A common issue arises when you install mods for one version of the game or mod loader but launch another. **Check your mods!**
:::note
Carefully verify the game version. Players often confuse `1.12` with `1.12.2`, or `1.20.1` with `1.21`. **Mods are written specifically for particular game versions** and likely won't run on newer or older versions. **Be vigilant!**
:::
:::warning
**Even if you're sure** no mods are installed, if you're launching a mod-supported version (like Forge/Fabric...), still check the mods folder!
:::
:::tip
Using [version-specific subfolders](../launcher/subfolders) helps avoid such issues.
:::

### Removing duplicate mods {#remove-duplicates}
Most mod loaders fail when encountering multiple versions of the same mod. Ensure each mod is installed only once.  
In older game versions, mods could be installed in both the `mods` folder and `mods/version-number`. **Check both folders**.
:::note[BetterPVP and Xaero Minimap]
BetterPVP already includes Xaero Minimap, and these mods will conflict.
:::
:::note[OptiFine]
If you selected a version with OptiFine, e.g., "ForgeOptiFine" - **remove OptiFine from the mods folder** or **choose a version without OptiFine, e.g., just "Forge"**. Having OptiFine in both the version and mods folder **will cause a conflict!**
:::
:::tip
Some mods for older versions (like 1.7.10 and 1.12.2) may automatically download and leave files in the `mods/version-number` folder. Carefully check its contents when removing mods - you might forget to delete a component that could cause crashes.
:::

### Removing OptiFine {#remove-optifine}
Yes, this solution is so common we've given it its own section.  
Many mods conflict with OptiFine. The first step is to remove OptiFine (choose a version without OptiFine and delete its files from the mods folder) and see if the game launches. If you're using Fabric - **do not use OptiFine or OptiFabric!**
:::note
If this step didn't help, don't reinstall OptiFine. Continue troubleshooting without it. You can always try reintroducing OptiFine after identifying the problem source (but we recommend using [alternatives](../faq/optifine-alternatives)).
:::

### Check mods for conflicts {#mod-conflicts}
You might have installed incompatible mods. Common incompatible combinations include:
* OptiFine and Sodium (Magnesium, Rubidium, Embeddium...) or Iris (Oculus). Remove OptiFine.
* OptiFine and Connector. Remove OptiFine.
* Installing different Sodium ports simultaneously (e.g., Rubidium and Embeddium).
* Mismatched AE2 versions and addons (e.g., AE2 rv3 with addons for rv2).
* VulkanMod. It conflicts with almost all mods (especially OptiFine, Sodium, etc.).
* DistantHorizons is highly version-specific with Sodium/Iris.
* Sodium versions below 0.6.0 break many Fabric mods unless [Indium](https://modrinth.com/mod/indium) is installed.
* Many Fabric mods require `fabric` (a.k.a. `fabric-api`, which includes mods with names like `fabric-api-something`). [Install it](https://modrinth.com/mod/fabric-api).
* Common conflict sources include MorePlayerModels, CustomNPCs, EpicFight mods.

### Check for known broken mods {#broken-mods}
* Most cheats, hacks, cracks, and other modifications, **especially** those requiring `-noverify`, will crash frequently. Avoid them!
* OptiFabric breaks compatibility with many mods. Do not use it.
* MemoryLeakFix and NotEnoughCrashes may break after Fabric updates.
* ModernFix breaks after Forge updates.
* Some known workarounds for popular mods can be found [here](/mod-specific)

### Check mod loader error messages
:::note[TODO!]
Examples of Forge, Fabric, and Quilt error windows needed here.
:::
Many mod loaders display a window describing the issue. Often, they highlight duplicates, missing dependencies, or mismatched versions.

### Reset configuration files {#drop-configs}
Corrupted configuration files are a common issue. Rename the `config` folder in the game directory (or delete it if there's nothing important to you inside) and try launching the game. Mods will re-create the folder and all files inside.

### Try the "refresh client" option {#force-update}
Your game files may be corrupted. Re-download them using the "Force update" checkbox or [manually reinstall the version](/tags/modloader).

### Check launcher settings {#check-args}
Go to Java settings in your launcher. Try removing all JVM arguments entered there.

## Nothing helps? {#support}
(Contact our support team)[../support/game] or try (self-repair guide)[./self-repair].