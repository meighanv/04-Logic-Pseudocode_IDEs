# Total Purchase  
Display "Enter price for item 1"  
input price1  
Display "Enter price for item 2"  
input price2  
Display "Enter price for item 3"  
input price3  
Display "Enter price for item 4"  
input price4  
Display "Enter price for item 5"  
input price5  
set SALES_TAX = 0.06  
set subtotal = price1 + price2 + price3 + price4 + price5  
set total = subtotal + (subtotal * SALES_TAX)  
  
