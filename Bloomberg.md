*4/22/2023*
### Bloomberg Guide
#### Prepayment <br/>
The prepayment option gives the borrower or issuer the flexibility to pay off the debt early. This can be beneficial for several reasons, such as reducing the total amount of interest paid over the life of the loan, freeing up cash flow for other investments or expenses, or taking advantage of lower interest rates. However, prepayment options may come with certain restrictions or penalties, such as a prepayment fee or a minimum time period before the prepayment is allowed. <br/>
* How to search/calculate prepayment option value in BB
  - SWPM &#8594; Product &#8594; Browse All; Cancellable Swap American (-CS -AMR)
  - Solver (Coupon)
  - Set premium = 0
  - Input Year (most of the time needs to be consistent) (Effective Date, Maturity Date, Curve Date (agreement date), Valuation (agreement date)) 
  - If it is a prepayment option, short; If demand option, long
  - Change NC (non-callable) = 0D (zero date), notification days = 0BD (business days) or just by default
  - Get the par coupon rate and coupon rate. Prepayment option value = coupon - par coupon
  - By default, US0003M (3-month US Dollar LIBOR rate), hit GC, but we want to use SOFRRATE (1D)
  - Note: 1) For prepayment option, we only change the Receive Column, do not touch the Pay part. <br/>
          2) We only change the blue part (variable), green is what Bloomberg generates for us.


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
Swap Manager <br/>
Add Leg - By Type - Floored Floater <br/>
Delete the Float leg <br/>
Change the Solver to be Leg 1: Coupon <br/>
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
Chart - Copy/Export Options - Copy Data to Clipboard <br/> <br/>

USD US Composite 
BS569: BB+
BS570: BB
BS571: BB-
BS572: B+
BS573: B
BS574: B-


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
Click Graph Slected Curves (GC) <br/>
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
CAD USD Curncy - HP <br/>
Select the date to be deal date <br/> <br/>
Forward <br/>
FRD <br/>
Type Currencies, Pricing Date, Type Value forwarded date under Broken Dates

*4/12/2024*
#### How to do an interest rate benchmark (Internal CUP)
SRCH (fixed income search) <br/>
Asset Classes (select Corporates, Additional Options: Consolidate Duplicate Bonds) <br/>
Remove Security status (as bloomberg does not have functionality to seek for past effective date) <br/>
Issuer name, input Santander Holdings USA Inc. Current Issuer and all subsidiaries <br/>
Issue Date <= 10/16/2023 <br/>
Maturity >= 10/16/2023 <br/>
Maturity Type Select Bullet, Make Whole Call <br/>
Coupon Type: Fixed <br/>

Adjust the column <br/>
Issuer Name <br/>
Bloomberg ID <br/>
Country/Region of Risk <br/>
BICS Level 1 Classification <br/>
BICS Level 2 Classification <br/>
Issue Date <br/>
Maturity <br/>
Next Call Date <br/>
Maturity Type <br/>
Coupon <br/>
Coupon Frequency Description <br/>
Coupon Type <br/>
Currency <br/>
Amount Issued <br/>
Amount Outstanding <br/>
BBG Composite <br/>
Moody's Rating <br/>
S&P Rating <br/>
Fitch Rating <br/>
Day Count Description <br/>

##### After Determining the comparable securities, <br/>

Input code, select securities, HP <br/>
as of 10/16/2023 <br/>
Source: TRACE (if you choose BVAL, you need to double check - Type BVAL, enter Security Code and confirm it is above 6 for the score) <br/>
Mid YTM 6.608

#### How to do an interest rate benchmark (External CUP)
Common Criteria: <br/>
Security Status (active) <br/>
BBG Composite <br/>
Country/Region of Risk <br/>
Coupon Type <br/>
BICS Classification <br/>
Currency USD <br/>
Maturity 10/16/2024-10/16/2028 (we usually benchmark remaining tenor (maturity date - effective date of our tested party)) <br/>
Maturity Type (i.e. Bullet / At Maturity, Make Whole Call)

### How to search the YTM of a security
Type the security code
as of date
Change the source to be TRACE
HP

### How to check BVAL final score
Type BVAL <br/>
Enter Securities Code <br/>
Change the Pricing Date <br/>
You can see the final BVAL score (out of 10)
We want to reject the one with BVAL <=6

### Elements to consider adjustments when doing CUPs
Credit Rating <br/>
Tenor <br/>
Term <br/>
Prepayment (Coupon - Par Coupon) <br/>
Frequency (Usually for USD US Financials, the frequency is semi-annual)
