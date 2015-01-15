kernel_mako
==========================

Android kernel for Nexus 4 (mako)

*aiming for better battery life with performance capabilities*

Based on Googles stock Kernel for Nexus 4
branch: **android-5.0.1_r1**


[changes]
---------
- Changed "perf" to "lolzen"
- Updated to Linux 3.4.105
- Possible to compile with gcc 4.7/4.8/4.9
- Fix building sdiv/udiv instructions for cortex-A15
- Added mako_lolzen_defconfig
- Added lolzen_tools

[optimizations]: 
----------------
- Krait optimizations
- neon kernel mode (neon-vfpv4)
- [CFLAGS]:
	- -mtune=cortex-a15 
	- -march=armv7-a 
	- -mfpu=neon-vfpv4
	- -ffast-math
	- -O3
	- -funsafe-math-optimization
	- -fgraphite-identity -floop-interchange -floop-block

[features]:
-----------
- GPU Overclock to 487,5 MHz
- additional lower frequency: 192 MHz set as default idle freq (when not in deep sleep)
- kexec-hardboot (MultiROM patch)
- ROW & SIO scheduler
- SmartAssV2 & Intellidemand Governors
- auto_hotplug (offline mode for cores when not needed)
- usb host mode (USB OTG) [Note: No framework changes, recommended app: StickMount)

[Thanks to]
- Google
- The Linux Foundation
- The community for shared patches

[ToDo]
- DT2W
- msm_thermal drivers
- Init.d support
- F2FS
- PRIMA updates
- stereo speaker option
- Voltage Control
- mute compile warnings