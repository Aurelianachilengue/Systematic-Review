# Systematic-Review
Cohen's Kappa_script
# Step 1: Install necessary packages (run these only if not already installed)
install.packages("readxl")  # For reading Excel files
install.packages("irr")     # For calculating Cohen's Kappa

# Step 2: Load the required libraries
library(readxl)  # To read Excel files
library(irr)     # To calculate Cohen's Kappa

# Step 3: Read the Excel file (replace 'your_file.xlsx' with your actual file path)
data <- read_excel("/Users/N1225366/Documents/Documents_Lenovo/Projecto_CHILI/Mozambique/Publicacao/Systematic Review paper/Hellen feedback/ReviwersDecision_Table.xlsx")

# Step 4: Preview the data to ensure it was loaded correctly
head(data)  # Shows the first few rows of the data

# Step 5: Calculate Cohen's Kappa using the specified columns
kappa_result <- kappa2(data[, c("Reviewer A Decision", "Reviewer B Decision")])

# Step 6: Print the result
print(kappa_result)  # Displays Cohen's Kappa statistic and related info

# Step 7: Extract specific details if needed
kappa_value <- kappa_result$value   # Extracts the Kappa value
kappa_confidence <- kappa_result$conf.int  # Extracts the confidence intervals

# Optional: Print extracted values
print(kappa_value)  # Print only the Kappa statistic

