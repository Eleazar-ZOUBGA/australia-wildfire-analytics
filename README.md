# Australia Wildfire Dashboard

An interactive web application developed with **Dash** and **Plotly** to analyze and visualize historical wildfire data in Australia from 2005 onwards.

---

## Project Overview

This interactive dashboard allows users to explore wildfire activity across Australia. Users can dynamically filter the data by **administrative region** and **year** to analyze two key metrics: the average estimated wildfire area and the average number of detected wildfire pixels.

## Application Features

* **Radio Button Selection:** Choose an Australian region (e.g., Victoria, New South Wales, Queensland, etc.).
* **Dropdown Menu:** Filter the data by a specific year available in the dataset.
* **Real-Time Updates (Callbacks):**
  * **Pie Chart:** Displays the monthly distribution of the average estimated wildfire area (`Estimated_fire_area`).
  * **Bar Chart:** Shows the monthly trend of the average number of detected wildfire pixels (`Count`).

---

## Setup and Installation

### Prerequisites

The application requires **Python 3.8+** and the following libraries:

* `pandas`
* `dash`
* `plotly`

### Installation

1. Clone this repository to your local machine:

```bash
git clone https://github.com/Eleazar-ZOUBGA/australia-wildfire-analytics.git
cd australia-wildfire-analytics
```

2. Install the required dependencies using `pip`:

```bash
pip install pandas dash plotly
```

---

## Running the Application

To start the Dash development server, simply run the main Python script:

```bash
python3.8 Dash_wildfire.py
```

Once the application is running, open your web browser and navigate to:

http://127.0.0.1:8050/

---

## Data Source

The dataset is based on historical wildfire observations from **NASA FIRMS (MCD14DL)** and is hosted on the **IBM Skills Network Cloud Object Storage**.

The dataset also includes the following preprocessing steps:

* Australian regions converted into abbreviated state codes (`NSW`, `NT`, `QLD`, `SA`, `TAS`, `VIC`, `WA`).
* Time-based transformations to extract the **Year** and the full **Month** name, making the visualizations easier to interpret.