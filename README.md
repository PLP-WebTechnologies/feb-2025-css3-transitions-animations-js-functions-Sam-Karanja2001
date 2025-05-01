# CSS3 Transitions, Animations, and Advanced JavaScript Functions

## Objectives

Create smooth CSS transitions and animations.
Use JavaScript functions for dynamic behavior.
Implement local storage for data persistence.

## Instructions
Add CSS animations to elements like buttons or images.

>[!NOTE]
> - Write a JavaScript function that:
> - Stores and retrieves user preferences using localStorage.
> - Implements an animation triggered by user actions.

## Tasks

Create a CSS animation.
Store data in localStorage.
Apply JavaScript to trigger animations.

Happy Coding! 💻✨


Question 1: INNER JOIN (Employees & Offices)
```sql
SELECT e.firstName, e.lastName, e.email, o.officeCode
FROM employees e
INNER JOIN offices o ON e.officeCode = o.officeCode;
```

Question 2: LEFT JOIN (Products & ProductLines
```sql
SELECT p.productName, p.productVendor, pl.productLine
FROM products p
LEFT JOIN productlines pl ON p.productLine = pl.productLine;
```

### Question 3: RIGHT JOIN (Customers & Orders)
```sql
SELECT o.orderDate, o.shippedDate, o.status, o.customerNumber
FROM customers c
RIGHT JOIN orders o ON c.customerNumber = o.customerNumber
ORDER BY o.orderDate
LIMIT 10;
```

CSS Animation
```css
button {
    background-color: #3498db;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    transition: transform 0.3s ease-in-out;
}

button:hover {
    transform: scale(1.1);
}
```

JavaScript for Animation & LocalStorage
```js
document.getElementById("animateBtn").addEventListener("click", function() {
    this.style.transform = "scale(1.5)";
    localStorage.setItem("userClicked", "true");

    setTimeout(() => {
        this.style.transform = "scale(1)";
    }, 500);
});

window.onload = function() {
    if (localStorage.getItem("userClicked") === "true") {
        document.getElementById("animateBtn").style.backgroundColor = "#2ecc71";
    }
};
```
