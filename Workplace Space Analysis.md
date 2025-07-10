Dashboard Link: https://github.com/johnhu25/PowerBI-Dashboards/blob/main/Space%20Utilisation.pbix

# Executive Summary

This dashboard merges space allocation data with booking activity to uncover trends in desk usage, availability, check-in behavior, and occupancy patterns across buildings and countries.

# Problem Statement
How to know if spaces are under utilised and if

# Data Sources
- Generated with Faker https://pypi.org/project/Faker/
- spaces.csv Desk/Space information
- employee_bookings.csv All bookings made on desks, with status & attendance between 1/01/2025 to 31/12/2025

# Data Preparation
- Removed duplicates
- Removed missing values
- Created new columns/measures

# Tools and Techniques
- Power BI, Excel
- DAX, Pivot tables, Aggregation (AVG, SUM, COUNT), DISTINCT, TOPN,
- Visualisation includes Map, Donut Chart, Column Chart, Area Chart
- Filters, Location (Country, Building, Floor), Org Unit, Space Type, Date

# Descriptive Statistics
Space Information
Total Workspaces: 1,567
Bookable Desks: 890
Countries: 7
Buildings: 7
Desks Under Maintenance: 156
Occupied Spaces: 1,176
Under Maintenance: 156
Vacant: 235

Booking Information
Total Bookings: 5,648
Bookings with Check-in: 2,508 (44%)
Booking Not Checked In: 3,140 (56%)
Cancelled Bookings: 535
Most Booked Building: Celestial Tower
Least Booked Building: Royal Heights
Top Check-In Country: Brazil
Least Check-In Country: India


# Key Findings:
- 5,648 bookings were made across 1,567 desks across 2025.
- Only 44% of bookings resulted in check-ins.
- Meeting Rooms and Office Desks are the most frequently used space types.
- Over 1 in 5 bookings were not checked in, indicating potential ghost bookings or did not go.

# Usage Trends & Patterns
By Space Type:
Most Space Type: Office Desk
Most Booking Space Types: Office Desk

By Country:
Most Spaces: Brazil
Least Spaces Germany
Most Bookable Desks: Australia
Least Bookable Desks: India
Brazil had the highest check-ins, suggesting high space utilization or effective attendance.

India had the lowest check-ins, which may indicate:
- Higher cancellation.
- Lower engagement despite booking.

By Building:
Location popularity
Availability of amenities
Team preferences
Organizational presence

# Check-In & Attendance Analysis

Checked In: 2,508 Only ~44.4% of bookings led to actual check-ins.
Avg Bookings/Day: 15.52 Reflects daily booking activity.
Avg Checked In/Day: 6.91 Fewer than half of daily bookings resulted in check-ins.
Cancelled Bookings: 535 About 9.5% of total bookings were canceled.


# Desk Utilization Analysis



# Actionable Insights & Recommendations
Issue/Opportunity	Recommendation
High no-show rate (56%)	Enforce stricter check-in rules or auto-release
Desk underutilization	Reduce or consolidate desks in low-use floors
Poor Last Used tracking	Sync booking activity with desk metadata system
Missing team/org linkage	Integrate team/org hierarchy for better filtering
Underused meeting spaces	Convert to bookable desks or cancel unused slots
