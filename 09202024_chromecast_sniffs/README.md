# Test Results

- Test device: `Google Chromecast`
- Mobile device: `Motorola Edge 2021`
- Mobile device OS: `Android 13`
- AP: `TP-Link Archer A54`
- Sniffer: `Turris Omnia`

Method used for capturing logs:
- Router:
  - `ifconfig wlan0 down`
  - `iwconfig wlan0 mode monitor`
  - `ifconfig wlan0 up`
  - `iwconfig wlan0 channel 6`
  - `tcpdump -n -i wlan0 -vvv -w - not port 12521 | nc <IP_OF_WINDOWS_PC> 12521`
- Windows PC: `ncat -l -p 12521 | "C:\Program Files\Wireshark\Wireshark.exe" -k -S -i -`

----

> out#.log, out#.pcapng

| pcapng                     | Result  | Reason                            |
| -------------------------- | ------- | --------------------------------- |
| [1](./google_out1.pcapng)  | Success |                                   |
| [2](./google_out2.pcapng)  | Success |                                   |
| [3](./google_out3.pcapng)  | Success |                                   |
| [4](./google_out4.pcapng)  | Success |                                   |
| [5](./google_out5.pcapng)  | Success |                                   |
| [6](./google_out6.pcapng)  | Failure |                                   |
| [7](./google_out7.pcapng)  | Success |                                   |
| [8](./google_out8.pcapng)  | Success |                                   |
| [9](./google_out9.pcapng)  | Success |                                   |
| [10](./google_out10.pcapng) | Success |                                   |
| [11](./google_out11.pcapng) | Success |                                   |
| [12](./google_out12.pcapng) | Success |                                   |
| [13](./google_out13.pcapng) | Success |                                   |
| [14](./google_out14.pcapng) | Success |                                   |
| [15](./google_out15.pcapng) | Success |                                   |
| [16](./google_out16.pcapng) | Success |                                   |
| [17](./google_out17.pcapng) | Success |                                   |
| [18](./google_out18.pcapng) | Success |                                   |
| [19](./google_out19.pcapng) | Success |                                   |
| [20](./google_out20.pcapng) | Success |                                   |
| [21](./google_out21.pcapng) | Success |                                   |
| [22](./google_out22.pcapng) | Success |                                   |
| [23](./google_out23.pcapng) | Success |                                   |
| [24](./google_out24.pcapng) | Success |                                   |
| [25](./google_out25.pcapng) | Success |                                   |
| [26](./google_out26.pcapng) | Success |                                   |
| [27](./google_out27.pcapng) | Success |                                   |
| [28](./google_out28.pcapng) | Success |                                   |
| [29](./google_out29.pcapng) | Success |                                   |
| [30](./google_out30.pcapng) | Success |                                   |
| [31](./google_out31.pcapng) | Success |                                   |
| [32](./google_out32.pcapng) | Success |                                   |
| [33](./google_out33.pcapng) | Success |                                   |
| [34](./google_out34.pcapng) | Success |                                   |
| [35](./google_out35.pcapng) | Success |                                   |
| [36](./google_out36.pcapng) | Success |                                   |
| [37](./google_out37.pcapng) | Success |                                   |
| [38](./google_out38.pcapng) | Success |                                   |
| [39](./google_out39.pcapng) | Success |                                   |
| [40](./google_out40.pcapng) | Success |                                   |
| [41](./google_out41.pcapng) | Success |                                   |
| [42](./google_out42.pcapng) | Success |                                   |
| [43](./google_out43.pcapng) | Success |                                   |
| [44](./google_out44.pcapng) | Success |                                   |
| [45](./google_out45.pcapng) | Success |                                   |
| [46](./google_out46.pcapng) | Success |                                   |
| [47](./google_out47.pcapng) | Success |                                   |
| [48](./google_out48.pcapng) | Success |                                   |
| [49](./google_out49.pcapng) | Success |                                   |
| [50](./google_out50.pcapng) | Failure | Network failure (displayed on monitor) |

