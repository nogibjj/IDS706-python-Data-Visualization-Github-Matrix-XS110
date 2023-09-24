
# World Population


## Data

The data is from kaggle [world population](https://www.kaggle.com/datasets/iamsouravbanerjee/world-population-dataset). In this Dataset, we have Historical Population data for every Country/Territory in the world by different parameters like Area Size of the Country/Territory, Name of the Continent, Name of the Capital, Density, Population Growth Rate, Ranking based on Population, World Population Percentage, etc.

I downloaded `word_population.csv` from kaggle and uploaded it into this resporitory.

## Setup

I used week3 mini project as a template and made the following modifications: 

### 1. Update cicd.yml:
```
jobs:
  build:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        python-version: [3.7,3.8,3.9,3.10.x,3.11]
 
    steps:
      - uses: actions/checkout@v4
      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: ${{ matrix.python-version }}
```
### 2. Generate report.md

Run ` make all` in terminal, I generated `report.md` automatically.

![Alt text](/image/image6.png)

## Data Visualization

I analysed the 234 countries' population in 2022, growth rate and Area(km²).

### 1. Summary statistics using the describe method

![Alt text](/image/image1.png)

### 2. Mean, Median and Mode

![Alt text](/image/image2.png)

### 3. Variance and standard deviation

![Alt text](/image/image3.png)

### 4. histogram of 2022 population

![Alt text](/image/population_histogram.png)

### 5. boxplot of 2022 population

![Alt text](/image/population_boxplot.png)