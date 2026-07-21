# 🥤 Lemonade Change | LeetCode 860

## Approach

I solved this problem using the **Greedy** algorithm.

The idea is to process each customer one by one while keeping track of the number of `$5` and `$10` bills available. Since every lemonade costs `$5`, each customer must receive the correct change immediately.

For each bill:

- If the customer pays with `$5`, simply increase the count of `$5` bills.
- If the customer pays with `$10`, give back one `$5` bill as change and increase the count of `$10` bills.
- If the customer pays with `$20`, always try to give one `$10` bill and one `$5` bill first, as this preserves more `$5` bills for future transactions. If that isn't possible, give three `$5` bills. If neither option is available, return `false`.

If all customers receive the correct change, return `true`.

---

## My Thought Process

- Maintain the count of `$5` and `$10` bills.
- Process each customer in order.
- Update the bill counts after every transaction.
- For a `$20` bill, prioritize giving one `$10` and one `$5` as change.
- If exact change cannot be provided at any point, return `false`.

---

## Concepts Used

- Greedy Algorithm
- Simulation
- Arrays

---

## Time Complexity

- **Time:** O(n)

## Space Complexity

- **Space:** O(1)

---

## What I Learned

This problem helped me understand how a greedy strategy can lead to an optimal solution. By always preferring to give a `$10` and a `$5` bill as change for a `$20` payment, I preserved smaller denominations for future customers, ensuring the maximum chance of successfully completing all transactions.

---

## Key Takeaway

When solving greedy problems, always make the **best local decision** that improves future possibilities. In this problem, preserving `$5` bills by using a `$10 + $5` combination whenever possible is the optimal strategy.
