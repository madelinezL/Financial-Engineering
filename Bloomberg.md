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
#### Swamp Manager <br/>
Swamp Manager - Solver leg 1 coupon
Add Leg - By Type - Floored Floater 
Change the date 05/04/2022, 10/31/2026 accordingly
Change the premium to be 0
Change the other attributes, i.e. pay freq, index, spread, floor, etc.
