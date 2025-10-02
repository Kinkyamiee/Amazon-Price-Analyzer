# Amazon-Price-Analyzer
This project is a Python script that analyzes the prices of products on Amazon and compares them with prices from competitors. It uses the Oxylabs API to scrape product details and the OpenAI to parse the HTML content.

## Prerequisites

Before running the script, make sure you have the following dependencies installed:

- Python 3.x
- pip
- requests
- openai api key
- oxylabs.io username and password
- pandas

You will also need an Oxylabs API key to access the Oxylabs API. You can sign up for a free trial at https://www.oxylabs.io/.

## Getting Started

1. Clone the repository:

   ```
   git clone https://github.com/your-username/amazon-price-analysis.git
   ```

2. Install the dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Create a file named `config.py` in the root directory and add the following code:

   ```python
   API_KEY = 'YOUR_API_KEY'
   USER_AGENT = 'YOUR_USER_AGENT'
   GEO_LOCATION = 'YOUR_GEO_LOCATION'
   ```

   Replace `'YOUR_API_KEY'`, `'YOUR_USER_AGENT'`, and `'YOUR_GEO_LOCATION'` with your actual values.

4. Run the script:

   ```
   python main.py
   ```

   This will scrape the prices of the top 10 most popular products on Amazon and compare them with prices from competitors.

## Usage

The script takes the following command-line arguments:

- `--asin`: The ASIN of the product to analyze
- `--domain`: The Amazon domain to scrape (e.g. "com", "co.uk", "de", etc.)
- `--geo`: The geo location to scrape (e.g. "US", "GB", "DE", etc.) (optional)

If you don't provide any arguments, the script will scrape the prices of the top 20 most popular products on Amazon.

## Output

The script will output a jsom file named data.json in the Tinydb database. The file will contain the following columns:

- `ASIN`: The ASIN of the product
- `Amazon Domain`: The Amazon domain where the product is sold
- `Geo Location`: The geo location where the product is sold
- `Product Title`: The title of the product
- `Competitor Price`: The price of the product from a competitor
- `Amazon Price`: The price of the product on Amazon
- `Competitor Rating`: The rating of the product from a competitor
- `Amazon Rating`: The rating of the product on Amazon
- `Competitor Stock`: The stock status of the product from a competitor
- `Amazon Stock`: The stock status of the product on Amazon

## License

This project is licensed under the MIT License. See the `LICENSE` file for more information.

## Acknowledgments

- Oxylabs API: https://www.oxylabs.io/
- OPENAI
- Pandas: https://pandas.pydata.org/

I hope this helps! Let me know if you have any questions.
