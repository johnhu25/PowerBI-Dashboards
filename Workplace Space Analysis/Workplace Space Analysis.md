Dashboard Link: https://github.com/johnhu25/PowerBI-Dashboards/blob/main/Workplace%20Space%20Analysis/Space%20Utilisation.pbix
Download PDF: https://github.com/johnhu25/PowerBI-Dashboards/blob/main/Workplace%20Space%20Analysis/Space%20Utilisation.pdf

# Executive Summary

This dashboard integrates space allocation data with booking activity to uncover actionable trends in desk usage, availability, check-in behavior, and occupancy patterns across buildings and countries. By visualizing these metrics together, it enables stakeholders to identify underutilised spaces, optimise capacity planning, and improve workplace efficiency based on real-time and historical user behavior.

# Problem Statement
Despite a substantial number of workspace bookings across global locations (5,113 non cancelled total bookings in 2025), less than half (49%) of these bookings resulted in actual check-ins (2,508). This low utilisation rate, combined with notable geographic and building-level disparities such as Brazil having the highest check-ins and India the lowest, and Celestial Tower being significantly more utilised than Royal Heights indicates inefficiencies in workspace usage and potential gaps in employee engagement or booking policy compliance.
Additionally, is the employee actually sitting at the desk and forgetting to check-in which is resulting in lower check-ins?

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

# Spaces Overview

- Total Workspaces: 1,567
- Bookable Desks: 890
- Countries: 7
- Buildings: 7
- Desks Under Maintenance: 156
- Occupied Spaces: 1,176
- Under Maintenance: 156
- Vacant: 235

# Booking Information
- Total Bookings: 5,648
- Total Bookiings (Not Cancelled): 5113
- Bookings with Check-in: 2,508
- Cancelled Bookings: 535
- Most Booked Building: Celestial Tower
- Least Booked Building: Royal Heights
- Top Check-In Country: Brazil
- Least Check-In Country: India
- Top Check-In Rate: Germany
- Lowest Check-In Rate: Netherlands

# Usage Trends & Patterns

- With a 49% Check-in rate this indicates that half of the spaces are not used, this causes wasted resources and reduced availability for employees that want to book.
- 9.5% cancellation rate may be good monitor if it is a healthy rate or too high.
- Brazil had the highest check-ins due to having the most spaces but with only a 49% check-in rate.
- Netherlands had the lowest check-ins, which may indicate, lower engagement despite booking.
- Under Maintenance (10%) and Vacant rate (15%) combined 25% is high which means only 75% of spaces are utilised.

Things that can affect Attendence
- Location popularity
- Availability of amenities
- Team preferences
- Organizational presence

# Actionable Insights & Recommendations
Issue/Opportunity, Recommendation
- Investigate Low check-in reasons to assist in improving them by employee feedback.
- Enforce stricter check-in rules or auto-release or another measurement to know they were utilising the space.
- Desk underutilization	Reduce or consolidate desks in low-use floors and decrease the vacant rate.
- Underused meeting spaces convert to bookable desks or cancel unused slots.
- Investigate if the employee is sitting at the desk but not check-in.

# Measures/PBI Queries

    Average Bookings Per Days = 
    VAR TotalBookings =
    COUNTROWS('employee_bookings')
    VAR BookingDays =
    DISTINCTCOUNT('employee_bookings'[Booking Long Date])
    RETURN
    DIVIDE(TotalBookings, BookingDays)

    Cancelled Booking Rate = ([Total Bookings (Not Cancelled)]/[Cancelled Bookings])/100

    Cancelled Bookings = 
    CALCULATE(
    COUNTROWS('employee_bookings'),
    'employee_bookings'[Booking Cancelled] = "Yes"
    )

    Checked In Count = 
    CALCULATE(
        COUNTROWS('employee_bookings'),
        'employee_bookings'[Checked In] = "Yes"
    )

    Count Country = DISTINCTCOUNT('spaces'[Country])

    Least Booked Buildings = 
    CALCULATE(
    FIRSTNONBLANK('employee_bookings'[Building], 1),
    TOPN(
        1,
        SUMMARIZE(
            'employee_bookings',
            'employee_bookings'[Building],
            "BookingCount", COUNTROWS('employee_bookings')
        ),
        [BookingCount],
        ASC
    )
    )

    
