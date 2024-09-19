# Test Results

- IDF version: `v5.2.1`
- Test device: `ESP32-S3-DevKitC-1`
- Mobile device: `Motorola Edge 2021`
- Mobile device OS: `Android 13`
- AP: `TP-Link Archer A54`
- Sniffer: `Turris Omnia`
- Build: [dpp_test_build_521_2](https://github.com/espressif/esp-idf/issues/10615#issuecomment-2348954979)

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
| [3](./out3.log)    | [3](./out3.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE            |
| [4](./out4.log)    | [4](./out4.pcapng)   | Success |                                   |
| [5](./out5.log)    | [5](./out5.pcapng)   | Success |                                   |
| [6](./out6.log)    | [6](./out6.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE            |
| [7](./out7.log)    | [7](./out7.pcapng)   | Success |                                   |
| [8](./out8.log)    | [8](./out8.pcapng)   | Success |                                   |
| [9](./out9.log)    | [9](./out9.pcapng)   | Success |                                   |
| [10](./out10.log)  | [10](./out10.pcapng) | Success |                                   |
