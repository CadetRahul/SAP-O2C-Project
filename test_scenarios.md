# Test Scenarios

## Scenario 1: Normal O2C Flow (Happy Path)
Customer: ABC Pvt Ltd | Material: Laptop 15" | Qty: 10 | Price: 55000/unit | GST: 18%
Expected: All 7 steps complete, AR cleared, stock reduced by 10

## Scenario 2: Credit Limit Block
Customer credit limit: 5,00,000 | Order value: 8,00,000
Expected: Sales Order blocked at VA01 due to credit limit

## Scenario 3: Partial Delivery
Order qty: 50 | Available stock: 30
Expected: Delivery for 30, backorder for 20

## Scenario 4: Returns (RE Order)
Order type: RE | Reference: Original billing doc
Expected: Return delivery created, credit memo issued
