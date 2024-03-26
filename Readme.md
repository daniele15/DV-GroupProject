## Thông tin các file: 
#### 1. `raw.csv`
> File lớn nhất chứa hầu hết data từ ngày 22/03/2020 về sau
> gồm các cột: `FIPS`, `Admin2`, `Province_State`, `Country_Region`, `Last_Update`, `Lat`, `Long_`, `Confirmed`, `Deaths`, `Recovered`, `Active`, `Combined_Key`, `Incident_Rate`, `Case_Fatality_Ratio`

### 2. `bef.csv`
> File chứa data từ 21/03/2020 về trước (22/01/2020)
> Gồm các cột: `Province/State`, `Country/Region`, `Last Update`, `Latitude`, `Longitude`, `Confirmed`, `Deaths`, `Recovered`

### 3. `raw_full_merged_df.csv`
> File merge các files 1 và 2 (có các cột như 1)

### 4. `full_data_final.csv`
> File cuối dùng cho tableau (dữ liệu đến 5/8/2021, do sau đó người cập nhật không ghi nhận recovered nữa)
> Gồm các cột: `Country_Region`, `Last_Update`, `Confirmed`, `Deaths`, `Recovered`, `Active`, `WHO Region`, `New cases`, `New deaths`, `New recovered`

### 5. `country_wise_latest_2021.csv`
> Giống file country_wise_latest nhưng dữ liệu đến 5/8/2021 + có population
> Gồm các cột: `Country_Region`, `Confirmed`, `Deaths`, `Recovered`, `Active`, `New cases`, `New deaths`, `New recovered`, `Deaths / 100 Cases`, `Recovered / 100 Cases`, `Deaths / 100 Recovered`, `Confirmed last week`, `1 week change`, `1 week % increase`, `WHO Region`, `Population`

Link đến data: [Folder](https://drive.google.com/drive/folders/1X5nbd8QFwFSWgZkvYOz9YndppHs5rFJY?usp=sharing)
