# 🚕 NYC Taxi Trip Duration Analysis
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)](https://pandas.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-3.0+-orange.svg)](https://matplotlib.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-0.11+-red.svg)](https://seaborn.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📋 Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Analysis Process](#analysis-process)
- [Analysis Results](#analysis-results)
- [Project Structure](#project-structure)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

## 🎯 Project Overview

*This is a mini-project to show exploratory data analysis (EDA) using NYC Taxi Trip Duration dataset from Kaggle. The analysis uncovers patterns in urban transportation behavior, identifies peak demand periods, and provides actionable business insights for taxi operations optimization.*

**🔗 Access the Analysis:**
- **Local Jupyter Notebook:** `notebooks/01_eda_nyc_taxi_trip_analysis.ipynb`

**Key Objectives:**
- Understand trip duration patterns and distributions
- Identify peak demand hours and passenger behavior
- Analyze temporal patterns and weekend vs weekday differences
- Create clear visualizations for data storytelling
- Provide data-driven business recommendations

## 📈 Dataset

**Source:** [NYC Taxi Trip Duration - Kaggle Competition](https://www.kaggle.com/c/nyc-taxi-trip-duration/data)

**Size:** 1,458,644 taxi trips from NYC

**Data Quality:** High-quality dataset with no missing values and no duplicate records

**Key Features:**
- `id` - Unique identifier for each trip
- `vendor_id` - Taxi company identifier (2 vendors)
- `pickup_datetime` - Trip start timestamp
- `dropoff_datetime` - Trip end timestamp
- `passenger_count` - Number of passengers (1-9)
- `pickup_longitude/latitude` - Pickup coordinates
- `dropoff_longitude/latitude` - Dropoff coordinates
- `store_and_fwd_flag` - Data transmission flag
- `trip_duration` - Target variable (duration in seconds)

## 🚀 Installation

### Prerequisites
```bash
Python 3.8+
Google Colab (recommended) or Jupyter Notebook
```

### Local Setup
1. **Clone the repository**
```bash
git clone https://github.com/yourusername/eda-nyc-taxi-trip-duration.git
cd eda-nyc-taxi-trip-duration
```

2. **Install required packages**
```bash
pip install pandas numpy matplotlib seaborn datetime
```

3. **Download the dataset**
- Visit [Kaggle NYC Taxi Competition](https://www.kaggle.com/c/nyc-taxi-trip-duration/data)
- Download `train.csv`
- Place in the `data/` directory

### Google Colab Setup
1. Open the [Colab notebook](https://colab.research.google.com/drive/1hpgeFswENh93s6BPnjWxCtapiSKibMgI)
2. Upload the dataset to your Google Drive
3. Update the file path in the notebook
4. Run all cells

## 🔍 My Analysis Journey

I approached this project with a researcher-like mindset who curiously explores everything from the dataset, breaking down the analysis into 6 systematic steps. Here's how I tackled each phase:

### **STEP 1: WHAT'S IN OUR DATA?**
![Step 1: WHAT'S IN OUR DATA?](output/images/02-Step-1.png)

**My first question:** *What am I actually working with here?*
I started by getting familiar with the dataset - like opening a new book, I needed to see what was inside before diving in. I examined the 1,458,644 taxi trips and 11 different features to understand the scope of data I was analyzing.

**What I discovered:** A massive dataset with pickup times, locations, passenger counts, and trip durations - everything needed to understand NYC taxi patterns.

### **STEP 2: IS OUR DATA CLEAN?**
![STEP 2: IS OUR DATA CLEAN?](output/images/03-Step-2.png)

**My concern:** *Can I trust this data to give me accurate insights?*
I've learned that bad data leads to wrong conclusions - it's like trying to cook with spoiled ingredients! So I carefully checked for missing values, duplicates, and unusual patterns that might throw off my analysis.

**What I found:** The data was remarkably clean with no missing values or duplicates, giving me confidence in my upcoming analysis.

### **STEP 3: WHEN DO PEOPLE TAKE TAXIS?**
![STEP 3: WHEN DO PEOPLE TAKE TAXIS?](output/images/04-Step-3.png)

**My curiosity:** *Are there specific times when New Yorkers really need taxis?*

I extracted time features from the pickup timestamps to understand daily and weekly patterns. This felt like detective work - looking for clues about when demand peaks and valleys occur.

**What I uncovered:** 6:00 PM is the absolute peak with 90,600 trips, and I discovered that 38.7% of all trips happen during traditional rush hours.

### **STEP 4: HOW LONG ARE TAXI TRIPS?**
![STEP 4: HOW LONG ARE TAXI TRIPS?](output/images/05-Step-4.png)

**My focus:** *Since trip duration is what we'd want to predict, what does this data tell us?*

I dove deep into trip duration statistics, hunting for outliers and understanding the typical NYC taxi ride. This analysis felt crucial since duration is often what passengers care about most.

**What I learned:** From the analysis, I learned that most trips are surprisingly short. The average is 16.0 minutes with a median of 11.0 minutes, showing that taxis serve as quick neighborhood connectors rather than long-distance transport.

### **STEP 5: WHO RIDES IN TAXIS?**
![WHO RIDES IN TAXIS?](output/images/06-Step-5.png)

**My hypothesis:** *I suspected most taxi rides were solo travelers, but let me verify this with data.*

I analyzed passenger counts to understand travel group behavior. This personal insight came from my own observations of taxi usage in busy cities.

**What confirmed my suspicion:** This confirms my suspicion that 70.9% of trips involve just one passenger, with only 14.4% having two passengers. This revealed a huge opportunity for fleet optimization.

### **STEP 6: SIMPLE VISUALIZATIONS**
![STEP 6: SIMPLE VISUALIZATIONS](output/images/07-Step-6.png)

**My belief:** *Numbers tell stories, but charts make them memorable.*

I created four key visualizations because I firmly believe that pictures reveal patterns our eyes can't catch in raw numbers. Each chart was designed to answer a specific business question.

**What I accomplished:** Visual charts that makes complex patterns more intuitively understandable.

## 📊 What I Discovered & My Key Insights

### 🔑 My Most Surprising Findings

**The "11-Minute City" Reality:**
When I first calculated the average trip duration of 16.0 minutes, I thought that seemed reasonable. But then the median hit me - just 11.0 minutes! This told me that NYC taxis aren't about long journeys across the city like I initially imagined. Instead, they're solving the "last mile" problem - getting people those crucial few blocks when walking feels too far or time is tight.

**The 6 PM Rush Hour Phenomenon:**
I was expecting rush hour patterns, but seeing 90,600 trips concentrated in a single hour (6 PM) genuinely surprised me. That's more than 1,500 taxi trips starting every minute! This made me realize that taxi demand isn't just about commuting - it's about the evening social economy, dinner plans, and after-work activities that define NYC life.

**The Solo Traveler Dominance:**
Going into this analysis, I had a hypothesis that most rides would be solo, but seeing 70.9% (over 1 million trips!) confirmed was still striking. What really fascinated me was that only 14.4% involved pairs - this suggests that even couples or friends often take separate taxis, prioritizing convenience over cost-sharing.

**The Weekend Paradox:**
Here's what caught me off guard: weekend trips are actually *shorter* on average (15.4 vs 16.2 minutes). I expected weekend leisure trips to be longer, but the data suggests weekends might involve more neighborhood-based activities, while weekdays include longer commutes to work districts.

### 💡 What This Means for Business (from my perspective)

**The 5.7x Opportunity:**
The most eye-opening business insight was the dramatic demand variation - 5.7 times more trips at peak versus off-peak hours. As someone interested in operations optimization, I see this as both a challenge and a massive opportunity. The companies that can dynamically adjust their supply to match this demand curve will dominate.

**The Fleet Efficiency Revelation:**
Discovering that 85%+ of taxi capacity goes unused (since most trips are solo) completely changed how I think about urban transportation. We're essentially running a network of mostly-empty cars around the city. This insight makes me believe that right-sizing the fleet could revolutionize both costs and environmental impact.

**The Underserved Hours:**
What struck me most was how different early morning looks compared to evening rush. While 6 PM sees 90,600 trips, 5 AM barely hits 16,000. This represents a blue ocean opportunity - less competition, dedicated customer base, and potential for premium pricing for reliability during those quiet hours.

### 📈 The Numbers That Changed My Thinking

**98.2% Data Quality Success:**
Finding that 98.2% of trips fell within reasonable durations (1 min - 1 hour) gave me confidence that my insights were built on solid ground. The 12,317 trips over an hour and the 979.5-hour outlier became interesting data stories rather than analysis-breaking problems.

**The 38.7% Rush Hour Economy:**
Realizing that more than one-third of all taxi trips happen during traditional rush hours helped me understand that NYC's taxi system is fundamentally built around the rhythm of the working day. This isn't just transportation - it's economic infrastructure.

### 🎯 My Visual Storytelling Success

Creating the four-chart dashboard was where everything clicked for me. Seeing the trip duration histogram's sharp peak at 5-10 minutes made the "neighborhood transportation" story immediately clear. The hourly demand line chart's dramatic evening spike told a story that no amount of statistics could capture as powerfully.

What I'm most proud of is how the passenger count bar chart visually screams "single passenger dominance" - sometimes the most important insights are the ones that jump off the page and change how you think about an entire industry.

### 🚀 What I'd Investigate Next

This analysis opened up so many questions for me: 
- How do weather patterns affect these demand cycles? 
- Are there geographic clusters where longer trips are more common? 
- What seasonal variations exist in this data?
- Could the extreme outliers (like that 979.5-hour trip) reveal interesting edge cases in urban transportation?

The beauty of exploratory data analysis is that every answer leads to new questions - and this dataset has given me plenty to think about.

## 📁 Project Structure

```
eda-nyc-taxi-trip-duration/
│
├── data/
│   └── train.csv                     # Raw dataset from Kaggle
│
├── notebooks/
│   └── 01_eda_nyc_taxi_trip_analysis.ipynb    # Main analysis notebook
│
├── python/
│   └── 01_eda_nyc_taxi_trip_analysis.py       # Python script version
│
├── output/
│   └── images/                       # Generated visualizations
│
├── .gitignore                        # Git ignore file
└── README.md                         # This file
```

## 📧 Contact

**Charlize Amorato** - charlizeamorato.works@gmail.com

**Phone Number** - +63 976 301 9316 

**Portfolio:** [Data Analyst Portfolio](https://github.com/izmecharr/data-analyst-portfolio)

**Project Link:** [NYC Taxi EDA Analysis](https://github.com/izmecharr/eda-nyc-taxi-trip-duration)

## 🙏 Acknowledgments

- [Kaggle NYC Taxi Trip Duration Competition](https://www.kaggle.com/c/nyc-taxi-trip-duration) for providing the comprehensive dataset
- NYC Taxi and Limousine Commission for the original data collection
- Google Colab for providing free computational resources
- Open source community for the amazing data science libraries (pandas, matplotlib, seaborn)
