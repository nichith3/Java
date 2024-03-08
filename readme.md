# Java CheatSheet

## Getting Started
```java
public class Hello {
  // main method
  public static void main(String[] args)
  {
    // Output: Hello, world!
    System.out.println("Hello, world!");
  }
}
```

#### Compiling and running
```
$ javac Hello.java
$ java Hello
Hello, world!
```

### Variables
```java
int num = 5;
float floatNum = 5.99f;
char ch = 'A';
boolean bool = true;
String s1 = "This is Java";
```

### Primitive Data Types
| Data Type | Size   | Default | Range           |
| --------- | ------ | ------- | --------------- |
| `byte`    | 1 byte | 0       | \-128 to 127    |
| `short`   | 2 byte | 0       | \-215 to 215\-1 |
| `int`     | 4 byte | 0       | \-231 to 231\-1 |
| `long`    | 8 byte | 0       | \-263 to 263\-1 |
| `float`   | 4 byte | 0.0f    | N/A             |
| `double`  | 8 byte | 0.0d    | N/A             |
| `char`    | 2 byte | \\u0000 | 0 to 65535      |
| `boolean` | N/A    | false   | true / false    |


### String
```java
String first = "coding";
String last = "language";
String word = first + " " + last;
System.out.println(word);
```

### Loops
```java
String word = "java";
for (char c: word.toCharArray()) {
  System.out.print(c + "-");
}
// Outputs: j-a-v-a-

```

### Array
```java
char[] chars = new char[10];
chars[0] = 'a'
chars[1] = 'b'

String[] letters = {"A", "B", "C"};
int[] mylist = {100, 200};
boolean[] answers = {true, false};
```

### Swap
```java
int a = 1;
int b = 2;
System.out.println(a + " " + b); // 1 2

int temp = a;
a = b;
b = temp;
System.out.println(a + " " + b); // 2 1
```

### Conditional
```java
int j = 10;

if (j == 10) {
  System.out.println("I get printed");
} else if (j > 10) {
  System.out.println("I don't");
} else {
  System.out.println("I also don't");
}
```

## Operators

#### 1. Arithmetic Operator
| Operator | Desc                |
|----------|---------------------|
| +        | addition            |
| -        | Subtraction         |
| *        | Multiplication      |
| /        | Division - Quotient |
| %        | Modulo - Remainder  |
| + +      | Increment           |
| - -      | Decremennt          |

#### 2. Relational Operator
| Symbol | Desc                  |
|--------|-----------------------|
| ==     | Equal to              |
| !=     | Not Equals to         |
| >      | Greater than          |
| >=     | Greater than or equal |
| <      | less than             |
| <=     | Less than or equal    |

#### 3. Bitwise Operator
| Operator | Name               | Example  | Result |
|----------|--------------------|----------|--------|
| &        | Bitwise AND        | 6 & 3    | 2      |
| \|       | Bitwise OR         | 10 \| 10 | 10     |
| ^        | Bitwise XOR        | 2 ^ 2    | 0      |
| ~        | Bitwise complement | ~ 9      | -10    |
| <<       | Left shift         | 10<<2    | 40     |
| >>       | Right Shift        | 10>>2    | 2      |

#### 4. Assignment Operator
| Operator | Example | Result |
|----------|---------|--------|
| + =      | a+=b    | a=a+b  |
| - =      | a-=b    | a=a-b  |
| * =      | a*=b    | a=a*b  |
| / =      | a/=b    | a=a/b  |
| % =      | a%=b    | a=a%b  |

#### 5. Logical Operator
| Operator | Desc                                |
|----------|-------------------------------------|
| &&       | return true if both are true        |
| \|\|     | returns true if atleast one is true |
| !        | returns true if false & vice versa  |

### TypeCasting
```java
// Widening
// byte<short<int<long<float<double
int i = 10;
long l = i;               // 10

// Narrowing 
double d = 10.02;
long l = (long)d;         // 10

String.valueOf(10);       // "10"
Integer.parseInt("10");   // 10
Double.parseDouble("10"); // 10.0
```


### User Input
```java
Scanner sc = new Scanner(System.in);
String sentence = sc.nextLine();
System.out.println(sentence);

int num1 = sc.nextInt();

String word = sc.next();
float num2 = sc.nextFloat();
double num3 = sc.nextDouble();
boolean bool = sc.nextBoolean();
long num4 = sc.nextLong();
short num5 = sc.nextShort();
byte num6 = sc.nextByte();

```

## Strings

#### Basics
```java
String str1 = "value"; 
String str2 = new String("value");
String str3 = String.valueOf(123);
```

#### Concatenations
```java
String s = 3 + "str" + 3;     // 3str3
String s = 3 + 3 + "str";     // 6str
String s = "3" + 3 + "str";   // 33str
String s = "3" + "3" + "23";  // 3323
String s = "" + 3 + 3 + "23"; // 3323
String s = 3 + 3 + 23;        // 29

'a' + 'b'          // 195
"a" + "b"          // "ab"
'a' + 1           // 98
(char)('a'+1)     // 'b'
"a" + 1           // "a1"
```

#### Comparison
```java
String s1 = new String("coding"); 
String s2 = new String("coding"); 

s1 == s2          // false
s1.equals(s2)     // true

"AB".equalsIgnoreCase("ab")  // true
```

#### Manipulation
```java
String str = "Abcd";

str.toUpperCase();     // ABCD
str.toLowerCase();     // abcd
str.concat("#");       // Abcd#
str.replace("b", "-"); // A-cd

"  abc ".trim();       // abc
"ab".toCharArray();    // {'a', 'b'}
```

#### Information
```java
String str = "abcd";

str.length();        // 4
str.charAt(2);       // c

str.isEmpty();       // false
str.indexOf("a")     // 0
str.indexOf("z")     // -1
str.toString();      // abcd
str.substring(2);    // cd
str.substring(2,3);  // c
str.contains("c");   // true
str.endsWith("d");   // true
str.startsWith("a"); // true
```

#### Immutable
```java
String str = "hello";
str.concat("world");

// Outputs: hello
System.out.println(str);
```
---
```java
String str = "hello";
String concat = str.concat("world");

// Outputs: helloworld
System.out.println(concat);
```


### String Builder
```java
StringBuilder sb = new StringBuilder("Coding");
// create sb with string coding

StringBuilder sb1 = new StringBuilder(10);
// create sb1 with length 10

StringBuilder sb2 = new StringBuilder();

sb.length();
sb.charAt(1);
sb.append("Language");
sb.insert(0, "My ");
sb.delete(0, 2); //(include, exclude)
sb.setcharAt(3, 'e');
```

#### System.out.println
```java
System.out.println ("Str" + new ArrayList<>());	
// Output : Str[]

System.out.println(new Integer(39) + new ArrayList<>());
// Output : Error
// Because no String is included

System.out.println(new Integer(39) + "" + new ArrayList<>())
// Output : 39[]
```


## Arrays
#### Declare
```java
int[] a1;
int[] a2 = {1, 2, 3};
int[] a3 = new int[]{1, 2, 3};

int[] a4 = new int[3];
a4[0] = 1;
a4[2] = 2;
a4[3] = 3;
```

#### Modify
```java
int[] a = {1, 2, 3};
System.out.println(a[0]); // 1

a[0] = 9;
System.out.println(a[0]); // 9

System.out.println(a.length); // 3
```

#### Loop 
```java
String[] arr = {"a", "b", "c"};
for (int a: arr) {
    System.out.print(a + " ");
}
// Outputs: a b c 
```

#### Multidimensional Array
```java
int[][] matrix = { {1, 2, 3}, {4, 5} };

int x = matrix[1][0];  // 4

// [[1, 2, 3], [4, 5]]
Arrays.deepToString(matrix)
// toString doesn't word for multidimensional

int rows = matrix.length;
int cols = matrix[0].length;

for (int i = 0; i < rows; ++i) {
  for(int j = 0; j < cols; ++j) {
    System.out.println(a[i][j]);
  }
}
// Outputs: 1 2 3 4 5 6 7 

```

#### Methods
```java
int[] nums = {1, 2, 3};
System.out.println(Arrays.toString(nums))
// [1, 2, 3]

char[] chars = {'b', 'a', 'c'};
Arrays.sort(chars);      // [a, b, c]

int[] arr = {42, 73, 98, 21}
int len = arr.length;    // 4

int[] original = {1, 2, 3};
int[] copy = Arrays.copyOf(original, original.length); 
// [1, 2, 3]


int[] array1 = {1, 2, 3};
int[] array2 = {1, 2, 3};
boolean isEqual = Arrays.equals(array1, array2);
// true

```


## Conditional
#### Ternary Operator
```java
int a = 10;
int b = 20;
int max = (a > b) ? a : b;

// Outputs: 20
System.out.println(max);
```

#### Switch
```java
int month = 3;
String str;
switch (month) {
  case 1:
    str = "January";
    break;
  case 2:
    str = "February";
    break;
  case 3:
    str = "March";
    break;
  default:
    str = "Some other month";
    break;
}

// Outputs: Result March
System.out.println("Result " + str);
```

#### Switch - Improved
```java
switch (x) {
    case 1 -> {
        System.out.println("One");
        System.out.println("One again");
    }
    case 2 -> System.out.println("Two");
    default -> System.out.println("Unknown");
}
```

## Loops
#### For Loop
```java
for (int i = 0; i < 10; i++) {
  System.out.print(i);
}
// Outputs: 0123456789
```

#### Enchanced forLoop
```java
int[] numbers = {1,2,3,4,5};

for (int number: numbers) {
  System.out.print(number);
}
// Outputs: 12345
```

#### While Loop
```java
int count = 0;

while (count < 5) {
  System.out.print(count);
  count++;
}
// Outputs: 01234
```

#### Do while
```java
int count = 0;

do {
  System.out.print(count);
  count++;
} while (count < 5);
// Outputs: 01234
```

#### Continue Statement
```java
for (int i = 0; i < 5; i++) {
  if (i == 3) {
    continue;
  }
  System.out.print(i);
}
// Outputs: 01245
```

#### Break Statement
```java
for (int i = 0; i < 5; i++) {
  System.out.print(i);
  if (i == 3) {
    break;
  }
}
// Outputs: 0123
```


## Misc

#### Comment
```java
// I am a single line comment!
 
/*
And I am a 
multi-line comment!
*/

/**
 * This  
 * is  
 * documentation  
 * comment 
 */
```

#### Keywords
| Keywords  |          |            |            |              |
|-----------|----------|------------|------------|--------------|
| abstract  | continue | for        | new        | switch       |
| assert*** | default  | goto*      | package    | synchronized |
| boolean   | do       | if         | private    | this         |
| break     | double   | implements | protected  | throw        |
| byte      | else     | import     | public     | throws       |
| case      | enum**** | instanceof | return     | transient    |
| catch     | extends  | int        | short      | try          |
| char      | final    | interface  | static     | void         |
| class     | finally  | long       | strictfp** | volatile     |
| const*    | float    | native     | super      | while        |


### Math function
| Function      | Desc               |
|---------------|--------------------|
| Math.max(a,b) | Maximum of a and b |
| Math.min(a,b) | Minimum of a and b |
| Math.abs(a)   | Absolute value a   |
| Math.sqrt(a)  | Square-root of a   |
| Math.pow(a,b) | Power of b         |
| Math.round(a) | Closest integer    |
| Math.PI       | Gives PI Value     |

```java
// ceil --> rounds to upper
Math.ceil(3.24) // 4.0
Math.ceil(3.7) // 4.0

// round --> equal or greater than 5
Math.round(1.878)  // 2
Math.round(1.5)    // 2
Math.round(1.34)   // 1

// floor --> rounds to lower 
Math.ceil(1.878)    // 1
Math.ceil(1.3)      // 1
```


#### Random number between 2 Numbers
```java
Math.floor(Math.random() * ((max-min)+1) + min);
```

#### Minimum & Maximum
```java
System.out.print(Integer.MAX_VALUE) //2147483647

System.out.println(Integer.MIN_VALUE) //-2147483648

```

#### Convert String to Char Array
```java
char[] ch = str.toCharArray();
```

#### Convert Char Array to String
```java
char[] charArr = new char[10];

// method 1
String s1 = new String(charArr);

// method 2
String s2 = String.valueOf(charArr);

// method 3
String s3 = String.copyValueOf(charArr);
```

#### Split String
```java
String s = "Java programming";
String arr[] = s.split(" ");
// Output : ["Java", "programming"]
```

#### Input Single Character
```java
char chr = sc.next().charAt(0);  
```

#### ASCII values
```java
a - 65 to z - 90
A - 97 to Z - 122

int num1 = 'a';   // 65
char ch1 = 66;    // 'b'

char num2 = 'Z';
int ch2 = (int)num2;  // 122

int num3 = 97;
char ch3 = (char)num3;  // 'A'
```

---

### Formatted Output

```java
double num = 843.7395232;
System.out.println (num);
System.out.println (String.format ("%.2f", num));
```

####  Formatting Using Printf()
```java
System.out.printf("%d%n",a); 		// 42

double a = 3.14159265359; 
System.out.printf("%f\n", a); 		// "3.141593"
System.out.printf("%5.3f\n", a); 	// "3.142"

// total 5 characters after decimal 2 digits
System.out.printf("%5.2f\n", a); 	// " 3.14"

Boolean b = true;
c = false;
Integer d = null;
System.out.printf("%b\n", a); 	// true
System.out.printf("%B\n", b); 	// TRUE
System.out.printf("%b\n", c); 	// false
System.out.printf("%B\n", d); 	// FALSE

char c = 'g'; 
System.out.printf("%c\n", c); 	// g
System.out.printf("%C\n", c); 	// G

String str = "java"; 
System.out.printf("%s \n", str); 	// java
System.out.printf("%S \n", str); 	// JAVA

System.out.printf("%h\n",42);   // any type to hexa
System.out.printf("%o\n",42);   // integer to octal
System.out.printf("%x\n",42);   // integer to hexa
```

####  Fromat Using DecimalFormat class
```java
// import java.text.DecimalFormat;

double num = 123.4567; 

DecimalFormat ft = new DecimalFormat("####");      
System.out.println("Without fraction part: "+ ft.format(num));
//	Output : 123 

ft = new DecimalFormat("#.##");       
System.out.println("Formatted to precision:" + ft.format(num)); 
// Output : 123.46

ft = new DecimalFormat("#.000000"); 
System.out.println("appended zeroes to right: "+ ft.format(num)); 
// Output : 123.456700

ft = new DecimalFormat("00000.00"); 
System.out.println("formatting Numeric part : " + ft.format(num)); 
// Output : 00123.46

double income = 23456.789;       
ft = new DecimalFormat("$###,###.##"); 
System.out.println("your Formatted Income : "+ ft.format(income)); 
// Output : $23,456.79
```
