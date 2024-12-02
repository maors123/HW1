// פונקציה לבדוק אם מספר הוא ראשונfunction PrimeNumber(num) {
    if (num <= 1) // 1 וכל המסםרים שמתחתיו לא ראשוניים
        return false; 
    for (let i = 2; i * i <= num; i++) {
        if (num % i === 0) {
            return false; // אם יש מחלקים פרט ל-1 ולמספר עצמו, הוא לא ראשוני
        }
    }
    return true;
}
for (let i = 2; i < 237; i++) { // ידפיס את כל המספרים הראשוניים הקטנים מ-237
    if (PrimeNumber(i)) {
        console.log(i);
    }
}
