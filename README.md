# cybersecurity-3
build a tool that assesses the strength of the password based on the criteria such as length,presence of uppercase and lowercase letters ,numbers and special characters


import re

def check_length(password):
    return len(password) >= 8

def has_uppercase(password):
    return bool(re.search(r'[A-Z]', password))

def has_lowercase(password):
    return bool(re.search(r'[a-z]', password))

def has_digit(password):
    return bool(re.search(r'[0-9]', password))

def has_special_char(password):
    return bool(re.search(r'[!@#$%^&*(),.?":{}|<>]', password))

def assess_password_strength(password):
    score = 0
    feedback = []

    if check_length(password):
        score += 1
    else:
        feedback.append("Password should be at least 8 characters long.")

    if has_uppercase(password):
        score += 1
    else:
        feedback.append("Password should contain at least one uppercase letter.")

    if has_lowercase(password):
        score += 1
    else:
        feedback.append("P
