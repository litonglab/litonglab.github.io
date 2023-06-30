---
title: 'TACK'
weight: 1
bookcase_cover_src: 'images/project_tack.png'
bookcase_cover_src_dark: 'images/project_tack.png'
changelogs:
---

**Project Name**: TACK

[ [Github] ](https://github.com/superlitong/fillp-demo)

[ [Video and Slides] ](https://github.com/superlitong/tack-paper-slides-video)

**Abstract**

The shared nature of the wireless medium induces contention between data transport and backward signaling, such as acknowledgement. The current way of TCP acknowledgment induces control overhead which is counter-productive for TCP performance especially in wireless local area network (WLAN) scenarios. In this paper, we present a new acknowledgement called TACK ("Tame ACK"), as well as its TCP implementation TCP-TACK. TCP-TACK works on top of commodity WLAN, delivering high wireless transport goodput with minimal control overhead in the form of ACKs, without any hardware modification. To minimize ACK frequency, TACK abandons the legacy received-packet-driven ACK. Instead, it balances byte-counting ACK and periodic ACK so as to achieve a controlled ACK frequency. Evaluation results show that TCP-TACK achieves significant advantages over legacy TCP in WLAN scenarios due to less contention between data packets and ACKs. Specifically, TCP-TACK reduces over 90% of ACKs and also obtains an improvement of ∼28% on goodput. We further find it performs equally well as high-speed TCP variants in wide area network (WAN) scenarios, this is attributed to the advancements of the TACK-based protocol design in loss recovery, round-trip timing, and send rate control.



**Reference**

- Tong Li, Kai Zheng, Ke Xu, Rahul Arvind Jadhav, Tao Xiong, Keith Winstein, Kun Tan. TACK: Improving Wireless Transport Performance by Taming Acknowledgments. Annual conference of the ACM Special Interest Group on Data Communication on the applications, technologies, architectures, and protocols for computer communication (ACM SIGCOMM), pp. 15-30, 2020.

- Tong Li, Kai Zheng, Ke Xu, Rahul Arvind Jadhav, Tao Xiong, Keith Winstein, Kun Tan. Revisiting Acknowledgment Mechanism for Transport Control: Modeling, Analysis, and Implementation. IEEE/ACM Transactions on Networking (TON), vol.29, no.6, pp. 2678-2692, 2021.

- Tong Li, Kai Zheng, Ke Xu. Acknowledgment On Demand for Transport Control. IEEE Internet Computing, vol.25, no.2, pp. 109-115, 2021.

{{< figure src="/images/project_tack.png" caption="Performance evaluation of TACK." >}}