# O2C Process — Step-by-Step Guide

## Step 1: Customer Inquiry (VA11)
T-Code: VA11 | Inquiry type: IN
Enter: customer no., material, quantity, requested date
Output: Inquiry Doc No. (e.g., 10000001)

## Step 2: Quotation (VA21)
T-Code: VA21 | Reference: Inquiry number
Set validity 30 days, confirm pricing
Output: Quotation Doc No. (e.g., 20000001)

## Step 3: Sales Order (VA01)
T-Code: VA01 | Order type: OR | Reference: Quotation
ATP check + Credit check auto-run
Output: Sales Order No. (e.g., 30000001) KEY DOCUMENT

## Step 4: Delivery (VL01N)
T-Code: VL01N | Reference: Sales Order
Confirm picking quantity in warehouse
Output: Delivery Doc No. (e.g., 80000001)

## Step 5: Goods Issue (VL02N)
T-Code: VL02N | Click: Post Goods Issue
Effect: Stock reduced in MM, COGS in FI auto-posted

## Step 6: Billing (VF01)
T-Code: VF01 | Billing type: F2
Effect: Invoice to customer, AR posted in FI
Output: Billing Doc No. (e.g., 90000001)

## Step 7: Payment (F-28)
T-Code: F-28 | Reference: Invoice number
Effect: AR cleared, O2C complete!
