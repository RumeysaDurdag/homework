# homework
studentlist = ["Rümeysa Durdağ"]
for i in range(3):
    student = input('Enter name and surname: ')
    if student in studentlist:
      print("Welcome")
      break
    if i == 2:
      print("Please try again later")
courses = []
for i in range(5):
    tempCourse = input("Enter a course name: ")
    courses.append(tempCourse)
lessons = []
def lesson_num(number):
    if 6 > number > 2:
        for i in range(number):
            takenlessons = input("Enter course you want: ")
            lessons.append(takenlessons)
            print(takenlessons)
        return "Your lessons: ", lessons
    elif number < 3:
        return "You failed in class!"
    else:
        return "You cannot take more than 5 lessons"
if True:
    number = int(input("How many lessons you want to take: "))
    print(lesson_num(number))
keys = "midterm", "final", "project"
grades = dict(zip(keys, ([] for _ in keys)))
print(grades)
for i in keys:
    exams_grade = int(input("Enter your grades: "))
    grades[str(i)] = exams_grade
print(str(dict(grades)))
def total_average(grades):
    midterm = grades["midterm"]
    final = grades["final"]
    project = grades["project"]
    score = 0.3 * midterm + 0.5 * final + 0.2 * project
    return score
def letter_grade(score):
    if score >= 90:
        return "AA"
    elif 70 <= score < 90:
        return "BB"
    elif 50 <= score < 70:
        return "CC"
    elif 30 <= score < 50:
        return "DD"
    else:
        return "FF"
print(letter_grade(total_average(grades)))
if letter_grade(total_average(grades)) == "FF":
    print("You are failure")
