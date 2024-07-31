# string_in_python
### السلاسل النصية (Strings) 

#### تعريف السلاسل النصية

السلاسل النصية هي نوع من البيانات يُستخدم لتمثيل النصوص. في بايثون، يتم تمثيل السلاسل النصية باستخدام علامات الاقتباس المفردة (' ') أو المزدوجة (" "). يمكن أن تحتوي السلاسل النصية على حروف، أرقام، مسافات، وأي رموز أخرى.

مثال:
```python
single_quote_string = 'Hello, World!'
double_quote_string = "Hello, World!"
```

#### التعامل مع السلاسل النصية

##### السلاسل النصية المتعددة الأسطر (Multiline Strings)

يمكن تعريف السلاسل النصية المتعددة الأسطر باستخدام ثلاثة علامات اقتباس مفردة أو مزدوجة.

مثال:
```python
multi_line_string = '''This is
a multi-line
string.'''
print(multi_line_string)

another_multi_line_string = """This is
another multi-line
string."""
print(another_multi_line_string)
```

##### استخدام علامات الاقتباس داخل النصوص (Quotation Marks in Strings)

يمكنك استخدام علامات الاقتباس داخل النصوص طالما أنها لا تطابق علامات الاقتباس المحيطة بالنص. هنا بعض الطرق لإدراج علامات الاقتباس داخل النصوص:

1. **استخدام علامات الاقتباس المزدوجة داخل علامات اقتباس مفردة:**
إذا كنت تستخدم علامات الاقتباس المفردة لتحديد النص، يمكنك استخدام علامات الاقتباس المزدوجة داخل النص بدون الحاجة إلى الهروب:
```python
print('He is called "Johnny"')
# الإخراج: He is called "Johnny"
```

2. **استخدام علامات الاقتباس المفردة داخل علامات اقتباس مزدوجة:**
إذا كنت تستخدم علامات الاقتباس المزدوجة لتحديد النص، يمكنك استخدام علامات الاقتباس المفردة داخل النص بدون الحاجة إلى الهروب:
```python
print("It's alright")
# الإخراج: It's alright
```

3. **استخدام نفس نوع علامات الاقتباس داخل النص مع الهروب:**
إذا كنت بحاجة لاستخدام نفس نوع علامات الاقتباس داخل النص، يمكنك استخدام الهروب باستخدام شريط العكس (\):
```python
print('He is called \'Johnny\'')
print("It's alright")
# الإخراج:
# He is called 'Johnny'
# It's alright
```

4. **استخدام علامات اقتباس مزدوجة ومفردة بداخل بعضهما:**
يمكنك أيضاً دمج علامات الاقتباس المزدوجة والمفردة في نفس النص:
```python
print("He said, 'She said, \"It's alright.\"'")
# الإخراج: He said, 'She said, "It's alright."'
```

### السلاسل النصية كصفائف (Strings as Arrays)

في بايثون، تُعتبر السلاسل النصية صفائف من البايتات التي تمثل أحرف اليونيكود. لا يوجد نوع بيانات خاص بالحروف في بايثون؛ الحرف الواحد هو سلسلة نصية بطول 1. يمكنك استخدام الأقواس المربعة للوصول إلى عناصر السلسلة النصية مباشرة.

#### مثال: الحصول على الحرف في الموضع 1 (تذكر أن الموضع الأول يبدأ من 0)
```python
a = "Hello, World!"
print(a[1])  # النتيجة: "e"
```

### التكرار عبر السلسلة النصية (Looping Through a String)

نظرًا لأن السلاسل النصية هي صفائف، يمكنك استخدام حلقة `for` للتكرار عبر الأحرف في السلسلة النصية.

#### مثال: التكرار عبر الأحرف في كلمة "banana"
```python
for x in "banana":
    print(x)
```

### طول السلسلة النصية (String Length)

يمكنك استخدام دالة `len()` للحصول على طول السلسلة النصية.

#### مثال: دالة `len()` تعيد طول السلسلة النصية
```python
a = "Hello, World!"
print(len(a))  # النتيجة: 13
```

### التحقق من وجود نص داخل السلسلة النصية (Check String)

للتحقق مما إذا كانت عبارة معينة أو حرف موجود في السلسلة النصية، يمكنك استخدام الكلمة المفتاحية `in`.

#### مثال: التحقق مما إذا كانت كلمة "free" موجودة في النص
```python
txt = "The best things in life are free!"
print("free" in txt)  # النتيجة: True
```

استخدامها في عبارة `if`:
#### مثال: طباعة فقط إذا كانت كلمة "free" موجودة
```python
txt = "The best things in life are free!"
if "free" in txt:
    print("Yes, 'free' is present.")
```

### التحقق من عدم وجود نص داخل السلسلة النصية (Check if NOT)

للتحقق مما إذا كانت عبارة معينة أو حرف غير موجود في السلسلة النصية، يمكنك استخدام الكلمة المفتاحية `not in`.

#### مثال: التحقق مما إذا كانت كلمة "expensive" غير موجودة في النص
```python
txt = "The best things in life are free!"
print("expensive" not in txt)  # النتيجة: True
```

استخدامها في عبارة `if`:
#### مثال: طباعة فقط إذا كانت كلمة "expensive" غير موجودة
```python
txt = "The best things in life are free!"
if "expensive" not in txt:
    print("No, 'expensive' is NOT present.")
```

### معلومات إضافية

#### التعامل مع السلاسل النصية كصفائف
يمكنك الوصول إلى الأحرف الفردية في سلسلة نصية باستخدام فهارس، حيث يبدأ الفهرس من 0.
في بايثون، السلاسل النصية تُعامل كمصفوفات من الأحرف. هذا يعني أنه يمكنك الوصول إلى أحرف فردية في السلسلة باستخدام الفهرسة (indexing). إليك بعض الأمثلة لتوضيح ذلك:


1. الوصول إلى حرف معين:
يمكنك الوصول إلى أي حرف في السلسلة باستخدام رقم الفهرس الخاص به. تذكر أن الفهرسة في بايثون تبدأ من 0.

```python
name = "Python"
print(name[0])  # سيطبع 'P'
print(name[2])  # سيطبع 't'
```


#### مثال: الحصول على الحرف الأول والأخير في السلسلة النصية
```python
a = "Hello, World!"
print(a[0])  # النتيجة: "H"
print(a[-1])  # النتيجة: "!"
```

```
2. الفهرسة السلبية:
يمكنك أيضًا استخدام الفهرسة السلبية للوصول إلى الأحرف بدءًا من نهاية السلسلة.

```python
word = "Hello"
print(word[-1])  # سيطبع 'o'
print(word[-3])  # سيطبع 'l'
```


#### استخدام دالة `len()` للحصول على طول السلسلة النصية
#### مثال
```python
txt = "Python is fun!"
length = len(txt)
print("The length of the string is:", length)  # النتيجة: "The length of the string is: 14"
```

### التحقق من وجود جزء معين في السلسلة النصية باستخدام `in`
#### مثال
```python
sentence = "The quick brown fox jumps over the lazy dog"
word = "fox"
if word in sentence:
    print(f"Yes, '{word}' is present in the sentence.")
else:
    print(f"No, '{word}' is not present in the sentence.")
```

### التحقق من عدم وجود جزء معين في السلسلة النصية باستخدام `not in`
#### مثال
```python
sentence = "The quick brown fox jumps over the lazy dog"
word = "cat"
if word not in sentence:
    print(f"No, '{word}' is not present in the sentence.")
else:
    print(f"Yes, '{word}' is present in the sentence.")

3. تقطيع السلسلة (slicing):
يمكنك استخراج جزء من السلسلة باستخدام التقطيع.

```python
sentence = "Programming is fun"
print(sentence[0:11])  # سيطبع 'Programming'
print(sentence[12:])   # سيطبع 'is fun'
```

4. التكرار على أحرف السلسلة:
يمكنك استخدام حلقة للتكرار على كل حرف في السلسلة.

```python
word = "Python"
for char in word:
    print(char)
# سيطبع:
# P
# y
# t
# h
# o
# n
```

5. الحصول على طول السلسلة:
يمكنك استخدام الدالة `len()` للحصول على طول السلسلة.

```python
text = "Welcome to Python"
print(len(text))  # سيطبع 18
```

6. البحث عن حرف أو سلسلة فرعية:
يمكنك استخدام عامل `in` للتحقق من وجود حرف أو سلسلة فرعية داخل السلسلة الرئيسية.

```python
sentence = "Python is a great language"
print('a' in sentence)  # سيطبع True
print('Java' in sentence)  # سيطبع False
```

من المهم ملاحظة أن السلاسل النصية في بايثون غير قابلة للتغيير (immutable). هذا يعني أنه لا يمكنك تغيير حرف فردي في السلسلة مباشرة. إذا أردت تعديل سلسلة، عليك إنشاء سلسلة جديدة بالتغييرات المطلوبة.

هذه الخصائص تجعل التعامل مع النصوص في بايثون مرنًا وقويًا، مما يسهل العديد من عمليات معالجة النصوص والبيانات. يمكنك استخدام هذه الميزات لتنفيذ مجموعة متنوعة من المهام، مثل تحليل النصوص، استخراج المعلومات، وتنسيق البيانات النصية.


### بايثون - تقطيع السلاسل النصية

#### التقطيع (Slicing)

يمكنك استرجاع جزء من السلسلة النصية باستخدام بناء جملة التقطيع في بايثون. يتم ذلك بتحديد مواضع البداية والنهاية مفصولين بنقطتين (`:`).

#### مثال:
الحصول على الأحرف من الموضع 2 إلى الموضع 5 (الموضع 5 غير مشمول):
```python
b = "Hello, World!"
print(b[2:5])  # النتيجة: "llo"
```
**ملاحظة:** الحرف الأول في السلسلة النصية يبدأ عند الفهرس 0.

#### التقطيع من البداية

يمكنك ترك موضع البداية فارغًا ليبدأ التقطيع من الحرف الأول في السلسلة النصية.
#### مثال:
الحصول على الأحرف من البداية حتى الموضع 5 (الموضع 5 غير مشمول):
```python
b = "Hello, World!"
print(b[:5])  # النتيجة: "Hello"
```

#### التقطيع حتى النهاية

يمكنك ترك موضع النهاية فارغًا ليشمل التقطيع كل الأحرف حتى نهاية السلسلة النصية.
#### مثال:
الحصول على الأحرف من الموضع 2 حتى النهاية:
```python
b = "Hello, World!"
print(b[2:])  # النتيجة: "llo, World!"
```

#### الفهرسة السلبية

يمكنك استخدام الفهارس السلبية لبدء التقطيع من نهاية السلسلة النصية.
#### مثال:
الحصول على الأحرف من "o" في "World!" (الموضع -5) إلى "d" في "World!" (الموضع -2) (غير مشمول):
```python
b = "Hello, World!"
print(b[-5:-2])  # النتيجة: "orl"
```

### بايثون - تعديل السلاسل النصية

تحتوي بايثون على مجموعة من الدوال المدمجة التي يمكن استخدامها مع السلاسل النصية.

#### التحويل إلى الأحرف الكبيرة (Upper Case)
##### مثال:
دالة `upper()` تُعيد السلسلة النصية بأحرف كبيرة:
```python
a = "Hello, World!"
print(a.upper())  # النتيجة: "HELLO, WORLD!"
```

#### التحويل إلى الأحرف الصغيرة (Lower Case)
##### مثال:
دالة `lower()` تُعيد السلسلة النصية بأحرف صغيرة:
```python
a = "Hello, World!"
print(a.lower())  # النتيجة: "hello, world!"
```

#### إزالة الفراغات (Remove Whitespace)
الفراغات هي المسافات التي توجد قبل و/أو بعد النص الفعلي، وغالبًا ما ترغب في إزالتها.
##### مثال:
دالة `strip()` تُزيل أي فراغات من بداية ونهاية السلسلة النصية:
```python
a = " Hello, World! "
print(a.strip())  # النتيجة: "Hello, World!"
```

### دوال أخرى لتعديل السلاسل النصية

#### استبدال جزء من النص (Replace)
##### مثال:
دالة `replace()` تستبدل جزء معين من النص بجزء آخر:
```python
a = "Hello, World!"
print(a.replace("World", "Python"))  # النتيجة: "Hello, Python!"
```

#### تقسيم السلسلة النصية (Split)
##### مثال:
دالة `split()` تقسم السلسلة النصية إلى قائمة من النصوص بناءً على محدد معين:
```python
a = "Hello, World!"
print(a.split(","))  # النتيجة: ['Hello', ' World!']
```

### بايثون - دمج السلاسل النصية

#### دمج السلاسل النصية (String Concatenation)

لدمج، أو جمع، سلسلتين نصيتين يمكنك استخدام معامل الجمع `+`.

##### مثال:
دمج المتغير `a` مع المتغير `b` في المتغير `c`:
```python
a = "Hello"
b = "World"
c = a + b
print(c)  # النتيجة: "HelloWorld"
```

##### مثال:
لإضافة مسافة بين السلسلتين النصيتين، يمكنك إضافة `" "`:
```python
a = "Hello"
b = "World"
c = a + " " + b
print(c)  # النتيجة: "Hello World"
```

### ملاحظات إضافية:
- **يمكنك استخدام نفس الطريقة لدمج أكثر من سلسلتين نصيتين.**
  ```python
  a = "Hello"
  b = "beautiful"
  c = "World"
  result = a + " " + b + " " + c
  print(result)  # النتيجة: "Hello beautiful World"
  ```

- **يمكنك أيضًا دمج النصوص باستخدام معامل `+=` لإضافة نص إلى نهاية متغير موجود:**
  ```python
  a = "Hello"
  a += " World"
  print(a)  # النتيجة: "Hello World"
  ```

- **عند دمج النصوص مع متغيرات من أنواع بيانات مختلفة (مثل الأعداد)، يجب تحويل الأنواع غير النصية إلى نص باستخدام دالة `str()`:**
  ```python
  age = 25
  message = "I am " + str(age) + " years old."
  print(message)  # النتيجة: "I am 25 years old."
  ```

### بايثون - تنسيق السلاسل النصية

#### تنسيق السلاسل النصية

كما تعلمنا في فصل المتغيرات في بايثون، لا يمكننا دمج النصوص والأرقام مباشرةً باستخدام المعامل `+`:
##### مثال:
```python
age = 36
txt = "My name is John, I am " + age
print(txt)  # هذا سيتسبب في خطأ
```

ولكن يمكننا دمج النصوص والأرقام باستخدام F-Strings أو دالة `format()`!

#### F-Strings

تم تقديم F-Strings في بايثون 3.6، وهي الآن الطريقة المفضلة لتنسيق السلاسل النصية.

لتحديد سلسلة نصية كـ F-String، ببساطة ضع حرف `f` أمام النص الحرفي، وأضف الأقواس `{}` كعناصر نائبة للمتغيرات والعمليات الأخرى.

##### مثال:
إنشاء F-String:
```python
age = 36
txt = f"My name is John, I am {age}"
print(txt)  # النتيجة: "My name is John, I am 36"
```

#### العناصر النائبة والمعدلات

يمكن أن يحتوي العنصر النائب على متغيرات وعمليات ودوال ومعدلات لتنسيق القيمة.

##### مثال:
إضافة عنصر نائب للمتغير `price`:
```python
price = 59
txt = f"The price is {price} dollars"
print(txt)  # النتيجة: "The price is 59 dollars"
```

يمكن أن يتضمن العنصر النائب معدلًا لتنسيق القيمة.

##### مثال:
عرض السعر مع منزلتين عشريتين باستخدام `.2f`:
```python
price = 59
txt = f"The price is {price:.2f} dollars"
print(txt)  # النتيجة: "The price is 59.00 dollars"
```

يمكن أن يحتوي العنصر النائب على كود بايثون، مثل العمليات الرياضية:
##### مثال:
إجراء عملية حسابية داخل العنصر النائب وعرض النتيجة:
```python
txt = f"The price is {20 * 59} dollars"
print(txt)  # النتيجة: "The price is 1180 dollars"
```

### استخدام `format()` لتنسيق السلاسل النصية

بدلاً من استخدام F-Strings، يمكنك استخدام دالة `format()` لتنسيق السلاسل النصية.

##### مثال:
استخدام `format()` لدمج متغير مع نص:
```python
age = 36
txt = "My name is John, I am {}".format(age)
print(txt)  # النتيجة: "My name is John, I am 36"
```

##### مثال:
استخدام `format()` لإضافة عدة متغيرات:
```python
quantity = 3
itemno = 567
price = 49.95
myorder = "I want {} pieces of item number {} for {:.2f} dollars."
print(myorder.format(quantity, itemno, price))
# النتيجة: "I want 3 pieces of item number 567 for 49.95 dollars."
```

### بايثون - أحرف الهروب

#### حرف الهروب (Escape Character)

لاستخدام أحرف غير قانونية في سلسلة نصية، يمكن استخدام حرف الهروب.

حرف الهروب هو شريط مائل عكسي `\` متبوعًا بالحرف الذي تريد إدراجه.

##### مثال:
من الأمثلة على الأحرف غير القانونية هي علامة الاقتباس المزدوجة داخل سلسلة نصية محاطة بعلامات اقتباس مزدوجة:
```python
# سيؤدي استخدام علامات اقتباس مزدوجة داخل سلسلة نصية محاطة بعلامات اقتباس مزدوجة إلى خطأ
txt = "We are the so-called "Vikings" from the north."
```

#### لحل هذه المشكلة، استخدم حرف الهروب `\"`:
##### مثال:
يسمح لك حرف الهروب باستخدام علامات الاقتباس المزدوجة عندما لا يكون ذلك مسموحًا به عادةً:
```python
txt = "We are the so-called \"Vikings\" from the north."
print(txt)  # النتيجة: We are the so-called "Vikings" from the north.
```

#### أحرف الهروب الأخرى المستخدمة في بايثون:

| الرمز  | النتيجة |
|--------|---------|
| `\'`   | علامة اقتباس مفردة |
| `\\`   | شريط مائل عكسي |
| `\n`   | سطر جديد |
| `\r`   | إرجاع العربة |
| `\t`   | علامة تبويب |
| `\b`   | مسافة للخلف |
| `\f`   | تغذية النموذج |
| `\ooo` | قيمة ثمانية |
| `\xhh` | قيمة ستة عشرية |

##### أمثلة:

**علامة اقتباس مفردة:**
```python
txt = 'It\'s a beautiful day'
print(txt)  # النتيجة: It's a beautiful day
```

**شريط مائل عكسي:**
```python
txt = "This is a backslash: \\"
print(txt)  # النتيجة: This is a backslash: \
```

**سطر جديد:**
```python
txt = "Hello\nWorld!"
print(txt)
# النتيجة:
# Hello
# World!
```

**علامة تبويب:**
```python
txt = "Hello\tWorld!"
print(txt)  # النتيجة: Hello    World!
```

**مسافة للخلف:**
```python
txt = "Hello\bWorld!"
print(txt)  # النتيجة: HellWorld!
```

**قيمة ثمانية:**
```python
txt = "\110\145\154\154\157"
print(txt)  # النتيجة: Hello
```

**قيمة ستة عشرية:**
```python
txt = "\x48\x65\x6c\x6c\x6f"
print(txt)  # النتيجة: Hello
```

أحرف الهروب مفيدة جدًا عند التعامل مع السلاسل النصية التي تتطلب إدراج أحرف خاصة أو التحكم في تنسيق النص.


### بايثون - دوال السلاسل النصية

تحتوي بايثون على مجموعة من الدوال المدمجة التي يمكن استخدامها مع السلاسل النصية.

**ملاحظة:** جميع دوال السلاسل النصية تُعيد قيمًا جديدة ولا تغير السلسلة النصية الأصلية.

#### دوال السلاسل النصية:

| الدالة        | الوصف                                                      |
|---------------|-------------------------------------------------------------------------------------------------------|
| `capitalize()`|                                                 تحويل الحرف الأول إلى حرف كبير                              |
| `casefold()`  |                                              تحويل السلسلة النصية إلى حروف صغيرة                         |
| `center()`    |                                                        إعادة سلسلة نصية متمركزة                                    |
| `count()`     |                                      إعادة عدد مرات تكرار قيمة محددة في السلسلة النصية           |
| `encode()`    | إعادة نسخة مشفرة من السلسلة النصية                          |
| `endswith()`  | إعادة `True` إذا انتهت السلسلة النصية بالقيمة المحددة       |
| `expandtabs()`| تحديد حجم علامة التبويب في السلسلة النصية                   |
| `find()`      | البحث في السلسلة النصية عن قيمة محددة وإعادة موضعها         |
| `format()`    | تنسيق القيم المحددة في السلسلة النصية                       |
| `format_map()`| تنسيق القيم المحددة في السلسلة النصية                       |
| `index()`     | البحث في السلسلة النصية عن قيمة محددة وإعادة موضعها         |
| `isalnum()`   | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية أبجدية رقمية|
| `isalpha()`   | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية حروف أبجدية|
| `isascii()`   | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية أحرف ASCII|
| `isdecimal()` | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية أرقام عشرية|
| `isdigit()`   | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية أرقام   |
| `isidentifier()`| إعادة `True` إذا كانت السلسلة النصية معرفًا صالحًا       |
| `islower()`   | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية حروف صغيرة|
| `isnumeric()` | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية أرقام   |
| `isprintable()`| إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية قابلة للطباعة|
| `isspace()`   | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية مسافات|
| `istitle()`   | إعادة `True` إذا كانت السلسلة النصية تتبع قواعد العنوان     |
| `isupper()`   | إعادة `True` إذا كانت جميع الأحرف في السلسلة النصية حروف كبيرة|
| `join()`      | دمج عناصر كائن قابل للتكرار إلى نهاية السلسلة النصية       |
| `ljust()`     | إعادة نسخة من السلسلة النصية بمحاذاة إلى اليسار            |
| `lower()`     | تحويل السلسلة النصية إلى حروف صغيرة                         |
| `lstrip()`    | إعادة نسخة من السلسلة النصية بعد إزالة الفراغات اليسارية   |
| `maketrans()` | إعادة جدول ترجمة لاستخدامه في الترجمات                      |
| `partition()` | إعادة قيمة مكونة من ثلاثة أجزاء حيث تنقسم السلسلة النصية   |
| `replace()`   | إعادة سلسلة نصية حيث يتم استبدال قيمة محددة بقيمة أخرى      |
| `rfind()`     | البحث في السلسلة النصية عن قيمة محددة وإعادة آخر موضع لها   |
| `rindex()`    | البحث في السلسلة النصية عن قيمة محددة وإعادة آخر موضع لها   |
| `rjust()`     | إعادة نسخة من السلسلة النصية بمحاذاة إلى اليمين            |
| `rpartition()`| إعادة قيمة مكونة من ثلاثة أجزاء حيث تنقسم السلسلة النصية من النهاية|
| `rsplit()`    | تقسيم السلسلة النصية عند الفاصل المحدد وإعادة قائمة        |
| `rstrip()`    | إعادة نسخة من السلسلة النصية بعد إزالة الفراغات اليمنية    |
| `split()`     | تقسيم السلسلة النصية عند الفاصل المحدد وإعادة قائمة        |
| `splitlines()`| تقسيم السلسلة النصية عند فواصل الأسطر وإعادة قائمة          |
| `startswith()`| إعادة `True` إذا بدأت السلسلة النصية بالقيمة المحددة        |
| `strip()`     | إعادة نسخة من السلسلة النصية بعد إزالة الفراغات            |
| `swapcase()`  | تبادل حالة الأحرف: الحروف الصغيرة تصبح كبيرة والعكس صحيح  |
| `title()`     | تحويل الحرف الأول من كل كلمة إلى حرف كبير                  |
| `translate()` | إعادة سلسلة نصية مترجمة                                    |
| `upper()`     | تحويل السلسلة النصية إلى حروف كبيرة                         |
| `zfill()`     | ملء السلسلة النصية بعدد محدد من القيم 0 في البداية         |


### قائمة دوال السلاسل النصية في بايثون (Python String Methods)

1. **طرق تغيير حالة الأحرف:**

   هذه الطرق تقوم بتغيير حالة الأحرف في السلسلة النصية.

   - `capitalize()`: تحول الحرف الأول إلى حرف كبير.
   - `upper()`: تحول جميع الأحرف إلى أحرف كبيرة.
   - `lower()`: تحول جميع الأحرف إلى أحرف صغيرة.
   - `title()`: تحول الحرف الأول من كل كلمة إلى حرف كبير.
   - `swapcase()`: تبادل حالة الأحرف: الحروف الصغيرة تصبح كبيرة والعكس صحيح.

   مثال:
   ```python
   text = "hello WORLD"
   print(text.capitalize())  # Output: Hello world
   print(text.upper())       # Output: HELLO WORLD
   print(text.lower())       # Output: hello world
   print(text.title())       # Output: Hello World
   print(text.swapcase())    # Output: HELLO world
   ```

2. **طرق البحث والتحقق:**

   هذه الطرق تساعد في البحث عن نصوص معينة أو التحقق من محتوى السلسلة النصية.

   - `startswith()`: تتحقق مما إذا كانت السلسلة تبدأ بنص معين.
   - `endswith()`: تتحقق مما إذا كانت السلسلة تنتهي بنص معين.
   - `find()`: تبحث عن نص معين وتعيد موقعه (أو -1 إذا لم يتم العثور عليه).
   - `index()`: مشابهة لـ `find()`، ولكنها ترفع استثناء إذا لم يتم العثور على النص.
   - `rfind()`: البحث عن قيمة معينة وإعادة آخر موضع لها.
   - `rindex()`: البحث عن قيمة معينة وإعادة آخر موضع لها.

   مثال:
   ```python
   filename = "document.txt"
   print(filename.startswith("doc"))    # Output: True
   print(filename.endswith(".pdf"))     # Output: False
   print(filename.find("ment"))         # Output: 4
   print(filename.index("txt"))         # Output: 9
   print(filename.rfind("c"))           # Output: 2
   print(filename.rindex("c"))          # Output: 2
   ```

3. **طرق التنسيق والتعديل:**

   هذه الطرق تساعد في تنسيق وتعديل محتوى السلسلة النصية.

   - `strip()`: تزيل المسافات والأسطر الجديدة من بداية ونهاية السلسلة.
   - `lstrip()`: تزيل المسافات من بداية السلسلة.
   - `rstrip()`: تزيل المسافات من نهاية السلسلة.
   - `replace()`: تستبدل نصًا بنص آخر.
   - `split()`: تقسم السلسلة إلى قائمة بناءً على فاصل معين.
   - `splitlines()`: تقسم السلسلة النصية عند فواصل الأسطر.
   - `join()`: تدمج عناصر قائمة في سلسلة نصية واحدة.
   - `zfill()`: ملء السلسلة النصية بعدد محدد من القيم 0 في البداية.
   - `expandtabs()`: تحديد حجم علامة التبويب في السلسلة النصية.
   - `center()`: إعادة سلسلة نصية متمركزة.
   - `ljust()`: إعادة نسخة من السلسلة النصية بمحاذاة إلى اليسار.
   - `rjust()`: إعادة نسخة من السلسلة النصية بمحاذاة إلى اليمين.

   مثال:
   ```python
   text = "  Python is awesome  "
   print(text.strip())                   # Output: Python is awesome
   print(text.lstrip())                  # Output: Python is awesome  
   print(text.rstrip())                  # Output:   Python is awesome
   print(text.replace("awesome", "great"))  # Output:   Python is great  
   print("Hello,World".split(","))       # Output: ['Hello', 'World']
   print("Hello\nWorld".splitlines())    # Output: ['Hello', 'World']
   print("-".join(["Python", "3", "9"]))  # Output: Python-3-9
   print("42".zfill(5))                  # Output: 00042
   print("Hello\tWorld".expandtabs(4))   # Output: Hello   World
   print("Python".center(10, "*"))       # Output: **Python**
   print("Python".ljust(10, "-"))        # Output: Python----
   print("Python".rjust(10, "-"))        # Output: ----Python
   ```

4. **طرق التحقق من المحتوى:**

   هذه الطرق تساعد في التحقق من نوع المحتوى في السلسلة النصية.

   - `isalpha()`: تتحقق مما إذا كانت جميع الأحرف أبجدية.
   - `isdigit()`: تتحقق مما إذا كانت جميع الأحرف أرقامًا.
   - `isalnum()`: تتحقق مما إذا كانت جميع الأحرف أبجدية رقمية.
   - `islower()`: تتحقق مما إذا كانت جميع الأحرف صغيرة.
   - `isupper()`: تتحقق مما إذا كانت جميع الأحرف كبيرة.
   - `isascii()`: تتحقق مما إذا كانت جميع الأحرف أحرف ASCII.
   - `isdecimal()`: تتحقق مما إذا كانت جميع الأحرف أرقام عشرية.
   - `isnumeric()`: تتحقق مما إذا كانت جميع الأحرف أرقام.
   - `isidentifier()`: تتحقق مما إذا كانت السلسلة النصية معرفًا صالحًا.
   - `isprintable()`: تتحقق مما إذا كانت جميع الأحرف قابلة للطباعة.
   - `isspace()`: تتحقق مما إذا كانت جميع الأحرف مسافات.
   - `istitle()`: تتحقق مما إذا كانت السلسلة النصية تتبع قواعد العنوان.

   مثال:
   ```python
   print("abc".isalpha())    # Output: True
   print("123".isdigit())    # Output: True
   print("abc123".isalnum()) # Output: True
   print("abc".islower())    # Output: True
   print("ABC".isupper())    # Output: True
   print("Hello".isascii())  # Output: True
   print("12345".isdecimal())# Output: True
   print("12345".isnumeric())# Output: True
   print("myVar".isidentifier())  # Output: True
   print("Hello, World!".isprintable())  # Output: True
   print("   ".isspace())    # Output: True
   print("Hello World".istitle()) # Output: True
   ```

5. **طرق التنسيق والتعديل المتقدمة:**

   هذه الطرق تساعد في تنسيق وتعديل محتوى السلسلة النصية بشكل متقدم.

   - `format()`: تنسيق القيم المحددة في السلسلة النصية.
   - `format_map()`: تنسيق القيم المحددة في السلسلة النصية باستخدام خريطة.
   - `maketrans()`: إعادة جدول ترجمة لاستخدامه في الترجمات.
   - `translate()`: إعادة سلسلة نصية مترجمة.
   - `partition()`: إعادة قيمة مكونة من ثلاثة أجزاء حيث تنقسم السلسلة النصية.
   - `rpartition()`: إعادة قيمة مكونة من ثلاثة أجزاء حيث تنقسم السلسلة النصية من النهاية.

   مثال:
   ```python
   age = 36
   txt = "My name is John, I am {}"
   print(txt.format(age))  # Output: My name is John, I am 36

   person = {'name': 'John', 'age': 36}
   txt = "My name is {name}, I am {age}"
   print(txt.format_map(person))  # Output: My name is John, I am 36

   txt = "Hello, World!"
   trans = txt.maketrans("H", "J")
   print(txt.translate(trans))  # Output: Jello, World!

   txt = "I could eat bananas all day"
   print(txt.partition("bananas"))  # Output: ('I could eat ', 'bananas', ' all day')
   print(txt.rpartition("bananas")) # Output: ('I could eat ', 'bananas', ' all day')
   ```

هذه الطرق تساعدك في التعامل مع السلاسل النصية بشكل فعال في بايثون. تذكر أن السلاسل النصية في بايثون غير قابلة للتغيير (immutable)، لذا فإن هذه الطرق تنشئ دائمًا سلسلة نصية جديدة بدلاً من تعديل السلسلة الأصلية.

### قائمة دوال السلاسل النصية في بايثون (Python String Methods)

#### طرق تغيير حالة الأحرف (Case Conversion Methods)
| **الدالة**        | **الوصف**                                               | **مثال**                                                                 |
|-------------------|----------------------------------------------------------|--------------------------------------------------------------------------|
| `capitalize()`    | تحويل الحرف الأول إلى حرف كبير                           | ```python
|                                                                        |     text = "hello world"<br>print(text.capitalize())  # Hello world
                                                                             ``` |
| `upper()`         | تحويل جميع الأحرف إلى أحرف كبيرة                          | ```python<br>print(text.upper())  # HELLO WORLD```                       |
| `lower()`         | تحويل جميع الأحرف إلى أحرف صغيرة                          | ```python<br>print(text.lower())  # hello world```                       |
| `title()`         | تحويل الحرف الأول من كل كلمة إلى حرف كبير                 | ```python<br>print(text.title())  # Hello World```                       |
| `swapcase()`      | تبادل حالة الأحرف: الحروف الصغيرة تصبح كبيرة والعكس صحيح | ```python<br>print(text.swapcase())  # HELLO world```                    |

#### طرق البحث والتحقق (Search and Check Methods)
| **الدالة**        | **الوصف**                                               | **مثال**                                                                 |
|-------------------|----------------------------------------------------------|--------------------------------------------------------------------------|
| `startswith()`    | تتحقق مما إذا كانت السلسلة تبدأ بنص معين                  | ```python<br>filename = "document.txt"<br>print(filename.startswith("doc"))  # True``` |
| `endswith()`      | تتحقق مما إذا كانت السلسلة تنتهي بنص معين                 | ```python<br>print(filename.endswith(".pdf"))  # False```               |
| `find()`          | تبحث عن نص معين وتعيد موقعه (أو -1 إذا لم يتم العثور عليه)| ```python<br>print(filename.find("ment"))  # 4```                        |
| `index()`         | مشابهة لـ `find()`، ولكنها ترفع استثناء إذا لم يتم العثور على النص | ```python<br>print(filename.index("txt"))  # 9```                        |
| `rfind()`         | البحث عن قيمة معينة وإعادة آخر موضع لها                   | ```python<br>print(filename.rfind("c"))  # 2```                          |
| `rindex()`        | البحث عن قيمة معينة وإعادة آخر موضع لها                   | ```python<br>print(filename.rindex("c"))  # 2```                         |

#### طرق التنسيق والتعديل (Formatting and Modification Methods)
| **الدالة**        | **الوصف**                                               | **مثال**                                                                 |
|-------------------|----------------------------------------------------------|--------------------------------------------------------------------------|
| `strip()`         | تزيل المسافات والأسطر الجديدة من بداية ونهاية السلسلة    | ```python<br>text = "  Python is awesome  "<br>print(text.strip())  # Python is awesome``` |
| `lstrip()`        | تزيل المسافات من بداية السلسلة                           | ```python<br>print(text.lstrip())  # Python is awesome```               |
| `rstrip()`        | تزيل المسافات من نهاية السلسلة                           | ```python<br>print(text.rstrip())  #   Python is awesome```             |
| `replace()`       | تستبدل نصًا بنص آخر                                      | ```python<br>print(text.replace("awesome", "great"))  #   Python is great``` |
| `split()`         | تقسم السلسلة إلى قائمة بناءً على فاصل معين               | ```python<br>print("Hello,World".split(","))  # ['Hello', 'World']```    |
| `splitlines()`    | تقسم السلسلة النصية عند فواصل الأسطر                     | ```python<br>print("Hello\nWorld".splitlines())  # ['Hello', 'World']``` |
| `join()`          | تدمج عناصر قائمة في سلسلة نصية واحدة                     | ```python<br>print("-".join(["Python", "3", "9"]))  # Python-3-9```      |
| `zfill()`         | ملء السلسلة النصية بعدد محدد من القيم 0 في البداية        | ```python<br>print("42".zfill(5))  # 00042```                           |
| `expandtabs()`    | تحديد حجم علامة التبويب في السلسلة النصية                | ```python<br>print("Hello\tWorld".expandtabs(4))  # Hello   World```     |
| `center()`        | إعادة سلسلة نصية متمركزة                                 | ```python<br>print("Python".center(10, "*"))  # **Python**```            |
| `ljust()`         | إعادة نسخة من السلسلة النصية بمحاذاة إلى اليسار          | ```python<br>print("Python".ljust(10, "-"))  # Python----```             |
| `rjust()`         | إعادة نسخة من السلسلة النصية بمحاذاة إلى اليمين          | ```python<br>print("Python".rjust(10, "-"))  # ----Python```             |

#### طرق التحقق من المحتوى (Content Verification Methods)
| **الدالة**        | **الوصف**                                               | **مثال**                                                                 |
|-------------------|----------------------------------------------------------|--------------------------------------------------------------------------|
| `isalpha()`       | تتحقق مما إذا كانت جميع الأحرف أبجدية                     | ```python<br>print("abc".isalpha())  # True```                          |
| `isdigit()`       | تتحقق مما إذا كانت جميع الأحرف أرقامًا                    | ```python<br>print("123".isdigit())  # True```                          |
| `isalnum()`       | تتحقق مما إذا كانت جميع الأحرف أبجدية رقمية               | ```python<br>print("abc123".isalnum())  # True```                       |
| `islower()`       | تتحقق مما إذا كانت جميع الأحرف صغيرة                      | ```python<br>print("abc".islower())  # True```                          |
| `isupper()`       | تتحقق مما إذا كانت جميع الأحرف كبيرة                      | ```python<br>print("ABC".isupper())  # True```                          |
| `isascii()`       | تتحقق مما إذا كانت جميع الأحرف أحرف ASCII                 | ```python<br>print("Hello".isascii())  # True```                        |
| `isdecimal()`     | تتحقق مما إذا كانت جميع الأحرف أرقام عشرية                | ```python<br>print("12345".isdecimal())  # True```                      |
| `isnumeric()`     | تتحقق مما إذا كانت جميع الأحرف أرقام                      | ```python<br>print("12345".isnumeric())  # True```                      |
| `isidentifier()`  | تتحقق مما إذا كانت السلسلة النصية معرفًا صالحًا          | ```python<br>print("myVar".isidentifier())  # True```                   |
| `isprintable()`   | تتحقق مما إذا كانت جميع الأحرف قابلة للطباعة              | ```python<br>print("Hello, World!".isprintable())  # True```            |
| `isspace()`       | تتحقق مما إذا كانت جميع الأحرف مسافات                     | ```python<br>print("   ".isspace())  # True```                          |
| `istitle()`       | تتحقق مما إذا كانت السلسلة النصية تتبع قواعد العنوان      | ```python<br>print("Hello World".istitle())  # True```                  |

#### طرق التنسيق والتعديل المتقدمة (Advanced Formatting and Modification Methods)
| **الدالة**        | **الوصف**                                               | **مثال**                                                                 |
|-------------------|----------------------------------------------------------|--------------------------------------------------------------------------|
| `format()`        | تنسيق القيم المحددة في السلسلة النصية                    | ```python<br>age = 36<br>txt = "My name is John, I am {}"<br>print(txt.format(age))  # My name is John, I am 36``` |
| `format_map()`    | تنسيق القيم المحددة في السلسلة النصية باستخدام خريطة     | ```python<br>person = {'name': 'John', 'age': 36}<br>txt = "My name is {name}, I am {age}"<br>print(txt.format_map(person))  # My name is John, I am 36``` |
| `maketrans()`     | إعادة جدول ترجمة لاستخدامه في الترجمات                  | ```python<br>txt = "Hello, World!"<br>trans = txt.maketrans("H", "J")<br>print(txt.translate(trans))  # Jello, World!``` |
| `translate()`     | إعادة سلسلة نصية مترجمة                                 | ```python<br>print(txt.translate(trans))  # Jello, World!```             |
| `partition()`     | إعادة قيمة مكونة من ثلاثة أجزاء حيث تنقسم السلسلة النصية | ```python<br>txt = "I could eat bananas all day"<br>print(txt.partition("bananas"))  # ('I could eat ', 'bananas', ' all day')``` |
| `rpartition()`    | إعادة قيمة مكونة من ثلاثة أجزاء حيث تنقسم السلسلة النصية من النهاية | ```python<br>print(txt.rpartition("bananas"))  # ('I could eat ', 'bananas', ' all day')``` |

### ملاحظات إضافية:
- **طرق التحقق من المحتوى**: جميع الطرق في هذه الفئة تعيد `True` أو `False` بناءً على محتوى السلسلة النصية.
- **طرق التنسيق والتعديل**:

 تذكر أن السلاسل النصية في بايثون غير قابلة للتغيير (immutable)، لذا فإن هذه الطرق تنشئ دائمًا سلسلة نصية جديدة بدلاً من تعديل السلسلة الأصلية.


