# Dataset Information

## About the Dataset

**Dataset Files**: Train.csv, Test.csv  
**Source**: Academic coursework (CS5062 - Machine Learning)  
**Size**: ~60,000+ observations  
**Type**: Electric vehicle operational data

## Features

The dataset includes:
- **Trip**: Trip identifier
- **VehicleSpeed_km_h_**: Vehicle speed in km/h
- **Battery_Status**: Binary target (0 = discharging, 1 = charging)

## Data Characteristics

- **Temporal Structure**: Sequential trip data with time dependencies
- **Class Imbalance**: Unequal distribution of charging/discharging states
- **Real-World Data**: Operational EV data with natural variability

## Data Availability

This dataset is from academic coursework at the University of Aberdeen and is **not included in this repository**.

To run the notebooks:
1. Place your datasets in a `data/` folder in this directory
2. Ensure files are named `Train.csv` and `Test.csv`
3. The notebooks will automatically load from `./data/Train.csv` and `./data/Test.csv`

## Alternative

If you're interested in the methodology and results without running the code:
- Review the comprehensive README.md in this folder
- View the notebook outputs (if preserved)
- Contact for dataset access or collaboration

---

**Note**: Dataset available upon request for academic or research purposes.
