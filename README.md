# Bitcoin Trading Behavior vs Market Sentiment Analysis

## 🎯 Project Overview

This project analyzes the relationship between cryptocurrency trader behavior and market sentiment using historical trading data from Hyperliquid and the Bitcoin Fear & Greed Index. The goal is to identify patterns that could lead to more informed trading strategies.

## Project Important Links

## Google Colab Links
notebook 1 : https://colab.research.google.com/drive/1T5CckY5FtuZyV9dA1qN5PgSEKczEWAcM?usp=sharing
notebook 2 : https://colab.research.google.com/drive/1iyvBNV1r9BD1O_Dl2VfU3RYb7ZK-LQ0y?usp=sharing

fear_greed_index.csv file : https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_mnrYv_nhSf/view?usp=sharing
historical Trader data: https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjV

## Final processed dataset : https://drive.google.com/file/d/1J9sp8_rFGbae1QPLrP9Nnc4vvOPyQ-KH/view?usp=sharing

## 📁 Project Structure

```
ds_bitcoin_sentiment_analysis/
├── notebook_1_data_exploration.ipynb     # Data loading, cleaning, and initial EDA
├── notebook_2_sentiment_analysis.ipynb   # Advanced analysis and pattern identification
├── csv_files/
│   ├── fear_greed_index.csv.csv            # Fear & Greed Index data
│   ├── historical_data.csv                 # Historical Hyperliquid trader data
│   └── processed_data.csv               # Merged and processed dataset
├── outputs/
│   ├── sentiment_distribution.png        # Market sentiment over time
│   ├── trading_volume_analysis.png       # Volume patterns by sentiment
│   ├── pnl_sentiment_correlation.png     # Profitability vs sentiment
│   ├── leverage_risk_analysis.png        # Risk patterns analysis
│   ├── temporal_patterns.png             # Time-based trading patterns
│   ├── contrarian_momentum_analysis.png  # Strategy type analysis
│   ├── trader_clustering_analysis.png    # Trader behavior clusters
│   ├── trading_strategy_insights.png     # Final insights visualization
│   └── final_analysis_results.csv        # Summary statistics
├── ds_report.pdf                         # Final analysis report
└── README.md                            # This file
```

## 📊 Datasets

### 1. Bitcoin Market Sentiment Dataset
- **Source**: Fear & Greed Index
- **Columns**: `Date`, `Classification` (Fear/Greed)
- **Description**: Daily market sentiment classification
- **Link**: [Fear & Greed Data](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_mnrYv_nhSf/view?usp=sharing)

### 2. Historical Trader Data from Hyperliquid
- **Columns**: `account`, `symbol`, `execution price`, `size`, `side`, `time`, `start position`, `event`, `closedPnL`, `leverage`
- **Description**: Individual trader transactions and performance metrics
- **Link**: [Trader Data](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing)

## 🚀 Quick Start

### Prerequisites
- Google Colab account
- Access to the provided datasets

### Setup Instructions

1. **Open Google Colab**
   - Go to [Google Colab](https://colab.research.google.com/)
   - Sign in with your Google account

2. **Upload Datasets**
   - Download the datasets from the provided links
   - Upload them to your Google Drive
   - Note the file paths for the notebooks

3. **Run Notebooks in Sequence**
   - Upload `notebook_1_data_exploration.ipynb` to Colab
   - Update dataset paths in the notebook
   - Run all cells
   - Upload `notebook_2_sentiment_analysis.ipynb` to Colab
   - Run all cells

4. **Download Results**
   - Download all outputs from `/content/outputs/`
   - Organize them according to the project structure

## 🔍 Analysis Overview

### Phase 1: Data Exploration (Notebook 1)

**Objectives:**
- Load and inspect both datasets
- Perform initial exploratory data analysis
- Clean and preprocess data
- Merge datasets on date alignment
- Generate initial insights

**Key Outputs:**
- `sentiment_distribution.png` - Market sentiment trends over time
- `trading_volume_analysis.png` - Trading patterns and volume analysis
- `processed_data.csv` - Clean, merged dataset for advanced analysis

### Phase 2: Advanced Analysis (Notebook 2)

**Objectives:**
- Correlation analysis between sentiment and trading behavior
- Risk and profitability analysis by market sentiment
- Temporal pattern identification
- Contrarian vs momentum strategy analysis
- Trader clustering and behavior segmentation

**Key Outputs:**
- `pnl_sentiment_correlation.png` - Profitability patterns by sentiment
- `leverage_risk_analysis.png` - Risk management patterns
- `temporal_patterns.png` - Time-based trading behaviors
- `contrarian_momentum_analysis.png` - Strategy type identification
- `trader_clustering_analysis.png` - Trader behavior segmentation
- `trading_strategy_insights.png` - Final strategic recommendations

## 📈 Key Research Questions

1. **Performance Analysis**: Do traders perform better during "Fear" or "Greed" periods?
2. **Risk Management**: How does leverage usage correlate with market sentiment?
3. **Contrarian Opportunities**: Are there profitable contrarian signals when sentiment is extreme?
4. **Leading Indicators**: What trading patterns emerge before sentiment shifts?
5. **Position Sizing**: How do trade sizes and risk management change with sentiment?

## 🎯 Expected Key Findings

### Performance Insights
- Identification of whether traders follow momentum or contrarian strategies
- Quantification of performance differences between fear and greed periods
- Win rate analysis across different market sentiments

### Risk Patterns
- Leverage usage patterns during different sentiment periods
- Risk-adjusted return analysis
- Maximum drawdown comparisons

### Trading Behavior
- Volume and frequency patterns by sentiment
- Temporal trading patterns (hourly, daily, weekly)
- Trader clustering and behavior segmentation

## 📊 Methodology

### Data Processing
1. **Data Cleaning**: Handle missing values, outliers, and data type conversions
2. **Feature Engineering**: Create time-based features, risk metrics, and performance indicators
3. **Data Merging**: Align datasets by date for comprehensive analysis

### Statistical Analysis
1. **Correlation Analysis**: Pearson correlation between sentiment and trading metrics
2. **Hypothesis Testing**: T-tests for performance differences between sentiment periods
3. **Clustering Analysis**: K-means clustering for trader behavior segmentation

### Visualization Techniques
1. **Time Series Analysis**: Trend analysis and pattern identification
2. **Distribution Analysis**: Performance and risk metric distributions
3. **Comparative Analysis**: Side-by-side sentiment period comparisons

## 🛠️ Technical Requirements

### Required Libraries
```python
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
plotly>=5.0.0
scikit-learn>=1.0.0
scipy>=1.7.0
```

### Google Colab Setup
```python
# Install additional packages if needed
!pip install plotly
!pip install scikit-learn

# Mount Google Drive
from google.colab import drive
drive.mount('/content/drive')
```

## 📋 Quality Assurance

### Data Validation
- Missing value analysis and handling
- Outlier detection and treatment
- Data type consistency checks
- Date range validation between datasets

### Statistical Rigor
- Significance testing for all major findings
- Confidence interval calculations
- Multiple hypothesis testing corrections
- Cross-validation for clustering analysis

### Reproducibility
- Fixed random seeds for all analyses
- Detailed documentation of all preprocessing steps
- Version control for all code and data transformations

## 🎯 Success Metrics

### Quantitative Metrics
- **Statistical Significance**: P-values < 0.05 for major findings
- **Effect Size**: Cohen's d > 0.2 for meaningful differences
- **Clustering Quality**: Silhouette score > 0.3
- **Data Coverage**: >80% overlap between datasets

### Qualitative Metrics
- **Actionable Insights**: Clear, implementable trading recommendations
- **Pattern Clarity**: Easily interpretable visualizations
- **Strategy Coherence**: Consistent findings across multiple analyses

## 🚨 Limitations and Considerations

### Data Limitations
- **Time Period**: Analysis limited to available data timeframe
- **Market Conditions**: Results may not generalize to different market cycles
- **Sample Bias**: Hyperliquid traders may not represent broader crypto market

### Methodological Considerations
- **Causality**: Correlation does not imply causation
- **Survivorship Bias**: Only active traders included in analysis
- **Market Regime Changes**: Patterns may shift over time

## 🔄 Next Steps and Extensions

### Immediate Actions
1. **Backtesting**: Test identified strategies on out-of-sample data
2. **Live Monitoring**: Track real-time performance of insights
3. **Risk Management**: Implement proper position sizing and stop-losses

### Future Enhancements
1. **Machine Learning**: Develop predictive models for sentiment-based trading
2. **Multi-Asset Analysis**: Extend to other cryptocurrencies
3. **Social Sentiment**: Incorporate Twitter/Reddit sentiment data
4. **Market Microstructure**: Add order book and flow analysis

## 📞 Contact and Support

For questions about this analysis or suggestions for improvements:

- **Project Repository**: [GitHub Link - To be updated]
- **Documentation**: This README and inline code comments
- **Issues**: Use GitHub issues for bug reports and feature requests

## 📜 License and Disclaimer

### Academic Use
This analysis is intended for educational and research purposes. All findings should be independently verified before making trading decisions.

### Risk Warning
- **Trading Risk**: Cryptocurrency trading involves substantial risk of loss
- **No Financial Advice**: This analysis does not constitute financial advice
- **Past Performance**: Historical patterns may not predict future results

### Data Attribution
- Fear & Greed Index data courtesy of the original data providers
- Hyperliquid trading data used with permission for research purposes

---

## 🎉 Acknowledgments

Special thanks to:
- The crypto trading community for providing valuable datasets
- Open source Python libraries that made this analysis possible
- Google Colab for providing free computational resources
