# Openwrt add Pine64-RTL8201 target
All the Pine64 SBCs are equipped with an **AllWiner A64** SoC AKA (sun50i) features a Quad-Core Cortex-A53 ARM core.

Few Pine64 however, the low-end boards, come with less memory, 512Kb, and a different Ethernet PHY.

While on the compatibility prospect, having less memory won't cause any change in the building tree, having different PHY has a huge impact on Ethernet functionality if the wrong one is used.

OpenWRT comes supporting only the **Pine64+** board. The firmware image produced using this as target provides a firmware where network won't work correctly on "poor" **Pine64**.

The two boards are equipped with two different PHY chips; RTL8201FN for the cheap Pine64, and the RTP8211E for the Pine64+.

The patch presented here lets you add to a standard OpenWrt build tree the new target "Pine64" equipped with the RTL8201FN allowing you to make the network work on the platform.
