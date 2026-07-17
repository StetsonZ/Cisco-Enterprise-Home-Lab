## Configured Layer 3 EtherChannel in the Incorrect Order

After configuring the Layer 3 EtherChannel between DSW1 and DSW2, the EtherChannel remained suspended and the member interfaces stayed down. After reviewing the running configuration, I discovered that one of the required commands had not been applied correctly on DSW2. Additionally, I learned that when configuring a Layer 3 EtherChannel, the physical interfaces must first be converted to routed ports using the `no switchport` command before assigning them to a channel group. After correcting the interface configuration and recreating the EtherChannel in the proper order, the Port-Channel came up successfully and Layer 3 connectivity was restored.

**Lesson learned:** When configuring Layer 3 EtherChannels, convert interfaces to routed ports before assigning them to a channel group.
## HSRP Failed Due to Missing Redundant Trunk Links

After configuring HSRP on both distribution switches, each switch reported itself as Active and failed to recognize the other as its standby peer. I determined that the redundant links between the distribution and access layers had not yet been configured as trunk ports, preventing HSRP hello packets from reaching the peer switch over the VLANs. After configuring the redundant links as 802.1Q trunks and allowing the required VLANs, HSRP neighbors were successfully established and gateway redundancy began operating as expected.

**Lesson learned:** HSRP relies on Layer 2 connectivity between switches. Proper trunk configuration is required before HSRP can establish neighbor relationships.
## Upgraded Cisco IOS Using a TFTP Server

While beginning the OSPF configuration on DSW2, the switch returned the error:

> `Protocol not in this image`

Comparing the software versions of both distribution switches revealed that DSW1 was running the **IP Services** feature set while DSW2 was running the **IP Base** feature set, which does not support OSPF.

To resolve the issue, I configured a TFTP server using **Tftpd64** on my workstation. I connected my PC to the lab network through ASW1, copied the IOS image from DSW1 to the PC using TFTP, then transferred the image from the PC to DSW2. After updating the boot variable and reloading the switch, DSW2 successfully booted into the IP Services image, allowing OSPF configuration to proceed.

**Lesson learned:** Different Cisco IOS feature sets provide different capabilities. Verifying the installed image before configuring advanced features can prevent unnecessary troubleshooting, and TFTP provides an efficient method for performing IOS upgrades on Cisco devices.
