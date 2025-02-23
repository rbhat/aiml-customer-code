# Will the Customer Accept the Coupon?

## Overview
This project explores the factors influencing whether a driver accepts a coupon delivered to their phone while driving. The coupons are for various establishments—restaurants (under $20 or $20–$50), coffee houses, carry-out, or bars—and the decision to accept may depend on user demographics, contextual factors, and coupon attributes. Using visualizations and probability distributions, this project distinguishes between customers who accept a coupon (Y = 1) and those who do not (Y = 0).

The analysis is implemented in Python using a Jupyter Notebook, leveraging data from a survey conducted via Amazon Mechanical Turk, sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/).

## Problem Context
Imagine driving through town when a coupon arrives on your phone for a nearby restaurant. Would you detour to use it immediately, save it for later, or ignore it? How does the decision change if it’s for a bar, a coffee house, or with a passenger in the car? Factors like weather, time of day, and proximity to the venue may play a role. This project investigates what drives coupon acceptance and how to predict it.

## Data Description
The dataset contains survey responses with the following attributes (values are averages):

### 1. User Attributes
- **Gender**: Male, Female
- **Age**: Below 21, 21–25, 26–30, etc.
- **Marital Status**: Single, Married, Unmarried Partner, Widowed
- **Number of Children**: 0, 1, 2+
- **Education**: High School, Bachelors, Associates, Graduate Degree
- **Occupation**: Architecture & Engineering, Business & Financial, etc.
- **Annual Income**: < $12,500, $12,500–$24,999, $25,000–$37,499, etc.
- **Frequency of Visits** (to bars, coffee houses, takeaway, or restaurants < $20): 0, <1, 1–3, 4–8, >8 times

### 2. Contextual Attributes
- **Driving Destination**: Home, Work, No Urgent Destination
- **Location**: Distance and direction between user, destination, and venue (with driving time)
- **Weather**: Sunny, Rainy, Snowy
- **Temperature**: 30°F, 55°F, 80°F
- **Time**: 10 AM, 2 PM, 6 PM
- **Passenger**: Alone, Partner, Kid(s), Friend(s)

### 3. Coupon Attributes
- **Expiration**: 2 hours, 1 day
- **Coupon Type**: Restaurant (< $20), Restaurant ($20–$50), Coffee House, Carry Out, Bar

**Label**: Y = 1 (accepted: "right away" or "later before expiry"), Y = 0 (rejected: "no, I don’t want it")

The dataset is stored in the `/data` subfolder.

## Prerequisites
This project requires the following Python libraries:
- `matplotlib.pyplot` (for plotting)
- `seaborn` (for enhanced visualizations)
- `pandas` (for data manipulation)
- `numpy` (for numerical operations)

Install them using:
```bash
pip install matplotlib seaborn pandas numpy
```


Alternatively, use the provided requirements.txt file:
```pip install -r requirements.txt```

## Repository Structure
```
├── data/               # Dataset files
├── notebook.ipynb      # Jupyter Notebook with analysis
├── README.md           # Project documentation
└── requirements.txt    # Python dependencies
```

## Usage
1. Clone the repository:
    bash
    git clone https://github.com/rbhat/aiml-customer-code.git
2. Navigate to the project directory:
    bash
    cd aiml-customer-code
3. Install dependencies:
    bash
    pip install -r requirements.txt
4. Open the Jupyter Notebook:
    bash
    jupyter notebook notebook.ipynb
    Run the cells to explore the analysis.

## Dependencies
Included in requirements.txt:
matplotlib
seaborn
pandas
numpy
termcolor

## License
This project is unlicensed (public domain) unless otherwise specified. Feel free to use and modify it as needed.

## Acknowledgments
- Data provided by the [UCI Machine Learning Repository](https://archive.ics.uci.edu/).
- Survey collected via Amazon Mechanical Turk.
- Special thanks to Grok, created by xAI, for assistance in drafting this README.
