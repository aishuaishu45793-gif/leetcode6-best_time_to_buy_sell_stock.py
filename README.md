# 📈 Best Time to Buy and Sell Stock

This project contains my Python solution for the **Best Time to Buy and Sell Stock** problem from LeetCode.

## 🧩 Problem

You are given an array `prices` where `prices[i]` represents the stock price on the `i`-th day.

You can:

* Buy the stock on one day.
* Sell the stock on a different day in the future.
* Complete only one transaction.

The goal is to find the **maximum profit**.

If no profit is possible, return `0`.

## 💡 Example

### Input

```text
prices = [7, 1, 5, 3, 6, 4]
```

### Output

```text
5
```

### Explanation

Buy at price `1` and sell at price `6`.

```text
Profit = 6 - 1 = 5
```

## 🐍 Python Solution

```python
class Solution:
    def maxProfit(self, prices):
        min_price = prices[0]
        max_profit = 0

        for price in prices:
            if price < min_price:
                min_price = price

            profit = price - min_price

            if profit > max_profit:
                max_profit = profit

        return max_profit


solution = Solution()

prices = [7, 1, 5, 3, 6, 4]

print(solution.maxProfit(prices))
```

### Output

```text
5
```

## 🔍 Approach

The solution keeps track of two values:

* `min_price` → the lowest stock price seen so far.
* `max_profit` → the highest profit found so far.

For every price:

1. Check if it is the lowest price.
2. Calculate the possible profit.
3. Update `max_profit` if the profit is larger.

This allows us to solve the problem in one pass through the array.

## ⏱️ Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(1)`

## 🛠️ Technologies

* Python
* LeetCode
* VS Code
* Git & GitHub

## ▶️ How to Run

1. Open the project in VS Code.
2. Open the Python file.
3. Save the file.
4. Open the VS Code terminal.
5. Run:

```bash
python filename.py
```

## 📚 What I Learned

* Working with Python lists
* Using `for` loops
* Finding minimum values
* Calculating maximum profit
* Understanding `O(n)` time complexity
* Solving LeetCode problems using Python
* Using Git and GitHub for version control

## 🚀 Learning Journey

This project is part of my **LeetCode problem-solving journey**.

I am practicing Python, Data Structures, Algorithms, and problem-solving skills one problem at a time.

---

⭐ **If you find this project useful, feel free to star the repository!**
