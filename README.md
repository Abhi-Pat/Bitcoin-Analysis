## Bitcoin Price Analysis and Visualization

This repository contains an analysis of Bitcoin price data spanning from April 28, 2013, to July 31, 2017. The project focuses on data preprocessing, stock price analysis, and visualizing Bitcoin's market trends using a variety of data visualization techniques.

### Key Steps:

1. **Imported the necessary packages:**
   - **pandas**: For data pre-processing, handling CSV files, and data manipulation.
   - **numpy**: Used for numerical computations.
   - **matplotlib.pyplot**: For static data visualization.
   - **seaborn**: For enhanced visualizations.
   - **plotly** (via `plotly.graph_objs` and `plotly.express`): For creating interactive visualizations.
   - **cufflinks**: For more interactive plotting and linking `pandas` with Plotly.

2. **Data Pre-processing:**
   - Checked and corrected the data types for each column.
   - Handled missing values in the dataset to ensure clean analysis.
   - Identified and removed duplicate entries.
   - Sorted the data in ascending order, which spans from **April 28, 2013** to **July 31, 2017**.

3. **Analyzing Changes in Bitcoin Price Over Time:**
   - Visualized Bitcoin's 'Open', 'High', 'Low', and 'Close' prices across time using 4 subplots with **matplotlib**.
   
4. **Candlestick Visualization of Bitcoin Prices:**
   - Converted the dataset into **candlestick plots** to visualize the price movements in the market.
   - Plotted the full dataset as well as a subset of the first 50 entries for a clear, interactive visualization.

    Example:
    ```python
    trace = go.Candlestick(
        x=bitcoin_sample['Date'],
        high=bitcoin_sample['High'],
        open=bitcoin_sample['Open'],
        close=bitcoin_sample['Close'],
        low=bitcoin_sample['Low']
    )
    candle_data = [trace]
    fig = go.Figure(data=candle_data, layout=layout)
    ```

5. **Analyzing Bitcoin's Closing Prices:**
   - Plotted the closing price of Bitcoin on both **normal scale** and **log-scale** for comparative analysis.
   - Used **numpy** to convert the closing price to a log scale for improved visual analysis.

6. **Resampling Bitcoin Prices:**
   - Analyzed Bitcoin's price on a **yearly**, **quarterly**, and **monthly** basis by calculating the average price over each period.
   - Resampled the data to calculate the mean closing prices for each time frame and plotted the results as line graphs.

7. **Daily Change in Bitcoin's Closing Price:**
   - Created a new column to calculate the **percentage change** in Bitcoin’s daily closing price.
   - Plotted the daily percentage change for better insights into daily market fluctuations.
   - Used **cufflinks** to make the plot interactive and more insightful by including a descriptive X-axis for the daily changes.

---

### Tools & Libraries Used:
- **pandas**: Data manipulation and handling CSV files.
- **numpy**: Numerical operations.
- **matplotlib** & **seaborn**: Visualization of static plots and charts.
- **plotly**: Interactive data visualization (for candlestick plots, line graphs, and more).
- **cufflinks**: Enhances `pandas` plots with interactive features.

This repository demonstrates various data visualization techniques, focusing on interactive plots and trend analysis of Bitcoin prices. By leveraging **Plotly** and **cufflinks**, this analysis provides rich visual insights into Bitcoin's historical price changes, offering the ability to interact with data and visualize trends over time.

Feel free to explore the interactive visualizations and data insights within the repository!

---

### How to Run:
1. Clone the repository.
2. Install the necessary libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `plotly`, and `cufflinks`.
3. Run the Jupyter notebook files to view the interactive plots and analysis.

---

### Future Enhancements:
- Extend the analysis to include other cryptocurrencies.
- Add more time-series forecasting models to predict future Bitcoin prices.
