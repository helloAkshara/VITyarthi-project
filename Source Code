import tkinter as tk
import re
def check_strength(password):
    score = 0
    if len(password) >= 8:
        score += 1
    if re.search(r'[A-Z]', password):
        score += 1
    if re.search(r'[a-z]', password):
        score += 1
    if re.search(r'\d', password):
        score += 1
    if re.search(r'[!@#$%^&*()_+{}|:<>?]', password):
        score += 1
    if score <= 2:
        return "Weak"
    elif score <= 4:
        return "Medium"
    else:
        return "Strong"
def on_check():
    pwd = entry.get()
    strength = check_strength(pwd)
    result_label.config(text=f"Password Strength: {strength}")
root = tk.Tk()
root.title("Password Strength Checker")
root.geometry("400x400")
tk.Label(root, text="Enter Password:").pack(pady=10)
entry = tk.Entry(root, show="*")
entry.pack(pady=5)
tk.Button(root, text="Check Strength", command=on_check).pack(pady=10)
result_label = tk.Label(root, text="")
result_label.pack(pady=10)
root.mainloop()
