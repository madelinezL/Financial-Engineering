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


