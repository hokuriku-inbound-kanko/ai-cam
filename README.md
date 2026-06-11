# ai-cam

日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

Open demographic data collected by AI cameras at Fukui Station for inbound tourism analysis, published by the Hokuriku Inbound Tourism DX Data Consortium.

## Background
This repository provides demographic insights from AI-powered cameras deployed to analyze inbound tourism patterns. The data supports regional tourism strategies by estimating visitor gender, age, nationality, and face orientation at Fukui Station, a key transportation hub in the Hokuriku region of Japan.

## Data File
The dataset is stored in a single CSV file:
- **`fukui_station.csv`**: Contains timestamped records of visitor demographics with confidence scores for AI predictions. Each row represents an individual detection with attributes like gender, age, nationality classifications, and face direction.

## Column Reference
| Column          | Description                                                                                     | Values / Range                          |
|------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------|
| `gender`         | Gender classification                                                                           | `1` = male, `0` = female                |
| `age`            | Estimated age of the individual                                                                 | Integer (e.g., 20, 65)                  |
| `accuracy`       | Confidence score for gender & age prediction                                                    | `0.000`–`1.000`                         |
| `nationality1`   | Nationality classification (Japanese vs. non-Japanese)                                          | `1` = Japanese, `0` = non-Japanese      |
| `accuracy`       | Confidence score for nationality1 prediction                                                    | `0.000`–`1.000`                         |
| `nationality2`   | Nationality classification (Western vs. non-Western)                                            | `1` = Western, `0` = non-Western        |
| `accuracy`       | Confidence score for nationality2 prediction                                                    | `0.000`–`1.000`                         |
| `nationality3`   | Nationality classification (non-Western excluding Western vs. others)                           | `1` = non-Western (excluding Western), `0` = not |
| `accuracy`       | Confidence score for nationality3 prediction                                                    | `0.000`–`1.000`                         |
| `direction`      | Face orientation relative to the camera                                                         | `0` = front, `0.5` = back, `1` = full rotation front |

## Data Collection
The data was collected using **AI cameras developed by Kanazawa University**, deployed at **Fukui Station**. These cameras analyze real-time video feeds to estimate demographic attributes and face orientation, providing insights into visitor behavior and demographics.

## Published By
This dataset is published by the **Hokuriku Inbound Tourism DX Data Consortium**, a collaborative initiative promoting data-driven strategies to enhance inbound tourism in the Hokuriku region.

## License
MIT License. See [LICENSE](LICENSE) for details.
