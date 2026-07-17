---
title: cart
categories:
  - Console Command
---

Commands for interacting with a character's cart.

Commands | Description
-------- | -----------
`cart` | Display a list of items in your cart.
`cart add <inventory_item> [<amount>]`<br>`cart add <inventory_item#> [<amount>]` | Add an item to cart from your inventory.
`cart get <cart_item> [<amount>]`<br>`cart get <cart_item#> [<amount>]` | Get an item from cart to your inventory.
`cart desc <cart_item#>` | Display a description of the specified cart item.
`cart release` | Release your cart.


`<inventory_item>` - an inventory [item name](../References.md/#item_names) from the inventory item list when you use the [`i`](i.md) command.

`<inventory_item#>` - a corresponding number from the inventory item list.

`<cart_item>` - a cart [item name](../References.md/#item_names) from the cart item list when you use the `cart` command.

`<cart_item#>` - a corresponding number from the cart item list when you use the `cart` command.

`<amount>` - [number](../References.md/#number) of items. Optional value.

!!! Note
    If the amount is not specified, this assumes the maximum amount of the item available.
