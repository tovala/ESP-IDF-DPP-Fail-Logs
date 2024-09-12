# Test Results

- IDF version: `v5.2.1`
- Test device: `ESP32-S3-DevKitC-1`
- Mobile device: `Motorola Edge 2021`
- Mobile device OS: `Android 13`

## Result explanation

- Loop: The device is not responsive to the DPP request, and continues printing the same logs.
- Never exiting from WIFI_EVENT:19: The firmware stops executing after a WIFI_EVENT:19 log.
- ESP_ERR_DPP_TX_FAILURE: The DPP request failed to transmit.
- Failed ROC: Failed when executing `esp_wifi_remain_on_channel`

## Verbose logs, no WPA logs

> out#.log

| Run                | Result  | Reason                              |
| ------------------ | ------- | ----------------------------------- |
| 1                  | Success |                                     |
| [2](./out2.log)    | Failure | Loop                                |
| 3                  | Success |                                     |
| 4                  | Success |                                     |
| 5                  | Success |                                     |
| [6](./out6.log)    | Failure | Loop                                |
| 7                  | Success |                                     |
| [8](./out8.log)    | Failure | Loop                                |
| 9                  | Success |                                     |
| 10                 | Success |                                     |
| [11](./out11.log)  | Failure | ESP_ERR_DPP_TX_FAILURE              |
| 12                 | Success |                                     |
| 13                 | Success |                                     |
| [14](./out14.log)  | Failure | Never exiting from WIFI_EVENT:19    |
| [15](./out15.log)  | Failure | ESP_ERR_DPP_TX_FAILURE              |
| [16](./out16.log)  | Failure | Loop                                |
| [17](./out17.log)  | Failure | DPP success, wifi connection failed |
| 18                 | Success |                                     |
| 19                 | Success |                                     |
| 20                 | Success |                                     |
| [21](./out21.log)  | Failure | ESP_ERR_DPP_TX_FAILURE              |
| [22](./out22.log)  | Failure | Loop                                |
| 23                 | Success |                                     |
| 24                 | Success |                                     |
| 25                 | Success |                                     |
| 26                 | Success |                                     |
| [27](./out27.log)  | Failure | Never exiting from WIFI_EVENT:19    |
| 28                 | Success |                                     |
| [29](./out29.log)  | Failure | Loop                                |
| [30](./out30.log)  | Failure | Loop                                |
| 31                 | Success |                                     |
| 32                 | Success |                                     |
| 33                 | Success |                                     |
| [34](./out34.log)  | Failure | Loop                                |
| 35                 | Success |                                     |
| [36](./out36.log)  | Failure | Loop                                |
| [37](./out37.log)  | Failure | Loop                                |
| [38](./out38.log)  | Failure | Loop                                |
| 39                 | Success |                                     |
| 40                 | Success |                                     |

## Verbose logs, WPA logs

> wpa_out#.log

| Run                   | Result  | Reason                           |
| --------------------- | ------- | -------------------------------- |
| [1](./wpa_out1.log)   | Failure | Failed ROC                       |
| [2](./wpa_out2.log)   | Failure | Failed ROC                       |
| [3](./wpa_out3.log)   | Failure | Failed ROC                       |
| [4](./wpa_out4.log)   | Failure | Failed ROC                       |
| [5](./wpa_out5.log)   | Failure | Failed ROC                       |
| [6](./wpa_out6.log)   | Failure | Never exiting from WIFI_EVENT:19 |
| [7](./wpa_out7.log)   | Failure | Loop                             |
