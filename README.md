# Extracting-and-Visualizing-Stock-Data
The focus of this project is to utilize Python to extract, clean, and visualize real-world stock data. It examines how to work with financial data computationally, prepares it for analysis, and clearly displays it using interactive graphs as part of a data analysis and visualization exercise.

# Objectives 
The goal of this project was to:
- Extract historical stock price data for Tesla and GameStop using the yfinance API.  
- Extract revenue data for both companies using web scraping with BeautifulSoup.  
- Clean and prepare both datasets for visualization.  
- Display the data using an interactive dashboard built with Plotly.

# Libraries used
- yfinance - To extract historical stock price data
- pandas - For data manipulation and cleaning
- requests - To fetch HTML content for web scraping
- BeautifulSoup (bs4) - To parse HTML and extract revenue data
- plotly - To create interactive data visualizations
- warnings - To suppress unnecessary warnings

# Project steps
- step 1: Extracting Tesla Stock Data
  - Made a Ticker object for Tesla (TSLA) using the yfinance library.
  - Utilizing the history(period="max") function, the entire historical stock data was retrieved.
  - To verify the data structure, reset the DataFrame's index and show the first few rows.
- step 2: Extracting Tesla Revenue Data
  - The HTML page with Tesla's quarterly revenue statistics was downloaded using the requests library.
  - Using BeautifulSoup, the HTML was parsed.
  - After extracting the suitable table, a pandas DataFrame with the columns date and revenue was built and named tesla_revenue.
  - Removed commas and dollar signs from the Revenue column.
- step 3: Extracting GameStop Stock Data
  - Used the same process as Tesla to create a Ticker object for GameStop (GME) and extract historical data.
  - Reset the index and used the head() function to verify the data.
- step 4: Extracting GameStop Revenue Data
  - The HTML data from the given GameStop revenue page was downloaded and parsed.
  - To retrieve the correct table, BeautifulSoup and pandas were used.
  - As with Tesla, the revenue data was cleaned.
- step 5: Visualizing the Data
  - Developed a reusable function called make_graph() that generates a two-layer interactive Plotly chart by taking revenue, stock, and company name data.
  - Historical share prices and revenue are shown in the top and bottom graphs, respectively.
  - This function make_graph() was used to plot the data for GameStop and Tesla.
 
# Graph screenshots
// The interactive HTML-based visualizations produced by Plotly were used to construct the graphs for this project. For security reasons, GitHub's Markdown viewer permit rendering interactive HTML or JavaScript content. On GitHub's project page, plotly graphs which are stored as.html files cannot be seen directly. I took screenshots of the Plotly graphs and included them in this README file so that others may view the project's visual output without having to execute the code themselves.

-Tesla Stock Graph
<img width="963" height="577" alt="question 5 scr2" src="https://github.com/user-attachments/assets/d8534c79-5372-4819-ae92-a03bb5284cb8" />
<img width="1000" height="592" alt="question 5 scr3" src="https://github.com/user-attachments/assets/999a1829-adcb-4661-9084-6fbf0125d0d2" />
<img width="979" height="608" alt="question 5 scr4" src="https://github.com/user-attachments/assets/9914a049-df97-4136-911b-51639c77b5d2" />
<img width="947" height="538" alt="question 5 scr5" src="https://github.com/user-attachments/assets/d1c3a152-bc6f-4889-8467-bfc6515450af" />


- GameStop Stock Graph screenshots
<img width="966" height="564" alt="question 6 scr2" src="https://github.com/user-attachments/assets/2ab5eb56-3563-4fde-8a91-872fdd11a614" />
<img width="968" height="571" alt="question 6 scr3" src="https://github.com/user-attachments/assets/7c4d53b8-0d91-49bc-8d44-bff86602614c" />
<img width="971" height="556" alt="question 6 scr4" src="https://github.com/user-attachments/assets/cbd6f6d9-3bb3-4c41-ae24-ceccc4aa0abf" />
<img width="957" height="498" alt="question 6 scr5" src="https://github.com/user-attachments/assets/2951341e-44bf-4fe2-a67c-8d9fef6b4314" />


# Results and insights
- Tesla shows consistent growth in both stock price and revenue up to mid-2021, reflecting the company’s strong market performance and expansion.
- Social media and retail investor activity are the main causes of GameStop's stock price volatility, especially in the early months of 2021.
- Both visualizations effectively demonstrate how data-driven insights can be extracted, cleaned, and visualized using Python tools.

# acknowledgements
This project was completed as part of the IBM Data Analyst Professional Certificate program on Coursera. It is inspired by a lab that demonstrates real-world applications of Python in financial data analysis.
