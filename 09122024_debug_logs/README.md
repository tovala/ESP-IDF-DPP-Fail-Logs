# Test Results

- IDF version: `v5.2.1`
- Test device: `ESP32-S3-DevKitC-1`
- Mobile device: `Motorola Edge 2021`
- Mobile device OS: `Android 13`
- Build: [dpp_test_build_s3](https://github.com/espressif/esp-idf/issues/10615#issuecomment-2345971419)

----

> out#.log

| Run                | Result  | Reason                              |
| ------------------ | ------- | ----------------------------------- |
| [1](./out1.log)    | Success |                                     |
| [2](./out2.log)    | Success |                                     |
| [3](./out3.log)    | Failure | Failed first attempt instantly, retrying failed, rescanning QR code failed; Never exiting from WIFI_EVENT:19 |
| [4](./out4.log)    | Success |                                     |
| [5](./out5.log)    | Success |                                     |
| [6](./out6.log)    | Success |                                     |
| [7](./out7.log)    | Failure | ESP_ERR_DPP_TX_FAILURE              |
| [8](./out8.log)    | Failure | Failed first 3 attempts; Never exiting from WIFI_EVENT:19 |
| [9](./out9.log)    | Failure | Unknown failure                     |
| [10](./out10.log)  | Failure | Never exiting from WIFI_EVENT:19    |
| [11](./out11.log)  | Success |                                     |
| [12](./out12.log)  | Failure | Never exiting from WIFI_EVENT:19    |
| [13](./out13.log)  | Success |                                     |
| [14](./out14.log)  | Success |                                     |
| [15](./out15.log)  | Failure | Failed first 3 attempts; Never exiting from WIFI_EVENT:19 |
| [16](./out16.log)  | Success |                                     |
| [17](./out17.log)  | Failure | ESP_ERR_DPP_TX_FAILURE              |
| [18](./out18.log)  | Success |                                     |
| [19](./out19.log)  | Success |                                     |
| [20](./out20.log)  | Success | DPP succeeded, but wifi failed to connect |
