*4/22/2023*
### Bloomberg Guide
#### Prepayment <br/>
The prepayment option gives the borrower or issuer the flexibility to pay off the debt early. This can be beneficial for several reasons, such as reducing the total amount of interest paid over the life of the loan, freeing up cash flow for other investments or expenses, or taking advantage of lower interest rates. However, prepayment options may come with certain restrictions or penalties, such as a prepayment fee or a minimum time period before the prepayment is allowed. <br/>
* How to search/calculate prepayment option value in BB
  - SWPM &#8594; Product &#8594; Option &#8594; Cancel swap american
  - Input Year (needs to be consistent)
  - If it is a prepayment option, short; If demand option, long
  - Change NC (non-callable) = 0D (zero date), notification days = 0BD (business days)
  - Set NPV=0
  - Get the par coupon rate and coupon rate. Prepayment option value = coupon - par coupon
  - By default, US0003M (3-month US Dollar LIBOR rate). We also want to see SOFRRATE (1D)


#### Yield Curve <br/>
Yield refers to the return on an investment, usually expressed as a percentage. A yield curve is a graphical representation of the relationship between the yield (i.e., interest rate) of bonds or other fixed-income securities and their respective maturities. Bonds with longer maturities generally have higher yields than bonds with shorter maturities. This is because investors demand a higher yield for holding longer-term bonds due to the greater uncertainty and risk associated with the longer holding period. <br/>
* How to search/calculate prepayment option value in BB
  - CRVF &#8594; Credit &#8594; Type in the Name &#8594; Choose Graph &#8594; Table &#8594; Value
  - Input Date
  - Select the table and screenshot
 
*8/28/2023*
#### REIT Yield Curve <br/>
CRVF - Credit - Sector BBB or BB or B - Then type REIT - Graph Selected Curves - Table - Values - Update the Date

*10/25/2023*
#### Swap Manager <br/>
Swap Manager - Solver leg 1 coupon <br/>
Add Leg - By Type - Floored Floater <br/>
Change the date 05/04/2022, 10/31/2026 accordingly <br/>
Change the premium to be 0 <br/>
Change the other attributes, i.e. pay freq, index, spread, floor, etc. <br/>

*1/10/2024*
#### Weighted Average Spread <br/>
Enter the CLO name <br/>
Choose the respective one <br/>
Group Summary
WAS 

*1/12/2024*
#### USD SOFR <br/>
Enter "USD SOFR (vs. FIXED RATE)", can also chose "YCSW0490 Index under Securities" - GC (graph curve) <br/>
Date as of xx/xx/xx <br/>
Table <br/>
Values

#### USD Composite <br/>
Enter "USD US Composite B-" <br/>
Date as of xx/xx/xx <br/>
Table <br/>
Values <br/>
Curves & Relatie Value - Add Curve - enter other credit ratings <br/>
Chart - Copy/Export Options - Copy Data to Clipboard


*3/4/2024*
#### How to perform a search on corporate bonds in a specific industry
Enter BICS (Bloomberg Industry Classification System), choose Semiconductors <br/>
Open a new tab, enter SRCH Fixed Income <br/>
Enter a series of criteria <br/>
1. BICS Classification - Semiconductor <br/>
2. Moody's Rating - Baa1 - Baa3 <br/>
3. Country/Region of Risk - United States of America <br/>
4. Coupon Type - Fixed <br/>
5. Maturity Type - Bullet or Make Whole Call <br/>
6. Maturity - 03/04/2029

*3/25/2024*
#### How to search Industrial Classification Info for a company
Enter Company Name or Ticker (e.g. Dynatrace Inc, DT US Equity) <br/>
Enter BICS <br/>
Enter the industry in "Search for an Industry" bar <br/>
Choose the company

#### How to search USD US Financial Services Industry YTM 
CRVF - Credit - Financials <br/>
Select BBB, Type USD US Financials, click the USD US Financials BBB+, BBB, BBB- BVAL Yield Curve <br/>
Same for BB and B <br/>
Clieck Graph Slected Curves (GC) <br/>
Change the date to be as of 3/1/24


*3/18/2024*
#### How to pull the interest rate on CRE CLO tranches
Key in the CRE CLO code (i.e. GSTNE 2024-HC3) <br/>
Choose the Multiple Matches (i.e. GSTNE 2024-HC3 Mtge) <br/>
Need the value of Floater Spread, Floater Formula columns

#### How to pull the IRR on CRE CLO tranches
Following the above steps, select the Class A <br/>
Select Group Summary <br/>
WAC (Weighted Average Coupon)

*4/1/2024*
#### How to pull the FX rates for SPOT and FORWARD
Spot <br/>
CADUSD Curncy - HP <br/>
Select the date to be deal date
Forward <br/>
FRD <br/>
Type Currencies, Pricing Date, Type Value forwarded date under Broken Dates
