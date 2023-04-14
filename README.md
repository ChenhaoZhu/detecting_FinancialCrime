# IMI BigDataAIHUB Case Competition

## Motivation
Financial Institutions are used by criminals to “legitimize” money generated from criminal activities, hence banks are expected by society and regulators to act proactively in detecting and stopping criminals from using the financial system to access their money through effective monitoring and reporting to authorities.

## Complication
- Number of clients and transaction volume are large and only expected to grow in the future
- Diminishing returns of adding more headcount
- Criminals are constantly innovating on ways to use financial system to “legitimize” their funds

## Case Goal
Use suitable data analytics tools and techniques to help Scotiabank detect financial crimes:
- Find known high risk people in our customer base using public data
- Score clients according to their likelihood of being involved in Money Laundering using transactional data
- Enhance scoring and visualize networks using connections between clients

## Case Tasks
1. Name Screening: Detect 50 Bad Actors in Scotiabank's customer base using public data sources.
2. Risking Rating: Classify customers into Low, Medium and High risk, and predict Bad Actors.
3. Improve Model using Graph Data: Add customer connections information to improve risk rating model or use a graph model directly.

## Data Sources
**Raw Data**
- `UofT_nodes.csv`: contains KYC, Transactional data and Risk Rating
- `UofT_edges.csv`: contains connections between customers i.e. amount of money sent via EMT from one customer (source) to another (target)
- `UofT_occupation_risk.csv`: contains mapping between an occupation (code) to their risk level of being involves in financial crimes
- `targets.simple.csv`: contains a list of Bad Actors from https://www.opensanctions.org/datasets/default/

**Intermediate Data**
- `matches_fuzzy.csv`: generated from `case.ipynb`, contains potential Customer-Bad Actor matches, based on names and birth dates, with FuzzyWuzzy method.
- `badactor_foundin_kyc_bt_match.csv`: generated from task 1, a subset of `UofT_nodes.csv` containing ONLY the Bad Actors.
