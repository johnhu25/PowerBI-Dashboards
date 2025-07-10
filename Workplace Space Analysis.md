Dashboard Link: https://github.com/johnhu25/PowerBI-Dashboards/blob/main/Space%20Utilisation.pbix

# Executive Summary

This dashboard merges space allocation data with booking activity to uncover trends in desk usage, availability, check-in behavior, and occupancy patterns across buildings and countries.

# Key Findings:
- 5,648 bookings were made across 1,567 desks.
- Only 44% of bookings resulted in check-ins.
- Meeting Rooms and Office Desks are the most frequently used space types.
- Over 1 in 5 bookings were not checked in, indicating potential ghost bookings or did not go.
    
# Data Sources
- Generated with Faker https://pypi.org/project/Faker/
- spaces.csv space information
- employee_bookings.csv All bookings made on desks, with status & attendance

# Problem Statement
How to use this data to know if spaces are under utilised.

# Descriptive Statistics
Space Information
Total Workspaces: 1,567
Bookable Desks: 890

Desks Under Maintenance: 521
Most Common Space Type: Office Desk

Booking Activity 
Total Bookings: 5,648
Bookings with Check-in: 2,508 (44%)
Booking Not Checked In: 3,140 (56%)
Cancelled Bookings: 535
Most Booked Building: Celestial Tower
Least Booked Building: Royal Heights

# Usage Trends & Patterns
By Space Type:

By Country:

# Check-In & Attendance Analysis

- Total Check-ins: 2,508
- Avg. Checked-in per Day: 6.91
- Desks with 0% Check-in Rate: Likely ghost desks or unused resources


# Desk Utilization Analysis



# Actionable Insights & Recommendations
Issue/Opportunity	Recommendation
High no-show rate (56%)	Enforce stricter check-in rules or auto-release
Desk underutilization	Reduce or consolidate desks in low-use floors
Poor Last Used tracking	Sync booking activity with desk metadata system
Missing team/org linkage	Integrate team/org hierarchy for better filtering
Underused meeting spaces	Convert to bookable desks or cancel unused slots
