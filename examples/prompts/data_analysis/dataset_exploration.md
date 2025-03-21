# Data Exploration Prompt Examples

> **Navigation**: [Examples](../../) | `Prompts` → Data Analysis → Dataset Exploration
> 
> **Related**: [Data Exploration](../../../docs/domains/data_analysis/data_exploration.md), [Format Control](../../../docs/prompt_patterns/format_control.md)

## Quick Summary
**For beginners**: Ready-to-use prompts to help you analyze and understand datasets, with examples you can customize for your own data.

**For practitioners**: A structured collection of data analysis prompts demonstrating different analytical frameworks, from exploratory analysis to predictive modeling.

**Key takeaway**: These templates show how to effectively structure prompts for different data analysis tasks. Adapt them to your specific datasets and analytical needs.

---

# Data Analysis Framework: Structured Exploration Patterns

This document provides optimized prompt patterns for systematic data exploration, statistical analysis, and insight extraction.

## Analytical Approach Matrix
| Analysis Stage | Core Components | Implementation Elements | Output Deliverables |
|---------------|-----------------|------------------------|-------------------|
| **Initial Exploration** | Dataset characterization + variable relationships + data quality assessment | Distribution analysis + correlation identification + anomaly detection | Structure summary + quality report + exploration roadmap |
| **Statistical Analysis** | Hypothesis testing + pattern quantification + predictive modeling | Statistical tests + dimensionality reduction + regression analysis | Statistical findings + confidence metrics + model parameters |
| **Visualization Strategy** | Relationship mapping + distribution visualization + temporal analysis | Chart selection + encoding optimization + interactive elements | Visual insights + pattern highlights + decision support visuals |
| **Insight Extraction** | Finding prioritization + business relevance mapping + actionability assessment | Significance ranking + impact estimation + implementation framing | Prioritized insights + action recommendations + monitoring framework |

## Exploratory Data Analysis Pattern

```
# Comprehensive Dataset Exploration Framework

## DATASET CONTEXT
- Type: [structured/unstructured/time-series/spatial]
- Volume: [rows × columns]
- Time period: [date range]
- Source: [origin systems/collection methods]
- Purpose: [original collection purpose]

## DATASET STRUCTURE
- Field inventory:
  * [field_name] ([data_type]): [description] [key statistics]
  * [field_name] ([data_type]): [description] [key statistics]
  ...

## EXPLORATION OBJECTIVES
1. [primary_question] requiring [analysis_approach]
2. [secondary_question] examining [relationship/pattern]
3. [data_quality_concern] needing [validation_approach]

## SAMPLE DATA
```csv
[column_headers]
[sample_row_1]
[sample_row_2]
[sample_row_3]
...
```

## ANALYSIS REQUIREMENTS
- Distribution analysis for [specific_variables]
- Relationship examination between [variable_x] and [variable_y]
- Temporal patterns in [time_variable]
- Segmentation analysis by [categorical_variable]
- Quality assessment focusing on [completeness/accuracy/consistency]

## DELIVERABLE FORMAT
- Key characteristics summary
- Variable relationship analysis
- Data quality assessment
- Recommended next analyses
- Visualization suggestions with rationale
```

### Implementation Example: Customer Transaction Data

```
# Comprehensive Dataset Exploration Framework

## DATASET CONTEXT
- Type: Structured transaction data with customer attributes
- Volume: 15,000 transactions × 10 variables
- Time period: January 2022 - December 2022
- Source: E-commerce platform and CRM system integration
- Purpose: Sales analysis and customer segmentation

## DATASET STRUCTURE
- Field inventory:
  * transaction_id (string): Unique transaction identifier [100% unique]
  * customer_id (string): Customer identifier [3,500 unique values]
  * purchase_date (date): Transaction date [YYYY-MM-DD format]
  * product_id (string): Product identifier [2,200 unique values]
  * product_category (categorical): Product classification [5 categories]
  * purchase_amount (numerical): Transaction value in USD [range: $5.99-$2,499.99]
  * payment_method (categorical): Payment type [4 categories]
  * customer_age (numerical): Customer age in years [range: 18-75]
  * customer_gender (categorical): Customer gender [3 categories]
  * customer_location (categorical): State/province code [42 unique values]

## EXPLORATION OBJECTIVES
1. Identify purchase patterns across demographic segments
2. Examine seasonal variations in category performance
3. Assess customer loyalty indicators through repeat purchase behavior
4. Validate data completeness and consistency across variables

## SAMPLE DATA
```csv
transaction_id,customer_id,purchase_date,product_id,product_category,purchase_amount,payment_method,customer_age,customer_gender,customer_location
T1001,C5432,2022-01-05,P765,Electronics,499.99,Credit,34,M,CA
T1002,C8765,2022-01-06,P234,Clothing,59.95,PayPal,27,F,NY
T1003,C5432,2022-01-12,P890,Home,129.50,Credit,34,M,CA
T1004,C2341,2022-01-15,P567,Electronics,899.00,Credit,45,M,TX
T1005,C7654,2022-01-17,P123,Food,75.25,Debit,29,F,FL
```

## ANALYSIS REQUIREMENTS
- Distribution analysis for purchase_amount across product categories
- Relationship examination between customer demographics and purchase behavior
- Temporal patterns in transaction frequency and value
- Segmentation analysis by product category and payment method
- Quality assessment focusing on completeness and logical consistency

## DELIVERABLE FORMAT
- Key characteristics summary with primary statistical measures
- Variable relationship analysis with correlation strengths
- Data quality assessment with issue prioritization
- Recommended next analyses with specific techniques
- Visualization suggestions with implementation approach
```

## Statistical Analysis Framework

### Analysis Specification Pattern

```
# Statistical Analysis Specification

## ANALYSIS CONTEXT
- Dataset: [dataset_name/description]
- Domain: [business_domain]
- Analysis purpose: [decision_support/pattern_identification/prediction]

## STATISTICAL QUESTIONS
1. [question_1]: Requires [test_type/approach]
2. [question_2]: Requires [test_type/approach]
3. [question_3]: Requires [test_type/approach]

## DATA CHARACTERISTICS
- Sample size: [n_value]
- Variables of interest:
  * [variable_1] ([type]): [distribution/characteristics]
  * [variable_2] ([type]): [distribution/characteristics]
  * [relationship_notes]

## METHODOLOGICAL REQUIREMENTS
- Confidence level: [statistical_threshold]
- Required tests: [specific_statistical_tests]
- Model validation approach: [validation_method]
- Effect size consideration: [minimum_detectable_effect]

## ANALYTICAL CONSTRAINTS
- Data limitations: [missing_data/sampling_issues/measurement_concerns]
- Assumptions to validate: [normality/independence/homogeneity]
- Alternative approaches if assumptions violated: [robust_methods]

## INTERPRETATION FRAMEWORK
- Business impact thresholds: [significance_levels_in_business_terms]
- Comparative benchmarks: [industry_standards/historical_performance]
- Implementation guidance requirements: [decision_criteria]
```

### Statistical Test Selection Matrix
| Question Type | Test Options | Assumptions | Business Applications |
|--------------|-------------|------------|---------------------|
| **Group Differences** | t-test/ANOVA/Mann-Whitney/Kruskal-Wallis | Sample distribution + group independence + variance characteristics | Customer segment performance + campaign effectiveness + product comparison |
| **Relationships** | Correlation/regression/chi-square | Variable types + relationship linearity + independence of observations | Driver analysis + predictive modeling + factor influence |
| **Time Series** | ARIMA/exponential smoothing/spectral analysis | Stationarity + seasonality + trend components | Forecasting + seasonality detection + anomaly identification |
| **Classification** | Logistic regression/discriminant analysis/machine learning | Sample size + class balance + feature independence | Customer segmentation + churn prediction + response modeling |

### Implementation Example: Retail Sales Analysis

```
# Statistical Analysis Specification

## ANALYSIS CONTEXT
- Dataset: Multi-category retail sales (2-year monthly data)
- Domain: Retail merchandising and marketing optimization
- Analysis purpose: Category performance evaluation and promotional effectiveness

## STATISTICAL QUESTIONS
1. Category performance differences: Requires ANOVA with post-hoc tests
2. Promotional impact assessment: Requires regression analysis with controls
3. Seasonality pattern identification: Requires time series decomposition
4. Sales anomaly detection: Requires statistical process control methods
5. Future sales forecasting: Requires time series modeling with exogenous variables

## DATA CHARACTERISTICS
- Sample size: 24 months × 4 categories = 96 observations
- Variables of interest:
  * Monthly_Sales (continuous): Right-skewed, range $120K-$350K
  * Promotional_Spend (continuous): Range $10K-$50K, coincides with seasonal peaks
  * Seasonal_Index (continuous): Normalized values 0.75-1.80
  * Category (categorical): Electronics, Clothing, Home, Food
  * Sales distribution varies significantly by category (variance heterogeneity)

## METHODOLOGICAL REQUIREMENTS
- Confidence level: 95% (α = 0.05)
- Required tests:
  * One-way ANOVA with Tukey's HSD for category differences
  * Multiple linear regression with promotional elasticity calculation
  * Seasonal decomposition using STL or X-13ARIMA-SEATS
  * Time series forecasting with ARIMAX or Prophet models
- Model validation: Time-based cross-validation with rolling origin
- Effect size consideration: Detect promotional ROI differences of 15% or greater

## ANALYTICAL CONSTRAINTS
- Data limitations: Limited promotion variation, possible omitted variables
- Assumptions to validate:
  * Sales distribution normality within categories
  * Homogeneity of variance across categories
  * Independence of monthly observations (autocorrelation check)
- Alternative approaches:
  * Non-parametric Kruskal-Wallis if normality violated
  * Heteroskedasticity-robust standard errors if variance issues
  * GARCH models if volatility clustering present

## INTERPRETATION FRAMEWORK
- Business impact thresholds:
  * Promotional elasticity > 1.5 considered highly effective
  * Category performance gap > 20% requires assortment review
  * Forecast accuracy within ±10% accepted for planning
- Comparative benchmarks: Prior year performance, category growth targets
- Implementation guidance: Promotional timing optimization, category investment reallocation
```

## Visualization Strategy Framework

### Visual Communication Pattern

```
# Visualization Specification System

## ANALYTICAL CONTEXT
- Audience: [technical/executive/mixed]
- Purpose: [exploratory/explanatory/persuasive]
- Key decisions: [specific_decisions_to_support]

## DATA RELATIONSHIPS
1. [relationship_1]: [variables] showing [pattern_type]
2. [relationship_2]: [variables] showing [pattern_type]
3. [relationship_3]: [variables] showing [pattern_type]

## VISUALIZATION PORTFOLIO
1. [chart_type_1]:
   - Variables: [specific_variables]
   - Insight goal: [pattern_to_highlight]
   - Design specifications: [details_on_implementation]
   - Interpretation guidance: [how_to_read_and_use]

2. [chart_type_2]:
   - Variables: [specific_variables]
   - Insight goal: [pattern_to_highlight]
   - Design specifications: [details_on_implementation]
   - Interpretation guidance: [how_to_read_and_use]

3. [chart_type_3]:
   - Variables: [specific_variables]
   - Insight goal: [pattern_to_highlight]
   - Design specifications: [details_on_implementation]
   - Interpretation guidance: [how_to_read_and_use]

## TECHNICAL IMPLEMENTATION
- Recommended tools: [visualization_libraries/applications]
- Interactivity requirements: [specific_interactive_elements]
- Integration needs: [dashboard/reporting_system]
```

### Visualization Selection Framework
| Data Relationship | Primary Visualization | Enhancements | Pattern Highlighting |
|-------------------|----------------------|--------------|---------------------|
| **Distribution (1-var)** | Histogram/box plot/density plot | Reference lines + annotation + distribution fit | Central tendency + outliers + shape characteristics |
| **Comparison (cat vs num)** | Bar chart/dot plot/violin plot | Color encoding + sorting + reference lines | Magnitude differences + variance patterns + group ranking |
| **Relationship (num vs num)** | Scatter plot/bubble chart/hexbin | Trendlines + confidence bands + faceting | Correlation strength + clusters + influential points |
| **Composition (parts to whole)** | Stacked bar/pie chart/treemap | Hierarchical grouping + percentage labeling + highlighting | Proportional relationships + dominant categories + nested structure |
| **Temporal (time series)** | Line chart/area chart/calendar heatmap | Trend highlighting + seasonality markers + forecasting | Trends + cycles + anomalies + change points |
| **Geospatial (location data)** | Choropleth/dot density/cartogram | Region highlighting + interactive tooltip + zoom levels | Spatial clusters + regional patterns + outlier areas |
| **Multivariate (3+ variables)** | Parallel coordinates/radar chart/heatmap | Dimension reduction + interactive filtering + hierarchical clustering | Complex relationships + segmentation patterns + correlation matrices |

### Implementation Example: Customer Segmentation Visualization

```
# Visualization Specification System

## ANALYTICAL CONTEXT
- Audience: Marketing team with mixed technical background
- Purpose: Actionable customer segment understanding for campaign planning
- Key decisions: Segment targeting priorities, message differentiation, channel allocation

## DATA RELATIONSHIPS
1. Segment characteristics: Demographics and behavioral metrics across 4 segments
2. Value dimensions: Spend, frequency, and AOV relationships by segment
3. Channel preference: Segment distribution across digital and physical touchpoints
4. Temporal stability: Segment membership consistency across customer tenure

## VISUALIZATION PORTFOLIO
1. Parallel coordinates plot:
   - Variables: All key metrics (spend, frequency, AOV, tenure, age)
   - Insight goal: Multi-dimensional segment differentiation
   - Design specifications:
     * Color-code by segment with distinct palette
     * Interactive highlighting on segment selection
     * Ordered axes with most discriminating variables first
     * Normalized scales for cross-variable comparison
   - Interpretation guidance: Line patterns reveal segment characteristics; crossing lines indicate variable importance

2. Radar/spider chart set:
   - Variables: Normalized metrics for each segment
   - Insight goal: Segment profile "shapes" for quick differentiation
   - Design specifications:
     * One radar chart per segment in small multiples
     * Consistent scale across all charts
     * Area fill with 50% transparency
     * Reference markers at quartile points
   - Interpretation guidance: Shape differences highlight segment specialization areas

3. Heatmap matrix:
   - Variables: Segments × channel preference × age group
   - Insight goal: Targeting opportunities by channel and demographics
   - Design specifications:
     * Color intensity encoding for preference strength
     * Hierarchical clustering to group similar patterns
     * Row/column sorting by similarity
     * Annotation for highest-value cells
   - Interpretation guidance: Dark clusters indicate targeting priorities; patterns reveal cross-segment opportunities

4. Sankey diagram:
   - Variables: Age group → segment → channel preference → purchase category
   - Insight goal: Customer flow visualization across decision points
   - Design specifications:
     * Node width proportional to population size
     * Flow width showing transition strength
     * Consistent color scheme with other visualizations
     * Interactive filtering by node
   - Interpretation guidance: Path thickness shows dominant journeys; diversions reveal segment variations

## TECHNICAL IMPLEMENTATION
- Recommended tools: Python (Plotly, Seaborn) or Tableau
- Interactivity requirements:
  * Segment highlighting across all charts
  * Metric filtering for focused analysis
  * Tooltip details for specific data points
- Integration needs: Interactive dashboard with segment selection controls and metric filters
```

## Insight Extraction and Synthesis

### Analytical Findings Structure

```
# Insight Extraction Framework

## ANALYTICAL SUMMARY
- Primary findings: [3-5 key discoveries]
- Confidence assessment: [statistical_reliability + data_quality_factors]
- Business relevance: [connection_to_objectives + decision_impact]

## KEY INSIGHTS
1. [insight_1]:
   - Evidence: [specific_data_points + statistical_measures]
   - Business impact: [operational/strategic/financial implications]
   - Confidence level: [statistical_confidence + limitations]
   - Action recommendation: [specific_next_steps]

2. [insight_2]:
   - Evidence: [specific_data_points + statistical_measures]
   - Business impact: [operational/strategic/financial implications]
   - Confidence level: [statistical_confidence + limitations]
   - Action recommendation: [specific_next_steps]

3. [insight_3]:
   - Evidence: [specific_data_points + statistical_measures]
   - Business impact: [operational/strategic/financial implications]
   - Confidence level: [statistical_confidence + limitations]
   - Action recommendation: [specific_next_steps]

## OPPORTUNITY ASSESSMENT
| Opportunity | Impact Potential | Implementation Complexity | Data Confidence | Priority Score |
|-------------|----------------|-------------------------|----------------|--------------|
| [opportunity_1] | [H/M/L + estimate] | [H/M/L + requirements] | [H/M/L + gaps] | [score] |
| [opportunity_2] | [H/M/L + estimate] | [H/M/L + requirements] | [H/M/L + gaps] | [score] |
| [opportunity_3] | [H/M/L + estimate] | [H/M/L + requirements] | [H/M/L + gaps] | [score] |

## NEXT ANALYSIS RECOMMENDATIONS
1. [follow_up_1]: [purpose + approach + expected_outcome]
2. [follow_up_2]: [purpose + approach + expected_outcome]
3. [follow_up_3]: [purpose + approach + expected_outcome]
```

### Implementation Example: E-commerce Insight Extraction

```
# Insight Extraction Framework

## ANALYTICAL SUMMARY
- Primary findings:
  * Customer segments show 3.2x difference in lifetime value
  * Promotional elasticity varies by season and category (0.8-2.7 range)
  * Mobile app users show 47% higher purchase frequency but 12% lower AOV
  * Cross-category shoppers have 58% lower churn probability
- Confidence assessment: High reliability on behavioral metrics, moderate on attributed profitability
- Business relevance: Directly impacts Q3 campaign planning and platform investment allocation

## KEY INSIGHTS
1. Premium segment profitability paradox:
   - Evidence: Highest-spending segment (22% of customers) generates 37% of revenue but only 29% of profit due to 3.2x higher return rate and 2.5x higher service costs
   - Business impact: Net margin drag of 4.7 percentage points on overall profitability
   - Confidence level: High (95% CI ±2.1%) with consistent pattern across 18-month analysis
   - Action recommendation: Implement tiered service model with premium handling fees for highest-maintenance customers

2. Seasonal category elasticity patterns:
   - Evidence: Home category shows highest promotional elasticity (2.7) during Q1, Electronics peaks in Q4 (2.3), while Fashion maintains consistent response (1.4-1.8)
   - Business impact: $430K annual promotional efficiency opportunity through reallocation
   - Confidence level: Moderate (multiple testing effects possible, validation needed)
   - Action recommendation: Test 30% promotional budget shift from underperforming seasons to high-elasticity periods

3. Cross-category purchase loyalty effect:
   - Evidence: Customers purchasing from 3+ categories have 58% lower 90-day churn and 74% higher 12-month LTV compared to single-category shoppers
   - Business impact: Each 5% increase in multi-category shoppers yields $290K incremental annual revenue
   - Confidence level: High (consistent across all customer cohorts and entry categories)
   - Action recommendation: Implement cross-category recommendation engine and bundle incentives during first 30 days of customer lifecycle

## OPPORTUNITY ASSESSMENT
| Opportunity | Impact Potential | Implementation Complexity | Data Confidence | Priority Score |
|-------------|----------------|-------------------------|----------------|--------------|
| Cross-category incentive program | High ($1.2M annual) | Medium (recommendation engine + incentive management) | High (validated pattern) | 86/100 |
| Seasonal promotional reallocation | Medium ($430K annual) | Low (campaign calendar adjustment) | Medium (validation needed) | 78/100 |
| Premium service tier implementation | Medium ($380K annual) | High (service model restructuring + customer communication) | High (consistent pattern) | 72/100 |
| Mobile app AOV enhancement | Medium ($290K annual) | Medium (UX modifications + testing framework) | Medium (causality not established) | 65/100 |

## NEXT ANALYSIS RECOMMENDATIONS
1. Premium segment profitability driver analysis: Detailed cost allocation study to identify specific service elements driving disproportionate costs
2. Promotional elasticity validation: Controlled A/B tests of promotional timing shifts with isolated category-specific campaigns
3. Cross-category path analysis: Purchase sequence mapping to identify optimal entry category and most effective cross-category transitions
```

## Advanced Analytical Techniques

### Predictive Modeling Framework

```
# Predictive Analysis Specification

## MODEL OBJECTIVE
- Prediction target: [dependent_variable]
- Model purpose: [classification/regression/forecasting/ranking]
- Success criteria: [performance_metrics + business_thresholds]

## FEATURE ENGINEERING
- Primary predictors:
  * [variable_1]: [transformation + expected_relationship]
  * [variable_2]: [transformation + expected_relationship]
  * [variable_3]: [transformation + expected_relationship]
- Derived features:
  * [feature_1]: [calculation_method + rationale]
  * [feature_2]: [calculation_method + rationale]
- Interaction terms:
  * [interaction_1]: [variables + theoretical_basis]

## MODELING APPROACH
- Candidate algorithms:
  * [algorithm_1]: [strengths + limitations + parameters]
  * [algorithm_2]: [strengths + limitations + parameters]
  * [algorithm_3]: [strengths + limitations + parameters]
- Validation strategy: [cross-validation_approach + test_methodology]
- Hyperparameter optimization: [tuning_method + search_space]

## IMPLEMENTATION REQUIREMENTS
- Data preparation pipeline: [preprocessing_steps + transformations]
- Computational needs: [infrastructure + performance_constraints]
- Monitoring plan: [drift_detection + refresh_frequency]

## EVALUATION FRAMEWORK
- Technical metrics: [specific_measures + acceptable_thresholds]
- Business impact estimation: [value_calculation + ROI_methodology]
- Interpretability requirements: [explanation_needs + transparency_level]
```

### Implementation Example: Customer Churn Prediction

```
# Predictive Analysis Specification

## MODEL OBJECTIVE
- Prediction target: 90-day customer churn probability
- Model purpose: Binary classification with propensity scores
- Success criteria: Minimum AUC 0.80, precision at 20% threshold >70%, recall of high-value churners >80%

## FEATURE ENGINEERING
- Primary predictors:
  * purchase_recency: Days since last purchase (log transform, positive relationship)
  * purchase_frequency: Orders per month (square root transform, negative relationship)
  * avg_order_value: Mean purchase amount (log transform, negative relationship)
  * support_contacts: Support interactions (Box-Cox transform, positive relationship)
  * product_categories: Distinct categories purchased (ordinal, negative relationship)
- Derived features:
  * purchase_acceleration: Change in inter-purchase interval (signals engagement trend)
  * price_sensitivity: Ratio of discounted to full-price purchases (indicates value perception)
  * browse_to_buy_ratio: Browsing sessions per purchase (engagement efficiency metric)
- Interaction terms:
  * recency × frequency: Captures combined effect of engagement patterns
  * AOV × product_categories: Identifies valuable cross-category shoppers

## MODELING APPROACH
- Candidate algorithms:
  * Gradient Boosted Trees (XGBoost): Handles non-linear relationships, feature interactions; requires tuning max_depth, learning_rate, n_estimators
  * Logistic Regression with L1 regularization: High interpretability, efficient with sparse data; tune regularization strength
  * Random Forest: Robust to outliers, captures complex interactions; tune n_estimators, max_features
- Validation strategy: Time-based 70/30 split with temporal validation (ensure no future data leakage)
- Hyperparameter optimization: Bayesian optimization with 5-fold cross-validation; focus on precision/recall trade-off

## IMPLEMENTATION REQUIREMENTS
- Data preparation pipeline:
  * Missing value imputation using category medians
  * Outlier capping at 99th percentile
  * Feature scaling (MinMax for tree models, StandardScaler for logistic regression)
  * Categorical encoding using target encoding for high-cardinality variables
- Computational needs: Daily scoring batch process (<30 min runtime)
- Monitoring plan: Weekly data drift checks, monthly feature importance stability analysis, quarterly full retrain

## EVALUATION FRAMEWORK
- Technical metrics:
  * AUC-ROC (target >0.80)
  * Precision at 20% threshold (target >70%)
  * Recall of top-value quartile (target >80%)
  * Calibration error <0.05
- Business impact estimation:
  * Retention lift × customer value matrix
  * Intervention ROI by churn probability decile
  * Cost of false positives vs. missed retention opportunities
- Interpretability requirements:
  * SHAP values for instance-level explanations
  * Partial dependence plots for key variables
  * Segmented model performance metrics for fairness assessment
```

### Cluster Analysis Framework

```
# Segmentation Analysis Specification

## SEGMENTATION OBJECTIVE
- Purpose: [customer_segmentation/product_categorization/behavior_clustering]
- Business application: [targeting/positioning/assortment_planning]
- Stability requirements: [temporal_consistency_needs + refresh_frequency]

## VARIABLE SELECTION
- Clustering dimensions:
  * [variable_1]: [scale + importance + preprocessing]
  * [variable_2]: [scale + importance + preprocessing]
  * [variable_3]: [scale + importance + preprocessing]
- Dimensional weighting: [weighting_approach + business_rationale]
- Excluded variables: [variables_not_used + rationale]

## CLUSTERING METHODOLOGY
- Algorithm selection:
  * [algorithm_1]: [strengths + limitations + parameters]
  * [algorithm_2]: [strengths + limitations + parameters]
- Optimal cluster determination: [methods_for_selecting_cluster_count]
- Validation approach: [stability_measures + quality_metrics]

## SEGMENT PROFILING
- Characterization method: [statistical_approach_to_describe_clusters]
- Naming convention: [systematic_approach_to_segment_naming]
- Actionability assessment: [criteria_for_segment_usefulness]

## IMPLEMENTATION FRAMEWORK
- Deployment method: [scoring_system + assignment_rules]
- Transition handling: [approach_for_segment_changes_over_time]
- Business activation: [specific_use_cases_by_department]
```

### Implementation Example: Customer Value Segmentation

```
# Segmentation Analysis Specification

## SEGMENTATION OBJECTIVE
- Purpose: Customer value-behavior segmentation
- Business application: Marketing resource allocation, service tier design, product development prioritization
- Stability requirements: Quarterly validation with maximum 15% segment migration; annual full reclustering

## VARIABLE SELECTION
- Clustering dimensions:
  * annual_spend: Total 12-month purchases (log transform, high importance, normalized 0-1)
  * purchase_frequency: Annual purchase count (square root transform, high importance, normalized 0-1)
  * AOV: Average order value (log transform, medium importance, normalized 0-1)
  * category_breadth: Distinct categories (raw count, high importance, normalized 0-1)
  * discount_sensitivity: % discount needed to trigger purchase (arcsin transform, medium importance, normalized 0-1)
  * return_rate: Items returned / items purchased (logit transform, low importance, normalized 0-1)
- Dimensional weighting:
  * Value metrics (spend, frequency, AOV): 2.0× weight
  * Behavioral metrics (breadth, price sensitivity): 1.5× weight
  * Operational metrics (returns): 1.0× weight
- Excluded variables:
  * Demographic data (excluded to focus on behavioral segmentation)
  * Geographic data (analyzed as overlay rather than clustering input)
  * Attitudinal data (incomplete across customer base)

## CLUSTERING METHODOLOGY
- Algorithm selection:
  * K-means with weighted dimensions: Efficient, interpretable centroids, sensitive to outliers; parameters: n_clusters, max_iter
  * Hierarchical clustering (Ward's method): Creates intuitive dendrogram, captures nested segments; parameters: n_clusters, linkage
  * Gaussian mixture models: Probabilistic assignments, handles overlapping segments; parameters: n_components, covariance_type
- Optimal cluster determination:
  * Statistical: Silhouette score, Davies-Bouldin index, elbow method
  * Business: Minimum segment size (5% of base), maximum count (6 segments for manageability)
- Validation approach:
  * Internal: Silhouette coefficient >0.4, intracluster/intercluster distance ratio
  * Stability: Bootstrap resampling with Rand index comparison
  * Business: ANOVA of key performance metrics across segments

## SEGMENT PROFILING
- Characterization method:
  * Z-scores for each variable by segment
  * ANOVA with post-hoc tests for significant differences
  * Decision tree classifier to identify defining characteristics
- Naming convention:
  * Two-part system: Behavioral descriptor + value indicator
  * Example: "Loyal Enthusiasts" (high frequency + high breadth)
  * Consistent with prior segmentation where applicable
- Actionability assessment:
  * Segment size (minimum 5% of customers)
  * Value differential (minimum 30% LTV gap between adjacent segments)
  * Targetability (identifiable via accessible data for campaigns)
  * Response differential (proven difference in marketing elasticity)

## IMPLEMENTATION FRAMEWORK
- Deployment method:
  * Production scoring algorithm with daily customer assignment
  * Decisioning system integration for real-time experience customization
  * Probability scores for customers near segment boundaries
- Transition handling:
  * 30-day stability rule (prevent frequent segment changes)
  * Transition notification system for significant migrations
  * Hybrid treatment for customers in transition zones
- Business activation:
  * Marketing: Segment-specific campaign calendar and creative briefs
  * Product: Feature prioritization by segment value and size
  * Service: Resource allocation and script customization by segment
  * Merchandising: Assortment optimization based on segment preferences
```

## Domain-Specific Applications

### Financial Data Analysis Pattern

```
# Financial Data Analysis Framework

## FINANCIAL CONTEXT
- Data domain: [market_data/company_financials/transaction_data/risk_metrics]
- Time granularity: [intraday/daily/quarterly/annual]
- Analysis purpose: [valuation/risk_assessment/anomaly_detection/forecasting]

## ANALYTICAL COMPONENTS
1. Performance metrics:
   - [metric_1]: [calculation + benchmark + interpretation]
   - [metric_2]: [calculation + benchmark + interpretation]
   - [metric_3]: [calculation + benchmark + interpretation]

2. Trend analysis:
   - [time_series_approach]: [methodology + parameters + interpretation]
   - Seasonality assessment: [detection_method + adjustment_approach]
   - Volatility analysis: [measurement_technique + significance_thresholds]

3. Comparative analytics:
   - Peer benchmarking: [selection_criteria + normalization_approach]
   - Historical comparison: [baseline_periods + adjustment_methodology]
   - Risk-adjusted metrics: [risk_adjustment_technique + rationale]

## VISUALIZATION REQUIREMENTS
- Performance dashboards: [specific_charts + arrangement + highlights]
- Anomaly indicators: [visual_cues + threshold_representation]
- Forecast visualization: [uncertainty_bands + scenario_comparison]

## INSIGHTFUL OUTPUTS
- Key finding summary: [format + prioritization_method]
- Action recommendations: [decision_framework + implementation_guidance]
- Monitoring framework: [ongoing_metrics + alert_thresholds]
```

### Operational Analytics Pattern

```
# Operational Analytics Framework

## OPERATIONAL CONTEXT
- Process domain: [supply_chain/manufacturing/service_delivery/logistics]
- Performance focus: [efficiency/quality/reliability/speed/cost]
- Decision scope: [strategic/tactical/operational]

## ANALYTICAL COMPONENTS
1. Performance measurement:
   - KPI framework: [metrics_hierarchy + calculation_methods]
   - Baseline establishment: [benchmark_sources + normalization_technique]
   - Target setting: [methodology + rationale + stretch_vs_realistic]

2. Variance analysis:
   - Root cause identification: [analytical_approach + prioritization_method]
   - Contributing factor quantification: [attribution_technique + confidence_levels]
   - Systematic vs. special cause separation: [methodology + detection_thresholds]

3. Optimization modeling:
   - Constraint identification: [detection_method + impact_quantification]
   - Scenario development: [parameter_ranges + assumption_sets]
   - Solution evaluation: [multi-criteria_framework + sensitivity_analysis]

## VISUALIZATION REQUIREMENTS
- Performance tracking: [control_charts + trend_indicators + target_comparison]
- Process mapping: [flow_visualization + bottleneck_highlighting]
- Resource utilization: [capacity_views + allocation_efficiency]

## INSIGHTFUL OUTPUTS
- Improvement prioritization: [opportunity_sizing + effort_estimation + sequencing]
- Implementation roadmap: [phasing + dependency_mapping + milestone_definition]
- Monitoring system: [leading_indicators + feedback_mechanisms]
```

### Marketing Analytics Pattern

```
# Marketing Analytics Framework

## MARKETING CONTEXT
- Campaign type: [acquisition/retention/cross-sell/brand_awareness]
- Channel mix: [digital/traditional/direct/partner]
- Measurement approach: [attribution_model + incrementality_testing]

## ANALYTICAL COMPONENTS
1. Performance assessment:
   - Funnel metrics: [stage_definitions + conversion_calculations]
   - ROI calculation: [investment_components + return_definition + timeframe]
   - Effectiveness comparison: [normalization_approach + significance_testing]

2. Audience analysis:
   - Segmentation framework: [dimension_selection + methodology + validation]
   - Response modeling: [predictive_approach + variable_importance + accuracy_metrics]
   - Lifetime value projection: [calculation_method + discount_rate + confidence_intervals]

3. Optimization strategy:
   - Budget allocation: [optimization_algorithm + constraint_handling]
   - Message customization: [testing_framework + personalization_approach]
   - Timing optimization: [frequency_modulation + sequencing_logic]

## VISUALIZATION REQUIREMENTS
- Campaign dashboards: [KPI_hierarchy + trend_visualization + benchmark_comparison]
- Audience insights: [segment_profiling + response_distribution + behavior_patterns]
- Attribution visualization: [touchpoint_journey + impact_quantification + interaction_effects]

## INSIGHTFUL OUTPUTS
- Performance drivers: [component_contribution + leverage_points + enhancement_opportunities]
- Audience strategy: [targeting_recommendations + message_customization + engagement_approach]
- Optimization roadmap: [test_design + implementation_phases + expected_lift]
``` 