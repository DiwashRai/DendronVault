---
id: mi2mzcn3m38ojt23pvwtr4c
title: Simpleorderbook Rthickling
desc: ''
updated: 1665622686229
created: 1665622686229
---

## logic

- parse arguments
- init order_book: dict
- clear my_output.csv if it exists
- init output trades_file (trade_csv_file)
- init input orders_file

- iterate through each order in orders_file
  - place_order(order_book, order_data, trade_csv_file) - each order_data: Customer, Item, Side, Quantity, Price
    - if 'Item' is not in order_data
      - create a new OrderBook for Item e.g. new orderbook for 'IBM'
    - create order object from order_data
    - order_book['Item'].match(order, side == 'buy')

__OrderBook.Match logic__
match(self, order, is_bid)
- Init matches list []
- if is_bid
  - other_side = asks
  - this_side = bids
  - compare = le
- else
  - other_side = bids
  - this_side = asks
  - compare = ge
- init matched_orders_to_remove list []
- loop through other_side:
  - if compare other.price /w order.price. If Ask price is lower than Bid and vice versa
    - partial_fill bool = other.quantity < order.quantity
    - quantity = order.quantity if enough. else other.quantity
    - if partial-fill
      - order.quantity - other.quantity
      - add other to matched_orders_to_remove
    - else
      - add other to matched_orders_to_remove
      - residual_quantity = other.quantity - order.quantity
      - order.quantity = 0
      - if there is residual_quantity
        - other.side.add(residual_quantity, other.price, other.customer, other.sequence_number)
      - break
    else: // means there's no more at acceptable price
      - break
- loop through matched_orders_to_remove
  - remove matched_order
- if orders.quantity left
  - this_side.add(order)
- if matches:
  - output to trade_csv_file



## Classes

### OrderBook
__Members__
  - name
  - trade_csv_file
  - bids: BidSide()
  - asks: AskSide()
  - sequence_number

__Methods__
  - get_sequence_number
  - depth
    - returns asks + bids
  - match
    - Most of the logic located here

### Order
Data container
__Members__
  - quantity
  - price
  - customer
  - sequence_number

__Methods__
  - __lt__ : less than
  _ __eq__ : equality
  - forward_key
  - reverse_key
  - __str__ : returns string of the data