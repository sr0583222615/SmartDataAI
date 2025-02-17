# SmartDataAI
# פיתוח מערכת חכמה מבוססת AI לעיבוד נתונים והפקת תובנות

תוכנית זו מאפשרת לבצע ניתוחים מבוססי NLP על מסמכים מסוגים שונים (Excel, PDF, אתרי אינטרנט), תוך שילוב של מודלים חכמים מ-OpenAI לצורך הפקת תובנות ושאלות. ניתן להפעיל את התוכנית כקובץ EXE ישירות משורת הפקודה.

## דרישות מקדימות

לפני הריצה של התוכנית, יש לוודא כי קיימים המתקנים הבאים:

## מפתח key api של OpenAI
- עליך להחזיק מפתח API פעיל מ-OpenAI.
- אם אין לך מפתח, היכנס לאתר OpenAI ויצור מפתח API אישי.
- שמור את המפתח בקובץ טקסט בשם `api_key.txt`.

### קבצי קלט:
- התוכנית תומכת בקבצים מסוגים Excel (XLSX), PDF, או קישורים לאתרים.
- ודא שיש לך את הקבצים או הקישורים אותם תרצה לנתח.

## איך להריץ את התוכנית

### שלב 1: הורדה והכנה
1. הורד את קובץ ה-EXE של התוכנית שיסופק לך.
2. הכנס את מפתח ה-API שלך לתוך קובץ טקסט בשם `api_key.txt`.
3. הגדר את השאלה שברצונך לשאול את המודל וכתוב אותה בקובץ טקסט בשם `question.txt`.
4. הכנס את קבצי הקלט שברצונך לנתח, לדוגמה: קובצי PDF, Excel או קישורים לאתרים.

### שלב 2: הרצה
הפעל את התוכנית דרך שורת הפקודה (Command Prompt) במחשב שלך, עם הפקודה הבאה: main.exe -i "file1.xlsx" "file2.pdf" "https://example.com" -q "question.txt" -o "output.txt" -k "api_key.txt"
#### פרמטרים:
- קובץ קלט: `-i` (אפשר להכניס כמה קבצים, כולל URL).
- קובץ שאלה: `-q` (השאלה שברצונך לשאול על התוכן).
- קובץ פלט: `-o` (היכן להוציא את התשובה).
- קובץ מפתח API של OpenAI: `-k` (המפתח שלך לקבלת גישה לשירותי OpenAI).

לאחר הרצת הפקודה, התוכנית תעבד את התוכן בקבצים שצוינו, תשלח את השאלה ל-OpenAI, ואז תכתוב את התשובה בקובץ הפלט שציינת.

דוגמאות להרצה:
דוגמה 1: הרצה עם קבצי PDF ו-Excel
אם ברצונך לשאול שאלה על תוכן מתוך קובץ PDF ו-Excel, השתמש בפקודה הבאה:main.exe -i "document1.pdf" "data.xlsx" -q "question.txt" -o "response.txt" -k "api_key.txt"



דוגמה 2: הרצה עם אתר אינטרנט
אם ברצונך לשאול שאלה על תוכן מאתר אינטרנט, השתמש בפקודה הבאה:main.exe -i "https://example.com" -q "question.txt" -o "response.txt" -k "api_key.txt"



איך התוכנית עובדת
התוכנית טוענת את הקבצים שציינת (PDF, Excel או קישורים לאתרים) וממזגת את התוכן.
התוכנית שואלת את השאלה שציינת ומעבדת את התשובה בעזרת מודל OpenAI.
התשובה נשמרת בקובץ הפלט שביקשת.









