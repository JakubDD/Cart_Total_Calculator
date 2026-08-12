

https://roadmap.sh/projects/js-cart-total-calculator](https://roadmap.sh/projects/js-cart-total-calculator)

Cart Total Calculator

A simple JavaScript program that calculates a shopping cart's subtotal, discount, tax, and final total.

Features
Calculate the subtotal by multiplying each item's price by its quantity
Apply a percentage-based discount to the subtotal
Apply a percentage-based tax on the amount after discount
Combine everything into a single cart summary object
Functions
calculateSubtotal(items)

Loops through an array of cart items and sums price * quantity for each one.

js
calculateSubtotal([{ price: 10, quantity: 2 }]); // 20
calculateDiscount(subtotal, discountPercent)

Returns the discount amount based on a percentage of the subtotal.

js
calculateDiscount(100, 10); // 10
calculateTax(amountAfterDiscount, taxPercent)

Returns the tax amount, calculated on the amount remaining after the discount is applied.

js
calculateTax(90, 5); // 4.5
createCartSummary(items, discountPercent, taxPercent)

Combines all the above into one summary object:

js
{
  subtotal,
  discount,
  tax,
  total,
}
Usage
bash
node cart.js
Example
js
const cartItems = [
  { name: 'Notebook', price: 10, quantity: 2 },
  { name: 'Pen', price: 2, quantity: 5 },
  { name: 'Bag', price: 30, quantity: 1 },
];

console.log(createCartSummary(cartItems, 10, 5));
// { subtotal: 60, discount: 6, tax: 2.7, total: 56.7 }
Project structure
cart-total-calculator/
├── cart.js
└── README.md
What I practiced
Array iteration with for...of
Function composition (smaller functions used inside a bigger one)
Working with percentages in calculations
Returning and structuring objects
Exporting functions with module.exports

