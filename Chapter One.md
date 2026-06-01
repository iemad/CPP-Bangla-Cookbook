# সি প্রোগ্রামিং - পূর্ণাঙ্গ নোট

## **Class 0: প্রোগ্রামিং এর ভূমিকা (Introduction to Programming)**

### প্রোগ্রামিং কী?
প্রোগ্রামিং হলো কম্পিউটারকে নির্দেশ দেওয়ার প্রক্রিয়া। কম্পিউটারকে দিয়ে কাজ করিয়ে নিতে আমাদের তাকে নির্দেশ দিতে হয়, এই নির্দেশগুলোকেই প্রোগ্রাম বলে।

### প্রোগ্রামিং ভাষা:
- **Low Level Language**: মেশিনের কাছাকাছি (Machine Language, Assembly Language)
- **High Level Language**: মানুষের বোধগম্য (C, C++, Java, Python)

### C ভাষার ইতিহাস:
- **১৯৭২ সালে** Dennis Ritchie C ভাষা আবিষ্কার করেন
- Bell Labs-এ UNIX অপারেটিং সিস্টেম তৈরির জন্য এটি ব্যবহার করা হয়
- C ভাষা খুব শক্তিশালী এবং দ্রুতগতির ভাষা

---

## **Class 1: প্রথম প্রোগ্রাম (First Program)**

### মৌলিক প্রোগ্রামের গঠন:

```c
#include <stdio.h>

int main() {
    printf("Hello, World!\n");
    return 0;
}
```

### কোডের ব্যাখ্যা:

1. **`#include <stdio.h>`**: এটি একটি প্রি-প্রসেসর ডিরেক্টিভ। এটি stdio.h হেডার ফাইল ইনক্লুড করে, যা ইনপুট-আউটপুট ফাংশনের জন্য প্রয়োজন [[12]]

2. **`int main()`**: এটি প্রোগ্রামের মূল ফাংশন। প্রতিটি C প্রোগ্রাম main() ফাংশন থেকে শুরু হয়

3. **`printf("Hello, World!\n");`**: এটি স্ক্রিনে টেক্সট প্রদর্শন করে। `\n` নতুন লাইনে যাওয়ার জন্য ব্যবহার করা হয় [[13]]

4. **`return 0;`**: প্রোগ্রাম সফলভাবে শেষ হয়েছে নির্দেশ করে

### আউটপুট:
```
Hello, World!
```

### আরও উদাহরণ:

```c
#include <stdio.h>

int main() {
    printf("আমার নাম: রহিম\n");
    printf("বয়স: ২৫ বছর\n");
    printf("শহর: ঢাকা\n");
    return 0;
}
```

---

## **Class 2: ভেরিয়েবল (Variable)**

### ভেরিয়েবল কী?
ভেরিয়েবল হলো মেমোরির একটি নামকরণ করা স্থান যেখানে ডেটা সংরক্ষণ করা হয় [[3]]। ভেরিয়েবলের মান পরিবর্তন করা যায়, তাই একে ভেরিয়েবল (পরিবর্তনশীল) বলে।

### ভেরিয়েবল ঘোষণা:
```c
datatype variable_name;
```

### ভেরিয়েবল ঘোষণা ও মান নির্ধারণ:

```c
#include <stdio.h>

int main() {
    int age;           // ঘোষণা
    age = 25;          // মান নির্ধারণ
    
    float height = 5.8; // একসাথে ঘোষণা ও মান নির্ধারণ
    
    char grade = 'A';
    
    printf("বয়স: %d\n", age);
    printf("উচ্চতা: %.1f\n", height);
    printf("গ্রেড: %c\n", grade);
    
    return 0;
}
```

### আউটপুট:
```
বয়স: 25
উচ্চতা: 5.8
গ্রেড: A
```

### ভেরিয়েবল ব্যবহারের উদাহরণ:

```c
#include <stdio.h>

int main() {
    int num1 = 10;
    int num2 = 20;
    int sum;
    
    sum = num1 + num2;
    
    printf("প্রথম সংখ্যা: %d\n", num1);
    printf("দ্বিতীয় সংখ্যা: %d\n", num2);
    printf("যোগফল: %d\n", sum);
    
    return 0;
}
```

### আউটপুট:
```
প্রথম সংখ্যা: 10
দ্বিতীয় সংখ্যা: 20
যোগফল: 30
```

---

## **Class 3: ভেরিয়েবল নামকরণের নিয়ম (Variable Naming Conventions)**

### বাধ্যতামূলক নিয়ম:

1. **ভেরিয়েবল নাম অবশ্যই অক্ষর (a-z, A-Z) বা আন্ডারস্কোর (_) দিয়ে শুরু হতে হবে** [[23]]
2. **নামে শুধুমাত্র অক্ষর, সংখ্যা (0-9) এবং আন্ডারস্কোর (_) থাকতে পারবে** [[23]]
3. **নামে কোনো স্পেস (ফাঁকা স্থান) থাকতে পারবে না** [[23]]
4. **C ভাষার কীওয়ার্ড (keyword) ভেরিয়েবল নাম হিসেবে ব্যবহার করা যাবে না** (যেমন: int, float, if, else, while ইত্যাদি) [[17]]
5. **ভেরিয়েবল নাম Case-Sensitive** (age, Age, AGE - তিনটি ভিন্ন ভেরিয়েবল)

### সঠিক উদাহরণ:
```c
int age;
float salary;
char initial;
int _count;
float salary2024;
char student_name;
```

### ভুল উদাহরণ:
```c
int 1st_number;      // ভুল: সংখ্যা দিয়ে শুরু হয়েছে
float my variable;   // ভুল: স্পেস আছে
char @symbol;        // ভুল: বিশেষ চিহ্ন ব্যবহার করা হয়েছে
int if;              // ভুল: কীওয়ার্ড ব্যবহার করা হয়েছে
```

### নামকরণের কনভেনশন (ঐচ্ছিক কিন্তু ভালো অভ্যাস):

1. **Snake Case** (ছোট হাতের অক্ষর ও আন্ডারস্কোর):
```c
int student_age;
float total_salary;
char first_name;
```

2. **Camel Case** (প্রথম শব্দ ছোট, পরের শব্দের প্রথম অক্ষর বড়):
```c
int studentAge;
float totalSalary;
char firstName;
```

3. **ধারাবাহিকতা বজায় রাখা**:
```c
// ভালো
int num1, num2, num3;
float salary1, salary2;

// খারাপ
int number_one, num2, n3;
```

4. **অর্থবহ নাম ব্যবহার**:
```c
// ভালো
int age;
float salary;
char grade;

// খারাপ
int a;
float x;
char z;
```

### পূর্ণাঙ্গ উদাহরণ:

```c
#include <stdio.h>

int main() {
    // ভালো নামকরণ
    int student_age = 20;
    float monthly_salary = 25000.50;
    char student_name[] = "Rahim";
    
    printf("নাম: %s\n", student_name);
    printf("বয়স: %d\n", student_age);
    printf("বেতন: %.2f\n", monthly_salary);
    
    return 0;
}
```

---

## **Class 4: ডেটা টাইপ (Data Types in C)**

### ডেটা টাইপ কী?
ডেটা টাইপ নির্ধারণ করে যে একটি ভেরিয়েবল কী ধরনের ডেটা সংরক্ষণ করবে এবং কতটুকু মেমোরি নেবে [[1]]।

### মৌলিক ডেটা টাইপ:

#### ১. **int (পূর্ণসংখ্যা)**
- পূর্ণসংখ্যা সংরক্ষণ করে (ধনাত্মক, ঋণাত্মক, শূন্য)
- সাধারণত ৪ বাইট মেমোরি নেয়
- রেঞ্জ: -২,১৪৭,৪৮৩,৬৪৮ থেকে ২,১৪৭,৪৮৩,৬৪৭

```c
#include <stdio.h>

int main() {
    int age = 25;
    int temperature = -5;
    int count = 0;
    
    printf("বয়স: %d\n", age);
    printf("তাপমাত্রা: %d\n", temperature);
    printf("গণনা: %d\n", count);
    
    return 0;
}
```

#### ২. **float (দশমিক সংখ্যা)**
- দশমিক সংখ্যা সংরক্ষণ করে
- ৪ বাইট মেমোরি নেয়
- ৬-৭টি দশমিক স্থান পর্যন্ত নির্ভুল

```c
#include <stdio.h>

int main() {
    float price = 99.99;
    float height = 5.8;
    float pi = 3.14159;
    
    printf("দাম: %.2f\n", price);
    printf("উচ্চতা: %.1f\n", height);
    printf("পাই: %f\n", pi);
    
    return 0;
}
```

#### ৩. **double (বড় দশমিক সংখ্যা)**
- বড় দশমিক সংখ্যা সংরক্ষণ করে
- ৮ বাইট মেমোরি নেয়
- ১৪-১৫টি দশমিক স্থান পর্যন্ত নির্ভুল

```c
#include <stdio.h>

int main() {
    double large_number = 123456.789012345;
    double scientific = 6.022e23;
    
    printf("বড় সংখ্যা: %.5f\n", large_number);
    printf("বৈজ্ঞানিক: %e\n", scientific);
    
    return 0;
}
```

#### ৪. **char (অক্ষর)**
- একটি অক্ষর সংরক্ষণ করে
- ১ বাইট মেমোরি নেয়
- একক উদ্ধৃতি চিহ্ন (' ') ব্যবহার করতে হয়

```c
#include <stdio.h>

int main() {
    char grade = 'A';
    char initial = 'R';
    char symbol = '$';
    
    printf("গ্রেড: %c\n", grade);
    printf("প্রথম অক্ষর: %c\n", initial);
    printf("প্রতীক: %c\n", symbol);
    
    return 0;
}
```

### মডифায়ার (Modifiers):

```c
#include <stdio.h>
#include <limits.h>

int main() {
    // signed (চিহ্নযুক্ত)
    signed int num1 = -100;
    
    // unsigned (চিহ্নহীন - শুধু ধনাত্মক)
    unsigned int num2 = 100;
    
    // short (ছোট)
    short int small = 100;
    
    // long (বড়)
    long int large = 100000L;
    
    printf("Signed: %d\n", num1);
    printf("Unsigned: %u\n", num2);
    printf("Short: %d\n", small);
    printf("Long: %ld\n", large);
    
    return 0;
}
```

### ফরম্যাট স্পেসিফায়ার (Format Specifiers):

| ডেটা টাইপ | ফরম্যাট স্পেসিফায়ার |
|-----------|-------------------|
| int | %d বা %i |
| float | %f |
| double | %lf |
| char | %c |
| string | %s |
| unsigned int | %u |
| long int | %ld |
| short int | %hd |

### পূর্ণাঙ্গ উদাহরণ:

```c
#include <stdio.h>

int main() {
    // বিভিন্ন ডেটা টাইপের ব্যবহার
    int age = 25;
    float weight = 65.5;
    double salary = 50000.75;
    char grade = 'A';
    char name[] = "Rahim";
    
    printf("=== ছাত্রের তথ্য ===\n");
    printf("নাম: %s\n", name);
    printf("বয়স: %d বছর\n", age);
    printf("ওজন: %.2f কেজি\n", weight);
    printf("বেতন: %.2f টাকা\n", salary);
    printf("গ্রেড: %c\n", grade);
    
    return 0;
}
```

### আউটপুট:
```
=== ছাত্রের তথ্য ===
নাম: Rahim
বয়স: 25 বছর
ওজন: 65.50 কেজি
বেতন: 50000.75 টাকা
গ্রেড: A
```

---

## **Class 5: টাইপ কনভারশন (Type Conversion in C)**

### টাইপ কনভারশন কী?
একটি ডেটা টাইপ থেকে অন্য ডেটা টাইপে রূপান্তর করাকে টাইপ কনভারশন বলে।

### দুই প্রকার টাইপ কনভারশন:

#### ১. **Implicit Type Conversion (স্বয়ংক্রিয়)**
কম্পাইলার স্বয়ংক্রিয়ভাবে ছোট ডেটা টাইপ থেকে বড় ডেটা টাইপে রূপান্তর করে।

```c
#include <stdio.h>

int main() {
    int num1 = 10;
    double num2 = 5.5;
    double result;
    
    // int automatically converts to double
    result = num1 + num2;
    
    printf("num1 (int): %d\n", num1);
    printf("num2 (double): %.2f\n", num2);
    printf("result: %.2f\n", result);
    
    return 0;
}
```

**আউটপুট:**
```
num1 (int): 10
num2 (double): 5.50
result: 15.50
```

#### ২. **Explicit Type Conversion (জোরপূর্বক/Casting)**
প্রোগ্রামার জোর করে এক ডেটা টাইপ থেকে অন্য ডেটা টাইপে রূপান্তর করে।

```c
#include <stdio.h>

int main() {
    double num1 = 10.75;
    int num2;
    
    // Explicit conversion (casting)
    num2 = (int)num1;
    
    printf("Original: %.2f\n", num1);
    printf("After casting: %d\n", num2);
    
    return 0;
}
```

**আউটপুট:**
```
Original: 10.75
After casting: 10
```

### টাইপ কনভারশনের উদাহরণ:

```c
#include <stdio.h>

int main() {
    // উদাহরণ ১: Integer Division
    int a = 10;
    int b = 3;
    double result1 = a / b;  // 3.00 হবে (ভুল!)
    double result2 = (double)a / b;  // 3.33 হবে (সঠিক!)
    
    printf("ভুল ফলাফল: %.2f\n", result1);
    printf("সঠিক ফলাফল: %.2f\n", result2);
    
    // উদাহরণ ২: Char to Int
    char ch = 'A';
    int ascii = (int)ch;
    
    printf("\nঅক্ষর: %c\n", ch);
    printf("ASCII মান: %d\n", ascii);
    
    // উদাহরণ ৩: Float to Int
    float price = 99.99;
    int whole_price = (int)price;
    
    printf("\nআসল দাম: %.2f\n", price);
    printf("পূর্ণসংখ্যা দাম: %d\n", whole_price);
    
    return 0;
}
```

### আউটপুট:
```
ভুল ফলাফল: 3.00
সঠিক ফলাফল: 3.33

অক্ষর: A
ASCII মান: 65

আসল দাম: 99.99
পূর্ণসংখ্যা দাম: 99
```

### গাণিতিক উদাহরণ:

```c
#include <stdio.h>

int main() {
    int num1 = 15;
    int num2 = 4;
    
    // বিভিন্ন ধরনের বিভাজন
    printf("Integer division: %d\n", num1 / num2);  // 3
    printf("Float division: %.2f\n", (float)num1 / num2);  // 3.75
    printf("Double division: %.4f\n", (double)num1 / num2);  // 3.7500
    
    return 0;
}
```

---

## **Class 6: ইনপুট - পর্ব ১ (Input Part 1)**

### scanf() ফাংশন
`scanf()` ফাংশন ব্যবহার করে ব্যবহারকারীর কাছ থেকে ইনপুট নেওয়া যায় [[14]]।

### বেসিক সিনট্যাক্স:
```c
scanf("format_specifier", &variable_name);
```

**গুরুত্বপূর্ণ:** ভেরিয়েবলের আগে `&` (address of operator) ব্যবহার করতে হয়

### ইনপুট নেওয়ার উদাহরণ:

```c
#include <stdio.h>

int main() {
    int age;
    
    printf("আপনার বয়স কত? ");
    scanf("%d", &age);
    
    printf("আপনার বয়স: %d বছর\n", age);
    
    return 0;
}
```

### একাধিক ইনপুট:

```c
#include <stdio.h>

int main() {
    int num1, num2;
    int sum;
    
    printf("প্রথম সংখ্যা: ");
    scanf("%d", &num1);
    
    printf("দ্বিতীয় সংখ্যা: ");
    scanf("%d", &num2);
    
    sum = num1 + num2;
    
    printf("%d + %d = %d\n", num1, num2, sum);
    
    return 0;
}
```

### বিভিন্ন ডেটা টাইপের ইনপুট:

```c
#include <stdio.h>

int main() {
    int age;
    float height;
    double salary;
    char grade;
    
    printf("বয়স: ");
    scanf("%d", &age);
    
    printf("উচ্চতা (মিটার): ");
    scanf("%f", &height);
    
    printf("বেতন: ");
    scanf("%lf", &salary);
    
    printf("গ্রেড: ");
    scanf(" %c", &grade);  // %c এর আগে স্পেস দিতে হয়
    
    printf("\n=== আপনার তথ্য ===\n");
    printf("বয়স: %d বছর\n", age);
    printf("উচ্চতা: %.2f মিটার\n", height);
    printf("বেতন: %.2f টাকা\n", salary);
    printf("গ্রেড: %c\n", grade);
    
    return 0;
}
```

### ক্যালকুলেটর প্রোগ্রাম:

```c
#include <stdio.h>

int main() {
    int num1, num2;
    int sum, diff, product;
    float division;
    
    printf("প্রথম সংখ্যা: ");
    scanf("%d", &num1);
    
    printf("দ্বিতীয় সংখ্যা: ");
    scanf("%d", &num2);
    
    sum = num1 + num2;
    diff = num1 - num2;
    product = num1 * num2;
    division = (float)num1 / num2;
    
    printf("\n=== ফলাফল ===\n");
    printf("যোগ: %d + %d = %d\n", num1, num2, sum);
    printf("বিয়োগ: %d - %d = %d\n", num1, num2, diff);
    printf("গুণ: %d × %d = %d\n", num1, num2, product);
    printf("ভাগ: %d ÷ %d = %.2f\n", num1, num2, division);
    
    return 0;
}
```

---

## **Class 7: ইনপুট - পর্ব ২ (Input Part 2)**

### একাধিক ভেরিয়েবলে একসাথে ইনপুট:

```c
#include <stdio.h>

int main() {
    int num1, num2, num3;
    
    printf("তিনটি সংখ্যা দিন (স্পেস দিয়ে আলাদা করুন): ");
    scanf("%d %d %d", &num1, &num2, &num3);
    
    printf("আপনি দিয়েছেন:\n");
    printf("num1 = %d\n", num1);
    printf("num2 = %d\n", num2);
    printf("num3 = %d\n", num3);
    
    return 0;
}
```

### স্ট্রিং ইনপুট:

```c
#include <stdio.h>

int main() {
    char name[50];
    
    printf("আপনার নাম: ");
    scanf("%s", name);  // স্ট্রিং এর জন্য & লাগে না
    
    printf("আপনার নাম: %s\n", name);
    
    return 0;
}
```

**সতর্কতা:** `scanf("%s")` শুধু প্রথম শব্দ পর্যন্ত নেয় (স্পেসের আগ পর্যন্ত)

### পূর্ণ নাম নেওয়ার উপায়:

```c
#include <stdio.h>

int main() {
    char fullName[100];
    
    printf("আপনার পূর্ণ নাম: ");
    scanf(" %[^\n]", fullName);  // পুরো লাইন নেবে
    
    printf("আপনার নাম: %s\n", fullName);
    
    return 0;
}
```

### বাস্তব উদাহরণ - ছাত্রের তথ্য:

```c
#include <stdio.h>

int main() {
    char name[50];
    int roll, age;
    float gpa;
    
    printf("=== ছাত্রের তথ্য ===\n\n");
    
    printf("নাম: ");
    scanf(" %[^\n]", name);
    
    printf("রোল নম্বর: ");
    scanf("%d", &roll);
    
    printf("বয়স: ");
    scanf("%d", &age);
    
    printf("GPA: ");
    scanf("%f", &gpa);
    
    printf("\n=== সংরক্ষিত তথ্য ===\n");
    printf("নাম: %s\n", name);
    printf("রোল: %d\n", roll);
    printf("বয়স: %d বছর\n", age);
    printf("GPA: %.2f\n", gpa);
    
    return 0;
}
```

### ইনপুট ভ্যালিডেশন:

```c
#include <stdio.h>

int main() {
    int number;
    
    printf("১ থেকে ১০০ এর মধ্যে একটি সংখ্যা দিন: ");
    scanf("%d", &number);
    
    if(number >= 1 && number <= 100) {
        printf("আপনি দিয়েছেন: %d\n", number);
    } else {
        printf("ভুল! সংখ্যা ১ থেকে ১০০ এর মধ্যে হতে হবে\n");
    }
    
    return 0;
}
```

### গড় নির্ণয়ের প্রোগ্রাম:

```c
#include <stdio.h>

int main() {
    float mark1, mark2, mark3, mark4, mark5;
    float total, average;
    
    printf("=== ছাত্রের নম্বর ===\n");
    
    printf("বাংলা: ");
    scanf("%f", &mark1);
    
    printf("ইংরেজি: ");
    scanf("%f", &mark2);
    
    printf("গণিত: ");
    scanf("%f", &mark3);
    
    printf("বিজ্ঞান: ");
    scanf("%f", &mark4);
    
    printf("সামাজিক বিজ্ঞান: ");
    scanf("%f", &mark5);
    
    total = mark1 + mark2 + mark3 + mark4 + mark5;
    average = total / 5;
    
    printf("\n=== ফলাফল ===\n");
    printf("মোট নম্বর: %.2f\n", total);
    printf("গড় নম্বর: %.2f\n", average);
    
    if(average >= 80) {
        printf("গ্রেড: A+\n");
    } else if(average >= 70) {
        printf("গ্রেড: A\n");
    } else if(average >= 60) {
        printf("গ্রেড: A-\n");
    } else if(average >= 50) {
        printf("গ্রেড: B\n");
    } else {
        printf("গ্রেড: F\n");
    }
    
    return 0;
}
```

---

## **গুরুত্বপূর্ণ টিপস:**

### ১. **scanf() ব্যবহারের সতর্কতা:**
- সবসময় ভেরিয়েবলের আগে `&` ব্যবহার করুন (string ছাড়া)
- সঠিক format specifier ব্যবহার করুন
- `%c` ব্যবহারের আগে স্পেস দিন: `scanf(" %c", &ch)`

### ২. **ভেরিয়েবল ঘোষণা:**
- ব্যবহারের আগে অবশ্যই ঘোষণা করুন
- অর্থবহ নাম দিন
- প্রয়োজনীয় ডেটা টাইপ ব্যবহার করুন

### ৩. **কোড লেখার ভালো অভ্যাস:**
- প্রতিটি লাইনের শেষে সেমিকোলন (;) দিন
- কোডকে সুন্দরভাবে indent করুন
- মন্তব্য (comment) যুক্ত করুন

### ৪. **সাধারণ ত্রুটি:**
```c
// ভুল
scanf("%d", age);        // & missing
scanf("%d", &age)        // ; missing
int 1number;             // সংখ্যা দিয়ে শুরু

// সঠিক
scanf("%d", &age);
int number1;
```

---

## **সম্পূর্ণ প্রোগ্রাম উদাহরণ:**

```c
#include <stdio.h>

int main() {
    // ভেরিয়েবল ঘোষণা
    char studentName[50];
    int roll, age;
    float mark1, mark2, mark3, total, average;
    
    // ইনপুট
    printf("ছাত্রের নাম: ");
    scanf(" %[^\n]", studentName);
    
    printf("রোল নম্বর: ");
    scanf("%d", &roll);
    
    printf("বয়স: ");
    scanf("%d", &age);
    
    printf("তিনটি বিষয়ের নম্বর: ");
    scanf("%f %f %f", &mark1, &mark2, &mark3);
    
    // গণনা
    total = mark1 + mark2 + mark3;
    average = total / 3;
    
    // আউটপুট
    printf("\n=== রেজাল্ট শিট ===\n");
    printf("নাম: %s\n", studentName);
    printf("রোল: %d\n", roll);
    printf("বয়স: %d\n", age);
    printf("মোট নম্বর: %.2f/300\n", total);
    printf("গড়: %.2f\n", average);
    
    return 0;
}
```

---

এই নোটগুলো সি প্রোগ্রামিং শেখার জন্য একটি শক্ত ভিত্তি তৈরি করবে। প্রতিটি টপিকের উদাহরণগুলো নিজে লিখে রান করে দেখুন। প্রশ্ন থাকলে অনুশীলন করুন এবং বিভিন্ন পরিবর্তন করে দেখুন কী হয়!

**শুভকামনা!** 🎓
