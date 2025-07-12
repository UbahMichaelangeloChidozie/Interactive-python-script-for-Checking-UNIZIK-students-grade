# Interactive-python-script-for-Checking-UNIZIK-students-grade
def get_grade(score):
    if 70 <= score <= 100:
        return "A"
    elif 60 <= score < 70:
        return "B"
    elif 50 <= score < 60:
        return "C"
    elif 46 <= score < 50:
        return "D"
    elif 40 <= score < 46:
        return "E"
    elif 0 <= score < 40:
        return "F"
    else:
        return "Invalid score"

def main():
    print("KNOW YOUR GRADE!")
    try:
        score = float(input("Enter your score (0 - 100): "))
        grade = get_grade(score)
        if grade == "Invalid score":
            print("⚠️ Please enter a score between 0 and 100.")
        else:
            print(f"Your grade is: {grade}")
    except ValueError:
        print("❌ Invalid input! Please enter a number.")

if __name__ == "__main__":
    main()