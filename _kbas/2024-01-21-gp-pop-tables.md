---
layout: post
title: POP Tables 
date:   2024-01-20 00:00:00 -0800
author: horacio 
image:  '/images/gp.webp'
tags:   [great plains, kba]
favorite: true
tags_color: '#477690'
---
# POP Tables

Commonly Used Tables:  
POP00101 – Buyer Master  
POP10100 – Purchase Order Work (header)  
POP10110 – Purchase Order Line Work (line detail)  
POP10150 – Purchase Order Comment (header)  
POP10300 – Receipt Work (header)  
POP10306 – Purchasing Receipt User-Defined  
POP10310 – Receipt Work Line (line detail)  
POP10330 – Serial / Lot Work  
POP10390 – Receipt Work Distributions  
POP10500 – Receipt Line Quantities (line detail)  
POP10550 – Line Item Comment (line detail)  
POP10600 – Purchasing Shipment Invoice Apply  
POP30100 – Purchase Order History (header)  
POP30110 – Purchase Order Line History (line detail)  
POP30300 – Receipt History (header)  
POP30310 – Receipt Line History (line detail)  
POP30330 – Serial / Lot History  
POP30390 – Distribution History  
POA40003 – PO Approval Control  

<cite>Status in POP10500:</cite>
```
0 – Unposted
1 – Posted
2 – Voided
```

PO Status:
```
1 – New
2 – Released
3 – Change Order
4 – Received
5 – Closed
6 – Cancelled
```

STATGRP (Status Group):
```
0 – Voided [this is not a valid according to the SDK, but we have seen it for voided PO’s]
1 – Active (includes New, Open and Modified)
2 – Closed (includes Cancelled and Closed)
```

[`Note:` In our experience, when a PO is voided and it moves to the history tables, in POP30100 the STATGRP will be 1 or 0 whereas for a regularly closed PO the STATGRP will be 2. Also, there is a value starting with POPVT in TRXSORCE of POP30100 for voided PO’s.]

PO Type:
```
1 – Standard
2 – Drop Ship
3 – Blanket
4 – Blanket Drop Ship
```

POLNESTA (PO Line Status):
```
1 – New
2 – Released
3 – Change Order
4 – Received
5 – Closed
6 – Cancelled
```

POPTYPE (POP Receipt Type):
```
1 – Shipment
2 – Invoice
3 – Shipment/Invoice
4 – Return
5 – Return w/Credit
6 – Inventory Return
7 – Inventory Return w/Credit
8 – Intransit Transfer (thanks to Jesus M. Cruz Narvaez for this one)
```

[Thanks to [Frank Hamelly](http://gp2themax.blogspot.com){:target="_blank"} of GP2theMax for the complete list of POP Receipt Types, as these are not in the SDK.]

DISTTYPE (Distribution Type):
```
1 – Purchases
2 – Trade Discounts
3 – Freight
4 – Miscellaneous
5 – Tax
6 – Discounts Available
7 – Accounts Payable
8 – Other
9 – Accrued
10 – Round
```

NONINVEN (Non-Inventory):
```
0 – Inventory item
1 – Non-inventory item
```

DECPLCUR (Decimal Places for Currency):
```
7 – 0
8 – 1
9 – 2
10 – 3
11 – 4
12 – 5
```

DECPLQTY (Decimal Places for Quantity):
```
1 – 0
2 – 1
3 – 2
4 – 3
5 – 4
6 – 5
```

DOCTYPE in POP10550:
```
1 – PO
2 – Receipt
```

ITMTRKOP (Item Tracking):
```
1 – None
2 – Serial Numbers
3 – Lot Numbers
```

PO Approval Status in POA40003:
```
1 – Unapproved
2 – Approved
```

PO Note ID Array in POP10100:
```
1 – PO Note Index – PONOTIDS_1
2 – Buyer Note Index – PONOTIDS_2
3 – Vendor ID Index – PONOTIDS_3
4 – Comment Note Index – PONOTIDS_4
5 – Payment Term ID Note Index – PONOTIDS_5
6 – Shipping Method Note Index – PONOTIDS_6
7 – Currency ID Index – PONOTIDS_7
8 – Tax Schedule Index – PONOTIDS_8
9 – Freight Tax Schedule Index – PONOTIDS_9
10 – Misc Tax Schedule Index – PONOTIDS_10
11 – Contract Number Index – PONOTIDS_11
12 – PONOTIDS_12 – not used at this time
13 – PONOTIDS_13 – not used at this time
14 – PONOTIDS_14 – not used at this time
15 – PONOTIDS_15 – not used at this time
```

PO Line Note ID Array Array in POP10110:
```
1 – Item Number Note Index – POLNEARY_1
2 – Location Code Note Index – POLNEARY_2
3 – Line Comment Note Index – POLNEARY_3
4 – Inventory Index Note Index – POLNEARY_4
5 – PO Line Note Index – POLNEARY_5
6 – Item Tax Schedule Note Index – POLNEARY_6
7 – Site Tax Schedule Note Index – POLNEARY_7
8 – Landed Cost Group ID Note Index – POLNEARY_8
9 – Shipping Method Note Index – POLNEARY_9
```

---

> Retrieved from [https://victoriayudin.com](https://victoriayudin.com/gp-tables/pop-tables){:target="_blank"}

