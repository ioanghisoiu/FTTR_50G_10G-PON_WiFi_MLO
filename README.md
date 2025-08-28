# FTTR_50G_10G-PON_WiFi_MLO
About This is an event-driven simulation of dynamic bandwidth allocation (DBA) in Fiber-To-The-Room (FTTR) network, where the External PON is a 50 Gbps Gigabit Passive Optical Network (50G-PON) with split-ratio 1:16 and the Internal PON is a 10G-PON with split-ratio 1:8 with WiFi-7 multi-link operation (MLO). Note that MAC is abstracted.

The WiFi access points operate on 5 GHz and 6 GHz bands. Out of 16 antennas, 8 are operating in 6 GHz and the remaining 8 are operating in 5 GHz.
For the current use case, only XR devices are connected to 6 GHz band with bandwidth 320 MHz. These STAs are configured with 8 spatial streams and MCS 13. 
Other devices, e.g., Head Mount Device (HMD) orientations, Control, Haptics, and Background devices are connected to 5 GHz band with total bandwidth 160 MHz. If they report buffer status report (BSR) > 0, then minimum 40 MHz bandwidth is allocated. Maximum can be 160 MHz, with granularity 2, 4, 8, 20, 40, 80, 160 MHz. These STAs are configured with 2 spatial streams and MCS 11. The actual throughput can be adjusted using normalized channel gains.
As OFDMA is considered, each TXOP is considered to be 1 msec interval. This time is divided into DL and UL transmission times according to the traffic load [4].

<img width="1280" height="648" alt="image" src="https://github.com/user-attachments/assets/3b5de562-9830-4c17-9d12-5cec802c9228" />

References:
[1] Sourav Mondal and Elaine Wong, “User Head Movement-Predictive XR in Immersive H2M Collaborations over Future Enterprise Networks,” IEEE Internet of Things Journal, July 2025.
[2] Sourav Mondal and Elaine Wong, “Enabling Immersive XR Collaborations over FTTR Networks (Invited),” in 2025 Optica Advanced Photonics Congress (APC), Marseille, France, July 2025. 
[3] Sourav Mondal and Elaine Wong, “Fiber-WiFi Coordinated Seamless Handover and Resource Allocation for Immersive XR Collaborations over FTTR-B,” in 2025 Optical Fiber Communication Conference and Exposition (OFC), San Francisco, USA, March 2025.
[4] E. Khorov, I. Levitsky and I. F. Akyildiz, "Current Status and Directions of IEEE 802.11be, the Future Wi-Fi 7," in IEEE Access, vol. 8, pp. 88664-88688, 2020.
