В этом задании в нашу функцию testDateTime передаются две строки вида "03 November 2017 04:17".
Вам нужно превратить строки в даты, сравнить их. Для той, что больше получить день недели и вернуть его из функции.

Название дня недели должно быть по-русски, с большой буквы, например: "Понедельник".

Sample Input 1:
04 April 1909 17:29
21 July 1909 09:13

Sample Output 1:
Среда

Sample Input 2:
09 May 1909 07:49
25 September 1909 04:13

Sample Output 2:
Суббота
Напишите программу. Тестируется через stdin → stdout
Верно решили 14 945 учащихся
Из всех попыток 28% верных


function testDateTime(a, b) {
    var date_a = new Date(a)
    var date_b = new Date(b)    
    days = ["Воскресенье", "Понедельник", "Вторник", "Среда", "Четверг", "Пятница", "Суббота"]
    if (+date_a > +date_b) return days[date_a.getDay()];
    else return days[date_b.getDay()];  
}