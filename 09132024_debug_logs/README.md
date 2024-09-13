# Test Results

- IDF version: `v5.2.1`
- Test device: `ESP32-S3-DevKitC-1`
- Mobile device: `Motorola Edge 2021`
- Mobile device OS: `Android 13`
- Build: [dpp_test_build_521_2](https://github.com/espressif/esp-idf/issues/10615#issuecomment-2348954979)

----

> out#.log

| Run                | Result  | Reason                              |
| ------------------ | ------- | ----------------------------------- |
| [1](./out1.log)    | Success | Failed to connect to wifi, dpp succeeded |
| [2](./out2.log)    | Success | Failed to connect to wifi, dpp succeeded |
| [3](./out3.log)    | Success |                                     |
| [4](./out4.log)    | Failure | ESP_ERR_DPP_TX_FAILURE              |
| [5](./out5.log)    | Failure | ESP_ERR_DPP_TX_FAILURE              |
| [6](./out6.log)    | Success |                                     |
| [7](./out7.log)    | Success |                                     |
| [8](./out8.log)    | Success |                                     |
| [9](./out9.log)    | Failure | ESP_ERR_DPP_TX_FAILURE              |
| [10](./out10.log)  | Success |                                     |
| [11](./out11.log)  | Success | Failed first attempt, succeeded on retry |
| [12](./out12.log)  | Failure | Unknown                             |
| [13](./out13.log)  | Failure | Unknown                             |
| [14](./out14.log)  | Failure | Never exiting from WIFI_EVENT:19    |
| [15](./out15.log)  | Success |                                     |
| [16](./out16.log)  | Success |                                     |
| [17](./out17.log)  | Failure | Never exiting from WIFI_EVENT:19    |
| [18](./out18.log)  | Success |                                     |
| [19](./out19.log)  | Failure | Never exiting from WIFI_EVENT:19    |
| [20](./out20.log)  | Success |                                     |
