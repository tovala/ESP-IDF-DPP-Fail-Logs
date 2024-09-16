# Test Results

- IDF version: `v5.2.1`
- Test device: `ESP32-S3-DevKitC-1`
- Mobile device: `Motorola Edge 2021`
- Mobile device OS: `Android 13`
- AP: `TP-Link AC1200`
- Build: [dpp_test_build_521_2](https://github.com/espressif/esp-idf/issues/10615#issuecomment-2348954979)

> Note: The packet captures were taken from wireshark from a device on the target network.
> The AP used did not support packet capture.

----

> out#.log
> out#.pcapng

| Run                | pcapng               | Result  | Reason                 |
| ------------------ | -------------------- | ------- | ---------------------- |
| [1](./out1.log)    | [1](./out1.pcapng)   | Success |                        |
| [2](./out2.log)    | [2](./out2.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE |
| [3](./out3.log)    | [3](./out3.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE |
| [4](./out4.log)    | [4](./out4.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE |
| [5](./out5.log)    | [5](./out5.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE |
| [6](./out6.log)    | [6](./out6.pcapng)   | Success |                        |
| [7](./out7.log)    | [7](./out7.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE |
| [8](./out8.log)    | [8](./out8.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE |
| [9](./out9.log)    | [9](./out9.pcapng)   | Failure | ESP_ERR_DPP_TX_FAILURE |
| [10](./out10.log)  | [10](./out10.pcapng) | Failure | ESP_ERR_DPP_TX_FAILURE |
