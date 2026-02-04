# CDR Dataset Analysis - Assignment 1

## Overview of Approach
This analysis examines telecommunications activity across Milan, Italy using Call Detail Records from three days in November 2013. The dataset captures SMS, calls, and internet usage patterns across 10,000 geographic grid squares.

## Analysis Workflow
Data Integration - Combined three daily datasets from November 2, 4, and 6 into a unified dataset with temporal tracking.
Data Cleaning - Addressed missing values through statistical imputation to ensure data quality.

Feature Engineering - Created aggregate metrics for SMS, calls, internet, and total activity to enable comprehensive analysis.
Temporal Analysis - Extracted hourly patterns to identify peak usage times and compared daytime versus nighttime distributions.
Geographic Analysis - Examined activity patterns across grid squares and compared domestic versus international behavior.
Statistical Correlation - Applied statistical methods to explore relationships between different activity types.

## Key Decisions
# Missing Value Treatment
Approach: Mean imputation for all numeric columns
Rationale: Preserves overall distribution while maintaining statistical validity
Impact: Imputed 4.4 million missing values across 2.2 million records, affecting 33% of the dataset in SMS outgoing, incoming calls, outgoing calls, and internet activity columns

## Time Period Classification
Daytime: 6:00 AM to 8:00 PM (14 hours)
Nighttime: 8:00 PM to 6:00 AM (10 hours)
Rationale: Aligns with standard human activity patterns and working hours
Geographic Classification

## Domestic: Country code 39 representing Italy
International: All other country codes
Rationale: Dataset originates from Milan; provides clear classification for comparative analysis
Aggregation Strategy
Grid-level aggregation for correlation analysis to reveal geographic patterns while reducing transaction-level noise.

## Summary of Key Findings
Dataset Overview
The dataset contains 6,564,031 records across three dates covering 10,000 unique grid squares in Milan with 222 country codes indicating diverse international connectivity.
Temporal Patterns

Peak Activity: Overall peak occurs at 6:00 PM in the evening, with lowest activity at 4:00 AM during sleep hours.
Activity Distribution: 79.77% of all telecommunications activity occurs during daytime hours compared to 20.23% during nighttime hours.

Call Statistics: Average of 0.32 calls per record with median of 0.28 and standard deviation of 0.22, indicating a right-skewed distribution with highest variability during evening hours between 6:00 PM and 8:00 PM.

## International vs Domestic Communication
Volume Distribution: Domestic telecommunications dominate the dataset with 93.52% of calls and 93.55% of SMS classified as domestic. International activity represents 6.48% of calls and 6.45% of SMS, maintaining a consistent 6.5% share across both communication channels.
Temporal Synchronization: Both international and domestic calls peak at 6:00 PM with extremely high correlation of 0.9999 between their hourly patterns, suggesting international communication from Milan follows similar daily rhythms as domestic communication rather than being driven by time zone differences.

Call Direction: International calls show a ratio of 0.90 for incoming versus outgoing, indicating 10% more outgoing than incoming calls. This suggests Milan residents actively initiate international communication rather than primarily receiving calls from abroad.
Activity Correlations

SMS and Calls: Correlation of 0.9998 at grid level indicates extremely strong relationship. Grid squares with high call volume consistently show high SMS volume. Linear relationship shows approximately 1.48 SMS messages occur for every call made.
Cross-Channel Patterns: All activity types show extremely high correlations: SMS versus internet at 0.9999 and calls versus internet at 0.9997. This indicates users engage comprehensively across all communication channels rather than specializing in a single medium.

Geographic Distribution: Activity is not uniformly distributed, with top 10% of grid squares accounting for disproportionate share of total activity, indicating concentration in commercial and residential centers.

# Conclusions: 
Predictable Daily Rhythms - Clear peak hours align with work-life patterns. The overwhelming majority of activity occurs during daytime hours, following predictable human behavior with evening peaks and early morning lows.

Integrated Communication Behavior Strong correlations exceeding 0.98 between SMS, calls, and internet usage indicate users engage across multiple channels rather than specializing in one medium.

International Connectivity Patterns - While representing only 6.5% of total activity, international communication follows similar temporal patterns to domestic usage. The outgoing bias suggests active international engagement by Milan residents.

Data Quality Achievement - Successfully handled missing data affecting one-third of records through mean imputation, enabling robust analysis across the full dataset.

Network Planning Insights - Peak capacity needed at 6:00 PM with daytime infrastructure requirements significantly higher than nighttime. Geographic clustering suggests opportunities for targeted infrastructure investment.