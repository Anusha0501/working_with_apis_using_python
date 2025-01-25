# Fetching Data From an API

This project demonstrates how to fetch data from The Movie Database (TMDb) API using Python. The script retrieves the top-rated movies data from the API, processes it, and stores the data in a CSV file for further analysis. Below is an overview of the steps implemented in the script:

## Steps

1. **Import Required Libraries**:

   - `pandas` for data manipulation and analysis.
   - `requests` for making HTTP requests to the API.

2. **API Request**:

   - The TMDb API endpoint for top-rated movies is queried using an API key.
   - Pagination is handled to fetch data across multiple pages (up to 428 pages).

3. **Data Extraction and Processing**:

   - The script extracts specific fields: `id`, `title`, `overview`, `release_date`, `popularity`, `vote_average`, and `vote_count`.
   - The data from all pages is combined into a single `DataFrame` for analysis.

4. **Error Handling**:

   - The script checks the HTTP response status code to ensure successful requests.
   - In case of a failed request, an error message is logged with the corresponding page number.

5. **Data Storage**:

   - The combined data is saved as a CSV file named `movies.csv` for future use.

6. **Output**:

   - The script prints the first few rows of the `DataFrame` and its shape to confirm the data is loaded correctly.

## Files

- **`movies.csv`**: Contains the extracted data of top-rated movies.
- **Script**: The Python script used for fetching and processing the data.

## Usage

To run the script, ensure you have:

- Python installed.
- The required libraries (`pandas` and `requests`) installed.
- A valid API key for TMDb.

Run the script in your Python environment to fetch the data and save it as a CSV file.

## Notes

- Modify the API key in the script to use your own TMDb API key.
- The script is designed to handle large data and combines data efficiently using `pd.concat`.

## Additional Suggestion

Consider using [RapidAPI](https://rapidapi.com/collection/list-of-free-apis), a platform providing free public APIs for developers. It offers a wide variety of APIs, making it a versatile option for expanding your projects.

This project serves as a foundation for working with APIs, handling pagination, and storing API responses in a structured format.

