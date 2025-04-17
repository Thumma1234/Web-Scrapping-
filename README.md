# Web-Scrapping-
🧠 Project Overview
This project is a **data scraping and analysis tool** built in Python to gather used car listings from the **Cars24 website** for a specific city (in this case, **Hyderabad**) and analyze the extracted data through various visualizations. It provides insights into car models, specifications, and locations.

🔧 Workflow Breakdown
1. **Web Scraping**
- **Tool Used**: `requests`, `BeautifulSoup`
- **Target URL**: Cars24 used cars in Hyderabad.
- The script sends a **GET request** to the URL.
- Parses the HTML content using `BeautifulSoup`.
- Locates a specific container with class `styles_carListingContainer__uob_6` that holds car listings.
- Extracts the textual data from the HTML structure.

2. **Data Extraction & Cleaning**
- The raw string is processed to:
  - Split text into meaningful blocks (each representing a car).
  - Extract relevant fields: **Car Model**, **Car Specifications**, and **Location**.
- Handles missing or incomplete data manually with list filtering and cleanup.
- Builds separate Python lists: `car_models`, `prices`, `locations`.

3. **Data Structuring with Pandas**
- Uses `pandas` to structure the data into a `DataFrame` with three columns:
  - `Car_models`
  - `Car Specifications`
  - `Locations`
- Additional cleaning:
  - Only last word from location (e.g., “Hyderabad”) is retained.
  - Car models are formatted to remove unwanted prefixes.

4. **CSV Export**
- Saves the cleaned data into a CSV file: `cars2025.csv`.
- Uses Google Colab's `files.download()` to allow downloading.

📊 Visualizations
I included **three types of visualizations** to demonstrate data analysis:
1. **Pie Chart**
- Labels: Dummy car data (`Car1`, `Car2`, …)
- Values: Random sizes (not from scraped data)
- Purpose: Show how you can visualize proportion/distribution of categories.

2. **Bar Chart**
- Labels: Dummy cars (`c1` to `c5`)
- Values: Dummy EMI values
- Purpose: Illustrate how to compare values like loan EMI across cars.

3. **Line Chart**
- X-axis: Car models
- Y-axis: Locations (text-based, so not numerically meaningful)
- Line plot isn’t meaningful here because both axes are categorical — could be enhanced by adding numerical features like EMI or price.

💡 Key Learnings
This project demonstrates:
- Practical web scraping skills for dynamic sites.
- Data cleaning and transformation.
- DataFrame manipulation using `pandas`.
- Basic data visualization with `matplotlib`.
- Exporting structured data for reuse.

⚙️ Potential Improvements
Here are some ideas to make the project more robust and professional:
🔄 1. **Dynamic Scraping with Pagination**
- Scrape multiple pages instead of just the first.
- Use tools like Selenium for dynamic JavaScript-rendered content.

📉 2. **Real Data Visualizations**
- Extract price or EMI directly from the site.
- Plot real prices, car counts by model, location distribution, etc.

🧪 3. **Data Validation**
- Filter out incomplete records automatically.
- Use regex to validate price/EMI formats.

🖼️ 4. **Add Images**
- Scrape image URLs for each car listing.
- Display them using `IPython.display.Image` in Colab or save them locally.

🧰 5. **Turn into a Web App**
- Use Flask or Streamlit to let users enter city/filters and get live scraped data with charts.


✅ Final Thoughts
This project is a solid demonstration of:
- Web scraping & parsing skills.
- Real-world data handling and cleansing.
- Foundational data visualization.
- Preparing a dataset for analysis or machine learning.

