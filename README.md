# FORKED FOR ARCHIVE PURPOSES (ENG Translated)

# 📢 Note
I understand, of course. Work should be paid, and piracy is a criminal offense in some countries,
but mere mortals shouldn't have to suffer because of tilting at windmills. Especially users of Huawei phones without Google Play
and ideological opponents of Google (I, for example, wouldn't give them a dime even if I could),
who are completely deprived of the opportunity to play with mods due to someone's whim. They
may have been able to buy a game on their phone from Google Play at one point, but having switched to
Huawei/having gotten rid of Google, they will be forced to suffer without mods, getting punched in the face
without a shred of sympathy or a solution. Moreover, if you believe the internet, even previously purchased copies from Google Play can no longer be installed in Russia. Consequently, there isn't much choice.

![image](./img/windmills.png)

It's not my style to be offended by the mentally ill people that ardent copyright zealots are.
The game is DRM-free, so this repository and fork don't violate the original license, the game's license, or anyone else's rights, as it doesn't allow anything to circumvent the already absent license check in the pure game. Not doing something isn't prohibited by law,
just like creating a fork that doesn't do what the original did.

# 🛠️ SMAPI Launcher
![image](https://github.com/user-attachments/assets/09a5f3fa-0b99-4aae-8f47-2de9009d5209)

# 🌟 Features
- Send logs to the SMAPI server with one button.
- Update SMAPI without reinstalling the game or loader.
- No labor-intensive manual manipulation required.
- Support for games installed from the Galaxy Store, Google Play, and via APK.
- Transparent build via GitHub Actions.
The APK is built directly from the contents of this repository in a clean and controlled virtual machine provided by GitHub. You can track the progress and download the latest build here:
  [![.NET](https://github.com/IvanKr08/SMAPILoader-Googleless/actions/workflows/publish.yml/badge.svg)](https://github.com/IvanKr08/SMAPILoader-Googleless/actions/workflows/publish.yml)


# 🕒 Plans
- [ ] Russification of SMAPI Launcher itself.
- [ ] Import/export/backup saves.
- [ ] Automatically download/update SMAPI.
- [x] ~~Automated build via GitHub Actions~~
- [x] ~~Android 5.~~ Currently confirmed to work on Android 5.1.
- [ ] ARM32, x86, and AMD64 support. Runtime patches have been written, but MonoMod hasn't been ported to ARM32 yet,
and I don't have native libraries for x86/AMD64. Furthermore, I'm not sure Stardew Valley even exists for these architectures. But if it does, please share the libraries from the APK.


# 📲 Installation
1. Download/compile and install [SMAPI Launcher](https://github.com/IvanKr08/SMAPILoader-Googleless/releases).
   Experimental builds are available in [GitHub Actions](https://github.com/IvanKr08/SMAPILoader-Googleless/actions).
2. Download SMAPI.4.x.x-(xxxx).zip [from here](https://github.com/NRTnarathip/SMAPI-Android-1.6/releases)
   **(The author has stopped releasing new SMAPI builds on GitHub, only on the Thai Discord.)**.
3. Launch SMAPI Launcher.
4. "Install SMAPI From Zip", then select the file with SMAPI.
5. Wait until it says "Successfully Install SMAPI".
6. "Start Game", After which SMAPI Launcher will clone the game, inject SMAPI and launch it.
7. Make sure the game is working, then install the desired mods through the built-in manager.

# ‼️ Known Issues
- A new save *isn't created* and the message "SMAPI Launcher is not responding" appears.
	- Don't tap the screen after confirming character creation; the game may take up to a minute to process.
	If the message still appears, restart the game immediately after entering the world.
	Loading an existing save takes 5-10 seconds and doesn't trigger this message.
- Mod X is disabled due to incompatibility. Please update the mod.
  - Most mods labeled "designed for Android" were created for mobile SMAPI 1.5 and are incompatible with the new fork.
	The PC version is more commonly used.
- The mod supposedly loads, but in practical it doesn't work or throws errors in the console.
  - Mobile SMAPI is in its development, and some internal aspects of the game differ from the desktop version.
	You can contact the mod's author with a request to fix it, but it's unlikely they'll be interested or even see the feasibility.
	Otherwise, you'll have to either abandon the mod or fix it yourself (after which you can offer the patch to the author).
	You'll need to unpack the game assemblies from the APK (assemblies.blob file) and have a basic understanding of C#.
After that, there are two options:
      1. Download the source code, include the dependencies (specifically StardewValley.dll and StardewModdingAPI.dll) and build it.
      2. Patch incompatibilities with dnSpyEx. It's generally simpler and faster, and it allows you to fix mods
		with closed source code, but it's somewhat outdated and can be quite intimidating due to the number of obscure features
		(which you don't need). It's also highly recommended to understand how the stack-based virtual machine works,
		so you can modify MSIL directly. Code from a decompiler doesn't always recompile.
  - Moreover, compatibility may break between SMAPI versions. Try 4.1.&ast;, 4.2.&ast; и 4.3.&ast;.

# #️⃣ Support
Original Discord server - SMAPI Thailand: https://discord.com/invite/ETtycvcJjr

**Don't expect to get any help there for this fork. At best, they won't answer you,
at worst, they might call you very nasty names and even ban you.**

For any problems or questions, please write to [Issues](https://github.com/IvanKr08/SMAPILoader-Googleless/issues)
and [Discussions](https://github.com/IvanKr08/SMAPILoader-Googleless/discussions).

If you don't have a GitHub account, then [4PDA](https://4pda.to/forum/index.php?showtopic=945283)
or [Russian Discord Server](https://discord.gg/XCka9TDaGx).
In the last two cases, don't forget to ping me (IvanKr08), because I don't just read them.

# 📦 Building
1. Install .NET SDK 8 and the Android SDK (I don't know anything about Android, but your SDK must support API 29).
	The Android SDK must be specified in the ANDROID_HOME variable. If you're using Visual Studio,
	you'll need to install the entire MAUI toolchain.
   (For some reason, the SDK manager doesn't appear, even if you install everything separately from MAUI.).
2. Clone or download the repository.
3. Open cmd and go to the repository folder.
4. "dotnet workload restore" (3+GB of free space on the system partition is required).
5. "dotnet run --project LibPatcher patch".
   This will automatically patch the Mono runtime. If you don't do this, the game will fail to launch due to a MethodAccessException.
(If you didn't patch it immediately, be sure to remove obj and bin before rebuilding.). [More information](/LibPatcher).
6. Pray and perform "dotnet publish ./SMAPIGameLoader".
7. If any errors occur, please report them via [Issues](https://github.com/IvanKr08/SMAPILoader-Googleless/issues) or
	try to fix it yourself.
8. If the build is successful, you can install the resulting APK.
