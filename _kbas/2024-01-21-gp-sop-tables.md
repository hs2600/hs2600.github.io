---
layout: post
title:  SOP Tables 
date:   2024-01-20 00:00:00 -0800
author: horacio 
image:  '/images/gp.webp'
tags:   [great plains, kba]
favorite: true
tags_color: '#477690'
---

# SOP Tables

Commonly Used Tables:

- SOP10100 – Unposted/Work Transactions (header)  – one record per unposted sales transaction  
- SOP10200 – Unposted/Work Transactions (line detail)  – one record per line item on unposted sales transactions (for kits, there will be one record per kit component)  
- SOP10101 – Commissions Work and History  
- SOP10102 – GL Distributions Work and History  – GL distributions for posted and unposted Invoices, Returns and Fulfillment Orders  
- SOP10103 – Payment Work and History  – one record per payment entered on sales transaction  
- SOP10104 – Process Holds Work and History  
- SOP10105 – Sales Taxes Work and History  
- SOP10106 – User Defined Work and History  – this table will also have the transaction level comment  
- SOP10107 – Tracking Numbers Work and History  
- SOP10201 – Serial/Lot Work and History  
- SOP10202 – Line Comment Work and History  
- SOP30200 – Historical Transactions (header)  – one record per posted sales transaction  
- SOP30300 – Historical Transactions (line detail)  – one record per line item on posted sales transactions (for kits, there will be one record per kit component)  
- SOP60100 – SOP-POP Link  – one record for each link to a PO line, unique link on: SOPNUMBE, SOPTYPE, LNITMSEQ  
- SOP60300 – Customer Item Numbers  

SOPTYPE (SOP Document Types):
```
1 – Quote
2 – Order
3 – Invoice
4 – Return
5 – Back Order
6 – Fulfillment Order
```

Distribution Types:
```
1 – SALES
2 – RECV
3 – CASH
4 – TAKEN
5 – AVAIL
6 – TRADE
7 – FREIGHT
8 – MISC
9 – TAXES
10 – MARK
11 – COMMEXP
12 – COMMPAY
13 – OTHER
14 – COGS
15 – INV
16 – RETURN
17 – IN USE
18 – IN SERVICE
19 – DAMAGED
20 – UNIT
21 – DEPOSITS
22 – ROUND
23 – REBATE
```

PYMTTYPE (Payment Type) in SOP10103:
```
1 – Cash Deposit
2 – Check Deposit
3 – Credit Card Deposit
4 – Cash Payment
5 – Check Payment
6 – Credit Card Payment
```

[Note:  The PYMTTYPE values in the GP SDK are not correct, at least for the recent versions of GP – thank you to Beth Lott for bringing that to my attention.  I have confirmed the values above with GP Support.]

Decimal Places (for both Quantity and Currency):
```
1 – 0
2 – 1
3 – 2
4 – 3
5 – 4
6 – 5
```

Transaction Frequency:
```
1 – Weekly
2 – Biweekly
3 – Semimonthly
4 – Monthly
5 – Bimonthly
6 – Quarterly
7 – Miscellaneous
```

PURCHSTAT (Purchasing Status):
```
1 – None (will always be this for Quote, Return and Invoice)
2 – Needs Purchase
3 – Purchased
4 – Partially Received
5 – Fully Received
```

QTYTYPE (Quantity Type):
```
1 – On Hand
2 – Returned
3 – In Use
4 – In Service
5 – Damaged
```

PROSPECT:
```
0 – Existing Customer
1 – Prospect
```

COMAPPTO (Commission Applied To):
```
0 – Sales
1 – Invoice Total
```

VOIDSTTS (Void Status):
```
0 – Not Voided
1 – Voided
```

DROPSHIP (Drop Ship):
```
0 – No Drop Ship
1 – Drop Ship
```

NONINVEN (Non-Inventory):
```
0 – Inventory item
1 – Non-inventory item
```

SOPSTATUS (SOP Status):
```
1 – New  (Order)
2 – Ready to Print Pick Ticket  (Fulfillment Order)
3 – Unconfirmed Pick  (Fulfillment Order)
4 – Ready to Print Pack Slip  (Fulfillment Order)
5 – Unconfirmed Pack  (Fulfillment Order)
6 – Shipped  (Fulfillment Order)
7 – Ready to Post  (Invoice)
8 – In Process  (Order)
9 – Complete  (Order)
```

DELETE1 (Delete)  in SOP10104:
```
0 – Not deleted
1 – Hold has been removed
```

PSTGSTUS (Posting Status):
```
0 – Not posted
2 – Posted
3 – Error
7 – checking for Duplicate Document numbers
12 – verifying accuracy of amounts between detail & header
14 – verifying total detail amounts match header amount
508 – transferring record from SOP10100 to SOP30200
600 – validating detail & header records match in history tables
```

### Notes on reporting in SOP:  
- Remember to filter out voided transactions.
- When linking SOP tables, always link on the SOPNUMBE and SOPTYPE.  While it doesn’t happen too often in real life, the system will allow you to have the same SOP number for different SOP types.
- On Invoices and Returns, QUANTITY is what was billed/credited, however, if you want to see the quantity in the ‘Base’ Unit of Measure (what the Inventory module keeps the quantities in), you will need to multiply the QUANTITY by the QTYBSUOM (Quantity in Base U of M).
- Returns will show up as positive numbers – you’ll need to change the sign if you are adding all the transactions together.
- Try not to use DEXROWID for any reporting logic, as there are times where these get repopulated, for example when you upgrade to a new version.

---

> Retrieved from [https://victoriayudin.com](https://victoriayudin.com/gp-tables/sop-tables){:target="_blank"}

