 Monthly Electricity Bill Calculator A simple and efficient Python script to calculate the monthly electricity bill based on consumption (kWh) using a configurable, tiered rate structure.

🌟 Features Tiered Rate Calculation: Calculates cost based on different rates for different consumption blocks (e.g., first 50 units at one rate, next 100 at another).

Fixed Service Charge: Includes a fixed monthly service/meter charge in the final bill.

Detailed Breakdown: Provides a step-by-step breakdown of how the total consumption charge is calculated across the tiers.

User-Friendly: Simple command-line interface for inputting consumption data.

🚀 Getting Started Prerequisites You only need Python installed on your system.

Python 3.x

Installation Clone the repository (if hosted) or download the script (electricity_bill_calculator.py).

Open your terminal or command prompt.

Navigate to the directory where you saved the file.

Usage Run the script from your terminal:

Bash

python electricity_bill_calculator.py The program will prompt you to enter the total monthly consumption:

Enter the total monthly electricity consumption in kWh: Enter the value (e.g., 250.5) and press Enter.

The output will display the detailed calculation and the final bill amount:

--- Consumption Breakdown --- Consumed 50.00 kWh @ Rs3.50/kWh = Rs175.00 Consumed 100.00 kWh @ Rs5.00/kWh = Rs500.00 Consumed 100.50 kWh @ Rs6.50/kWh = Rs653.25 Fixed Monthly Service Charge: Rs50.00 Total Consumption Charge: Rs1328.25 ⚡ Total Electricity Bill for 250.50 kWh: Rs1378.25 ⚡ ⚙️ Configuration The rate structure is defined inside the calculate_electricity_bill function and can be easily modified to match any local utility tariffs.

Rate Tiers Modify the RATE_TIERS dictionary. The keys represent the cumulative upper limit of the consumption block, and the values are the rate per kWh for that block. Upper Limit (kWh) Rate (Rs/kWh) Block Covered 50 3.50 1 to 50 kWh 150 5.00 51 to 150 kWh 300 6.50 151 to 300 kWh float('inf') 8.00 Above 300 kWh

Export to Sheets

Code Snippet:

Python

RATE_TIERS = { 50: 3.50, # First 50 kWh at Rs3.50 per unit 150: 5.00, # Next 100 kWh (up to 150 total) at Rs5.00 per unit 300: 6.50, # Next 150 kWh (up to 300 total) at Rs6.50 per unit float('inf'): 8.00 # All units above 300 kWh at Rs8.00 per unit } 2. Service Charge Modify the SERVICE_CHARGE variable for the fixed monthly fee.

Code Snippet:

Python

SERVICE_CHARGE = 50.00 # Fixed monthly charge 📝 Future Enhancements [ ] Load rates from a configuration file (e.g., JSON or CSV) instead of hardcoding.

[ ] Include tax calculations (e.g., GST/VAT) on the final amount.

[ ] Allow calculation for multiple months or comparison between months.

[ ] Implement a simple graphical user interface (GUI).
