# Responsive-Product-Cards
Using grid for desktop and mobile

## Step 1 — HTML

## Step 2 — Desktop CSS
Try writing this yourself first:

.products {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.card {
  padding: 20px;
  border: 1px solid #ddd;
}

Expected:
```text
┌────────┐ ┌────────┐ ┌────────┐
│ Laptop │ │ Phone  │ │ Mouse  │
│ ₹50,000│ │ ₹30,000│ │ ₹1,000 │
└────────┘ └────────┘ └────────┘

┌────────┐ ┌────────┐ ┌────────┐
│Keyboard│ │ Monitor│ │Headphone│
└────────┘ └────────┘ └────────┘
```
## Step 3 — Responsive Mobile CSS
@media (max-width: 768px) {
  .products {
    grid-template-columns: 1fr;
  }
}

Expected:
```text
┌──────────┐
│  Laptop  │
│ ₹50,000  │
└──────────┘

┌──────────┐
│  Phone   │
│ ₹30,000  │
└──────────┘

┌──────────┐
│  Mouse   │
│ ₹1,000   │
└──────────┘
```
## ⭐ Bonus: More Responsive Production-Style Version

Once you can build the above without notes, try:

.products {
  display: grid;
  grid-template-columns:
    repeat(auto-fit, minmax(220px, 1fr));
  gap: 20px;
}

This can reduce the need for manually specifying every breakpoint.

## CSS Rapid-Fire Interview Answers

### 1. What is CSS Grid?
A two-dimensional layout system for arranging elements in rows and columns.

### 2. Grid vs Flexbox?
Grid is two-dimensional; Flexbox is primarily one-dimensional.

### 3. When use Grid instead of Flexbox?
When I need structured control over both rows and columns.

### 4. What is 1fr?
A fraction of the available space in a Grid container.

### 5. What does repeat() do?
It repeats Grid track definitions, such as repeat(3, 1fr).

### 6. auto-fit vs auto-fill?
auto-fit collapses empty tracks and lets existing items expand; auto-fill can preserve empty track positions.

### 7. What is minmax()?
It defines the minimum and maximum size of a Grid track.

### 8. Can Grid and Flexbox work together?
Yes. For example, Grid for the page layout and Flexbox inside individual cards.

### 9. How do you create a responsive Grid?
Use media queries or a fluid combination such as repeat(auto-fit, minmax(...)).


## 🧠 Remember This

```
Grid
 ↓
Rows + Columns

Flexbox
 ↓
Row OR Column

1fr
 ↓
Fraction of available space

repeat()
 ↓
Repeat tracks

minmax()
 ↓
Minimum + Maximum

auto-fit
 ↓
Fit existing items

auto-fill
 ↓
Fill possible tracks

Media Query
 ↓
Responsive breakpoints
```
