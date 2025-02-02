

### **ما هو Linux؟**
- **Linux** هو نظام تشغيل (Operating System)، زي نظام Windows أو macOS، لكنه مفتوح المصدر (يعني الكود الخاص به متاح لأي شخص لتعديله أو تحسينه).  
- يُستخدم في السيرفرات، الهواتف، الأجهزة الذكية، وحتى أجهزة الكمبيوتر الشخصية.

---

### **كيف يعمل نظام Linux؟**
- يعتمد Linux على شيء اسمه **النواة (Kernel)**، وهي الجزء الأساسي من النظام اللي يدير كل شيء:  
  - **التعامل مع العتاد (Hardware):** مثل المعالج والذاكرة.  
  - **إدارة العمليات (Processes):** مثل تشغيل البرامج.  

- الملفات والنظام كله يعتمد على هيكل هرمي (Tree Structure)، يعني كل شيء يبدأ من **"/"** اللي هو جذر النظام (Root).

---

### **هيكل الملفات في Linux**
#### لما تفتح نظام Linux، حتشوف هيكل الملفات مقسّم إلى:
1. **/** (Root):  
   - هو الجذر، وكل الملفات والمجلدات موجودة تحته.
   
2. **/home:**  
   - هنا توجد ملفات المستخدمين (كل مستخدم عنده مجلد خاص باسمه).  
   - مثال: إذا اسم المستخدم "shaheen"، فملفاتك تكون في:  
     ```
     /home/shaheen
     ```

3. **/etc:**  
   - يحتوي على ملفات إعدادات النظام والبرامج.

4. **/bin:**  
   - يحتوي على الأوامر والبرامج الأساسية مثل `ls` و`cp`.

5. **/var:**  
   - يحتوي على ملفات متغيرة مثل سجلات النظام (logs).

6. **/tmp:**  
   - ملفات مؤقتة يتم حذفها تلقائيًا بعد فترة.

7. **/usr:**  
   - يحتوي على البرامج والتطبيقات اللي يتم تثبيتها.

---

### **الأوامر الأساسية في Linux**
#### لما تستخدم Linux، تتعامل معه عن طريق **سطر الأوامر (Terminal)**. خليني أشرح لك أهم الأوامر:

---

#### 1. **عرض الملفات والمجلدات (ls):**
   - يستخدم لاستعراض الملفات في المجلد الحالي.  
   - مثال:  
     ```
     $ ls
     ```
   - النتيجة:  
     ```
     file1.txt  file2.txt  my_folder
     ```

#### 2. **الدخول إلى مجلد (cd):**
   - يستخدم للتنقل بين المجلدات.  
   - مثال:  
     ```
     $ cd /home/shaheen
     ```

#### 3. **عرض المجلد الحالي (pwd):**
   - يعرض المسار الحالي اللي انت فيه.  
   - مثال:  
     ```
     $ pwd
     ```
   - النتيجة:  
     ```
     /home/shaheen
     ```

#### 4. **إنشاء ملف أو مجلد:**
   - لإنشاء ملف فارغ:  
     ```
     $ touch myfile.txt
     ```
   - لإنشاء مجلد:  
     ```
     $ mkdir my_folder
     ```

#### 5. **نسخ الملفات (cp):**
   - لنسخ ملف من مكان لآخر.  
   - مثال:  
     ```
     $ cp myfile.txt /home/backup/
     ```

#### 6. **نقل الملفات (mv):**
   - لنقل أو إعادة تسمية ملف.  
   - مثال:  
     ```
     $ mv myfile.txt newname.txt
     ```

#### 7. **حذف الملفات أو المجلدات:**
   - لحذف ملف:  
     ```
     $ rm myfile.txt
     ```
   - لحذف مجلد:  
     ```
     $ rm -r my_folder
     ```

#### 8. **عرض محتوى ملف (cat):**
   - يعرض محتويات ملف نصي.  
   - مثال:  
     ```
     $ cat myfile.txt
     ```

#### 9. **تحميل البرامج (apt-get):**
   - يستخدم لتثبيت البرامج (في توزيعات مثل Ubuntu).  
   - مثال:  
     ```
     $ sudo apt-get install firefox
     ```

#### 10. **إدارة الصلاحيات (chmod):**
   - لتغيير صلاحيات ملف.  
   - مثال:  
     ```
     $ chmod 755 myfile.sh
     ```

---

### **أمثلة عملية بسيطة:**

#### مثال 1: إنشاء ملف ونقله لمجلد آخر
1. إنشاء ملف:
   ```
   $ touch test.txt
   ```
2. إنشاء مجلد جديد:
   ```
   $ mkdir myfolder
   ```
3. نقل الملف إلى المجلد:
   ```
   $ mv test.txt myfolder/
   ```

#### مثال 2: البحث عن ملف معين
- باستخدام أمر `find`:
  ```
  $ find /home -name "test.txt"
  ```

---

### **أشياء يجب معرفتها عن Linux:**
1. **الحساسية لحالة الأحرف:**  
   - في Linux، "File.txt" و"file.txt" يعتبران ملفات مختلفة.

2. **صلاحيات المستخدم:**  
   - هناك صلاحيات للمستخدم العادي وصلاحيات للمسؤول (root).  
   - أوامر تحتاج إلى صلاحيات المسؤول تبدأ بـ `sudo`.

3. **التوزيعات (Distributions):**  
   - هناك توزيعات مختلفة مثل Ubuntu، Fedora، Arch، ولكل واحدة ميزاتها.

---
