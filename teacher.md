---FILE: nandini-cs-teacher-portfolio.md---

# Nandini NC - CBSE Computer Science Teacher Profile

## Professional Summary
Hello, I'm Nandini NC, Java Full Stack Developer with 2 years of combined experience in **teaching and development**.

### Experience
- **Java Full Stack Trainer** (1 year)  
  **Besant Technologies, Bangalore**  
  Trained students in Java full stack development and guided them to secure jobs in software companies.

- **Java Full Stack Developer** (1 year)  
  **Swajyot Technologies, Bangalore**  
  Handled full-stack development (UI, APIs, database) and presented product demos to clients.

## Education
- **Bachelor of Engineering** - Computer Science  
  **KLS VDIT, Haliyal** (2021)
- **Diploma** - Computer Science  
  **Government Polytechnic, Hubli** (2017)

## Personal Background
I live with my mother and two younger brothers in **Hubli near Glass House**. Currently based in **Bangalore Koramangala** for work.

## Why Switch to Teaching?
> "Working away from home worries my mother, especially since she isn't keeping well often. As the sole breadwinner, teaching roles near Hubli let me leverage my 2 years of development + training experience while staying home. **I'm passionate about teaching**."

## Interview Ready Answers

### **Q: What is a Flowchart?**
Visual diagram using symbols to show process steps, decisions, and flow direction from start to end.

### **Q: Student Not Paying Attention?**
1. Stand near them (proximity)  
2. Question directly (accountability)  
3. Pair with focused student  
4. After class: Find root cause

### **Q: Student Copied Code?**
1. Private discussion: "Whose idea was this?"
2. Ask to explain line-by-line
3. Assign original mini-project
4. Praise unique solutions publicly

### **Q: Students Hate Coding?**
- Start with **Scratch games** (Pong)
- **Pair programming** (strong+weak)
- Celebrate **"Hello World"** wins
- Build **student attendance system**

## Technical Demo: Loops (Java)

```java
// Print "Hello" 5 times - WRONG WAY ❌
System.out.println("Hello");
System.out.println("Hello");
System.out.println("Hello");
System.out.println("Hello");
System.out.println("Hello");

// CORRECT WAY - for loop ✅
for(int i = 0; i < 5; i++) {
    System.out.println("Hello");
}
```

**3 Loop Types:**
```java
// 1. for loop - Print 1-5
for(int i = 1; i <= 5; i++) {
    System.out.print(i + " ");
}

// 2. while loop - Sum 1-10
int total = 0, i = 1;
while(i <= 10) {
    total += i; i++;
}

// 3. Nested - Star pattern
for(int row = 1; row <= 4; row++) {
    for(int star = 1; star <= row; star++) {
        System.out.print("* ");
    }
    System.out.println();
}
```

## Live Interview Demo: Grade Calculator
```java
import java.util.Scanner;
public class GradeDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter marks: ");
        int marks = sc.nextInt();
        
        if(marks >= 90) System.out.println("🎉 A Grade");
        else if(marks >= 80) System.out.println("👍 B Grade"); 
        else if(marks >= 70) System.out.println("👌 C Grade");
        else System.out.println("💪 Practice More!");
    }
}
```

**Teaching Flow**: Ask marks → Run → Students change boundaries → Real grades connection.

---
