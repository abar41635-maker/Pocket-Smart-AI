print("================================")
print("       PocketSmart AI")
print(" Smart Budget & Recommendation")
print("================================")

name = input("Enter your name: ")
income = float(input("Enter monthly income: ₹"))
goal = float(input("Enter savings goal: ₹"))
print("\nExpense Categories:")
print("1. Food")
print("2. Travel")
print("3. Shopping")
print("4. Education")
print("5. Other")

food = float(input("Food expenses: ₹"))
travel = float(input("Travel expenses: ₹"))
shopping = float(input("Shopping expenses: ₹"))
education = float(input("Education expenses: ₹"))
other = float(input("Other expenses: ₹"))

total_expense = food + travel + shopping + education + other
balance = income - total_expense
expenses = {
    "Food": food,
    "Travel": travel,
    "Shopping": shopping,
    "Education": education,
    "Other": other
}

highest = max(expenses, key=expenses.get)
print("\n----- Budget Summary -----")
print("Name:", name)
print("Income: ₹", income)
print("Food: ₹", food)
print("Travel: ₹", travel)
print("Shopping: ₹", shopping)
print("Education: ₹", education)
print("Other: ₹", other)
print("Total Expenses: ₹", total_expense)
print("Remaining Balance: ₹", balance)
print("Savings Percentage:", round((balance/income)*100, 2), "%")
print("Highest Expense Category:", highest)
print("Savings Goal: ₹", goal)
print("Difference: ₹", balance - goal)
if balance >= goal:
    print("Goal Achieved! 🎉")
else:
    print("Goal Not Achieved!")
if highest == "Food":
    print("Suggestion: Try to reduce food expenses.")
elif highest == "Shopping":
    print("Suggestion: Control shopping expenses.")
elif highest == "Travel":
    print("Suggestion: Reduce travel expenses if possible.")
if balance > 0:
    print("\nRecommendation: Good! You have savings.")
elif balance == 0:
    print("\nRecommendation: Income and expenses are equal.")
else:
    print("\nRecommendation: Reduce unnecessary expenses.")

print("\nThank you for using PocketSmart AI!")
print("Thank you,", name)
print("Keep tracking your expenses regularly!")
