# 📰 Biased News Identification in Malayalam Media

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)

Automated bias detection system for Malayalam news platforms using NLP and web scraping techniques.

## 🎯 Project Overview

This project identifies coverage and demographic bias in Malayalam digital news media through automated data collection and analysis.

**Target Sources:**
- Malayala Manorama
- Kerala Kaumudi  
- Mathrubhumi

## 🛠️ Technical Stack

### Data Collection
- **BeautifulSoup4** - HTML parsing
- **Scrapy** - Web crawling framework
- **Selenium** - Dynamic content handling

### NLP Pipeline
- **IndicTrans2** - Malayalam-English translation
- **BERT** - Named Entity Recognition
- **Transformers** - Zero-shot classification

### Analysis
- **Pandas** - Data manipulation
- **NumPy** - Numerical computing
- **Matplotlib/Seaborn** - Visualization

## 📊 Methodology

### Data Collection
- Scraped 225+ articles from Malayalam news platforms
- Sources: RSS feeds, sitemaps, direct HTML parsing
- Data format: CSV with date, title, summary, source, URL

### Bias Detection
- **Geographic Analysis:** Entropy-based location diversity scoring
- **Demographic Analysis:** Gender and urban-rural representation ratios
- **Named Entity Recognition:** Person, location, organization extraction
- **Zero-shot Classification:** Automated content categorization

## 📈 Key Findings

- **Urban Concentration:** 62% coverage focused on major cities vs <5% for rural districts
- **Geographic Distribution:** Significant disparity in regional coverage
- **Content Categories:** Politics, crime, and entertainment dominate coverage

## 🔧 Installation

```bash
# Clone repository
git clone https://github.com/username/malayalam-news-bias-detection.git
cd malayalam-news-bias-detection

# Install dependencies
pip install -r requirements.txt
```

## 💻 Usage

```python
# Basic scraping
from scrapers import MalayalamNewsScraper
scraper = MalayalamNewsScraper()
articles = scraper.scrape_all_sources(days=7)

# Bias analysis
from analysis import BiasAnalyzer
analyzer = BiasAnalyzer(articles)
geo_bias = analyzer.calculate_geographic_bias()
```

## ⚠️ Limitations

- Translation quality affects NLP accuracy
- Cultural context loss in Malayalam→English conversion
- NER model limitations on translated text

## 📈 Key Findings

- ~62% of news focused on Trivandrum, Kochi, and Kozhikode
- Underreporting in Idukki, Kasaragod, and other rural areas
- Limited coverage of development and agriculture topics

## 🚀 Future Scope

- Implement emotion tagging and fine-grained sentiment classification
- Build interactive dashboards for bias and sentiment visualization
- Develop multilingual idiom corpora for improved NLP accuracy
- Collaborate with fact-checking networks for real-time alerts

## 🧾 Citation

If you use this research, please cite appropriately or mention this repository in your work.

## 📬 Contact

For questions or collaboration inquiries, feel free to open an issue or contact the author.
