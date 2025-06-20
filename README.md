# EV Charging Time Series Simulation

This repository contains simulated electric vehicle (EV) charging time series data for 100 households for the years **2023**, **2037**, and **2045**, based on projected EV penetration levels. The data is derived from real-world measurements (the Pecan Street dataset) using actual charging behavior from households with EVs.

---

## Penetration Assumptions

| Year | EV Penetration | # Households with EVs |
|------|----------------|------------------------|
| 2023 | 3%             | 3                      |
| 2037 | 63%            | 63                     |
| 2045 | 87%            | 87                     |

---

## Folder Structure

The main folder ev_charging_data_full/ contains subfolders for each year. Each year folder has 100 files, each representing one household’s EV charging profile. Each file is a Python pickle (.pckl) containing a pandas DataFrame with time series data.

```plaintext
ev_charging_data_full/
├── 2023/
│ ├── household_0.pckl
│ ├── household_1.pckl
│ └── ...
├── 2037/
│ ├── household_0.pckl
│ ├── household_1.pckl
│ └── ...
└── 2045/
├── household_0.pckl
├── household_1.pckl
└── ...
```


## How Data Was Generated

- Raw data from `1minute_data_austin.csv`(from https://www.pecanstreet.org/dataport/licenses/)
- Only households with `car1` or `car2` activity were used
- 3%, 63%, and 87% EV penetration assumed in years 2023, 2037, and 2045 respectively
- Random households assigned EVs based on penetration, and a realistic charging profile was chosen from real data
