# Test Results

- IDF version: `v5.2.1`
- Test device: `ESP32-S3-DevKitC-1`
- Mobile device: `Motorola Edge 2021`
- Mobile device OS: `Android 13`
- AP: `TP-Link Archer A54`
- Sniffer: `Turris Omnia`
- Build: [test_build_3oct](https://github.com/espressif/esp-idf/issues/10615#issuecomment-2390582375)

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

| Run                | pcapng               | Result  | Reason                            |
| ------------------ | -------------------- | ------- | --------------------------------- |
| [1](./out1.log)    | [1](./out1.pcapng)   | Success |                                   |
| [2](./out2.log)    | [2](./out2.pcapng)   | Success |                                   |
| [3](./out3.log)    | [3](./out3.pcapng)   | Success | ESP_ERR_DPP_AUTH_TIMEOUT, ESP_ERR_DPP_FAILURE, Failed ROC 0x301c, succeeded on retry |
| [4](./out4.log)    | [4](./out4.pcapng)   | Success |                                   |
| [5](./out5.log)    | [5](./out5.pcapng)   | Success |                                   |
| [6](./out6.log)    | [6](./out6.pcapng)   | Success |                                   |
| [7](./out7.log)    | [7](./out7.pcapng)   | Success |                                   |
| [8](./out8.log)    | [8](./out8.pcapng)   | Success |                                   |
| [9](./out9.log)    | [9](./out9.pcapng)   | Success |                                   |
| [10](./out10.log)  | [10](./out10.pcapng) | Success |                                   |
| [11](./out11.log)  | [11](./out11.pcapng) | Success |                                   |
| [12](./out12.log)  | [12](./out12.pcapng) | Success |                                   |
| [13](./out13.log)  | [13](./out13.pcapng) | Success | ESP_ERR_DPP_TX_FAILURE, phone displayed failure instantly, retired sending frames 4 times, failed, had to press retry on phone |
| [14](./out14.log)  | [14](./out14.pcapng) | Success |                                   |
| [15](./out15.log)  | [15](./out15.pcapng) | Success |                                   |
| [16](./out16.log)  | [16](./out16.pcapng) | Success |                                   |
| [17](./out17.log)  | [17](./out17.pcapng) | Success |                                   |
| [18](./out18.log)  | [18](./out18.pcapng) | Success |                                   |
| [19](./out19.log)  | [19](./out19.pcapng) | Success |                                   |
| [20](./out20.log)  | [20](./out20.pcapng) | Success |                                   |
| [21](./out21.log)  | [21](./out21.pcapng) | Success | DPP auth failed, phone displayed failure instantly, success on retry |
| [22](./out22.log)  | [22](./out22.pcapng) | Success |                                   |
| [23](./out23.log)  | [23](./out23.pcapng) | Success |                                   |
| [24](./out24.log)  | [24](./out24.pcapng) | Success |                                   |
| [25](./out25.log)  | [25](./out25.pcapng) | Success |                                   |
| [26](./out26.log)  | [26](./out26.pcapng) | Success |                                   |
| [27](./out27.log)  | [27](./out27.pcapng) | Success |                                   |
| [28](./out28.log)  | [28](./out28.pcapng) | Success | Dpp auth failed, retry dpp auth failed, succeeded on 2nd retry |
| [29](./out29.log)  | [29](./out29.pcapng) | Success | ESP_ERR_DPP_AUTH_TIMEOUT, ESP_ERR_DPP_FAILURE, Failed ROC 0x301c, succeeded on retry |
| [30](./out30.log)  | [30](./out30.pcapng) | Success |                                   |
| [31](./out31.log)  | [31](./out31.pcapng) | Success |                                   |
| [32](./out32.log)  | [32](./out32.pcapng) | Failure | ESP_ERR_DPP_AUTH_TIMEOUT, ESP_ERR_DPP_FAILURE, Failed ROC 0x301c, connected to wifi on retry, shows failure on phone |
| [33](./out33.log)  | [33](./out33.pcapng) | Success |                                   |
| [34](./out34.log)  | [34](./out34.pcapng) | Success |                                   |
| [35](./out35.log)  | [35](./out35.pcapng) | Success | ESP_ERR_DPP_AUTH_TIMEOUT, ESP_ERR_DPP_FAILURE, Failed ROC 0x301c, succeeded on retry |
| [36](./out36.log)  | [36](./out36.pcapng) | Success | ESP_ERR_DPP_AUTH_TIMEOUT, ESP_ERR_DPP_FAILURE, Failed ROC 0x301c, ESP_ERR_DPP_TX_FAILURE on retry, succeeded on 2nd retry |
| [37](./out37.log)  | [37](./out37.pcapng) | Success |                                   |
| [38](./out38.log)  | [38](./out38.pcapng) | Success |                                   |
| [39](./out39.log)  | [39](./out39.pcapng) | Success |                                   |
| [40](./out40.log)  | [40](./out40.pcapng) | Success | ESP_ERR_DPP_AUTH_TIMEOUT, ESP_ERR_DPP_FAILURE, Failed ROC 0x301c, succeeded on retry |
| [41](./out41.log)  | [41](./out41.pcapng) | Success |                                   |
| [42](./out42.log)  | [42](./out42.pcapng) | Success |                                   |
| [43](./out43.log)  | [43](./out43.pcapng) | Success |                                   |
| [44](./out44.log)  | [44](./out44.pcapng) | Success |                                   |
| [45](./out45.log)  | [45](./out45.pcapng) | Success |                                   |
| [46](./out46.log)  | [46](./out46.pcapng) | Success |                                   |
| [47](./out47.log)  | [47](./out47.pcapng) | Success | ESP_ERR_DPP_AUTH_TIMEOUT, ESP_ERR_DPP_FAILURE, Failed ROC 0x301c, succeeded on retry |
| [48](./out48.log)  | [48](./out48.pcapng) | Success |                                   |
| [49](./out49.log)  | [49](./out49.pcapng) | Success |                                   |
| [50](./out50.log)  | [50](./out50.pcapng) | Success |                                   |
