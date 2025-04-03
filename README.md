
# goit-js-hw-06

This repository contains JavaScript objects and classes for managing customer data, storage operations, and string manipulation.

## `task-1.js` - `customer` object

Represents a customer with balance, discount, and order management functionalities.

### Methods:
---
#### `getBalance()` - returns the current balance of the customer.

**Returns:**
-   `number` – the current balance.
    
**Example:**
```
console.log(customer.getBalance()); // 24000
```
---
#### `getDiscount()` - returns the current discount rate.

**Returns:**
-   `number` – the discount rate.
    
**Example:**
```
console.log(customer.getDiscount()); // 0.1
```
---
#### `setDiscount(value)` - updates the customer's discount rate.

**Params:**
-   `value` (number) – new discount rate.
   
**Example:**
```
customer.setDiscount(0.15);
console.log(customer.getDiscount()); // 0.15
```
---
#### `getOrders()` - returns the list of customer orders.

**Returns:**
-   `array` – an array of ordered items.
    
**Example:**
```
console.log(customer.getOrders()); // ["Burger", "Pizza", "Salad"]
```
---
#### `addOrder(cost, order)` - adds a new order and updates the balance, applying the discount.

**Params:**
-   `cost` (number) – price of the order.
-   `order` (string) – name of the ordered item.
    
**Example:**
```
customer.addOrder(5000, 'Steak');
console.log(customer.getBalance()); // 19750
console.log(customer.getOrders()); // ["Burger", "Pizza", "Salad", "Steak"]
```
----------

## `task-2.js` - `Storage` class

Manages a collection of items with methods to add, remove, and retrieve them.

### Methods:
---
#### `getItems()` - returns the stored items.

**Returns:**
-   `array` – the list of stored items.
    
**Example:**
```
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator"]
```
---
#### `addItem(newItem)` - adds a new item to the storage.

**Params:**
-   `newItem` (string) – item to add.
    
**Example:**
```
storage.addItem('Droid');
console.log(storage.getItems()); // ["Nanitoids", "Prolonger", "Antigravitator", "Droid"]
```
---
#### `removeItem(itemToRemove)` - removes a specified item from the storage.

**Params:**
-   `itemToRemove` (string) – item to remove.
    
**Example:**
```
storage.removeItem('Prolonger');
console.log(storage.getItems()); // ["Nanitoids", "Antigravitator", "Droid"]
```
----------

## `task-3.js` - `StringBuilder` class

Allows string manipulation by adding characters at the start, end, or both sides of a string.

### Methods:
---
#### `getValue()` - returns the current string value.

**Returns:**
-   `string` – the stored string value.
    
**Example:**
```
console.log(builder.getValue()); // "."
```
---
#### `padEnd(str)` - appends the provided string to the end.

**Params:**
-   `str` (string) – string to append.
    
**Example:**
```
builder.padEnd('^');
console.log(builder.getValue()); // ".^"
```
---
#### `padStart(str)` - prepends the provided string at the beginning.

**Params:**
-   `str` (string) – string to prepend.
    
**Example:**
```
builder.padStart('^');
console.log(builder.getValue()); // "^."
```
---
#### `padBoth(str)` - adds the provided string to both the beginning and end.

**Params:**
-   `str` (string) – string to add on both sides.
    
**Example:**
```
builder.padBoth('=');
console.log(builder.getValue()); // "=^.^="
```