```
student_grades = {
    "건우": 90,
    "채원": 85,
    "현우": 92,
}
for student in student_grades:
    grade = student_grades[student]
    print(student, grade)
```
코드설명:  
```
student_grades = {
    "건우": 90,
    "채원": 85,
    "현우": 92,
}
```
- 이 부분은 딕셔너리(dictionary) 를 생성하는 코드입니다.
- student_grades는 학생들의 이름을 키(key), 점수를 값(value)으로 가지는 딕셔너리입니다.
- 예를 들어 "건우"라는 이름의 학생은 점수 90점을 가지고 있습니다.

```
for student in student_grades:
    grade = student_grades[student]
    print(student, grade)
```
이 코드는 student_grades라는 딕셔너리 안에 있는 모든 학생 이름과 점수를 하나씩 꺼내서 출력하는 코드예요.
1. for student in student_grades:  
➤ 해석:  
딕셔너리 student_grades 안에 있는 모든 키(key), 즉 학생 이름을 하나씩 꺼내서 student라는 변수에 저장하며 반복합니다.  
이 for문은 다음처럼 작동합니다:  
- 첫 번째 반복: student = "건우"
- 두 번째 반복: student = "채원"
- 세 번째 반복: student = "현우"

2. grade = student_grades[student]
➤ 해석:  
방금 위에서 꺼낸 학생 이름(student)을 사용해서 점수를 가져옵니다.  
예: student = "건우"일 때. 
grade = student_grades["건우"] → grade = 90. 
즉, 딕셔너리[키] 를 쓰면 해당 키에 연결된 값을 얻을 수 있어요.  

3. print(student, grade). 
➤ 해석:  
현재 반복 중인 학생 이름(student)과 점수(grade)를 출력합니다.  
예: "건우"와 90 → 출력: 건우 90. 

---
