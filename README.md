# Data-analytics
# Drop rows with too many missing values or impute
df = df.dropna(subset=['Satisfaction'])  # Assume 'Satisfaction' is the target

# Fill missing values
df.fillna(df.mean(), inplace=True)

# Convert categorical variables to numeric (if any)
df = pd.get_dummies(df, drop_first=True)
