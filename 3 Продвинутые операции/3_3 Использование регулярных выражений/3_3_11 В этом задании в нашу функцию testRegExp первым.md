В этом задании в нашу функцию testRegExp первым параметром передается случайная строка(переменная s), а вторым - случайная подстрока(переменная sub_s), которую нужно использовать в качестве шаблона регулярного выражения. Вам нужно вернуть из функции строку, в которой будут перечислены через запятую все совпадения шаблона с первой строкой.

 
Sample Input 1:
Andsirdaarrevarariarewbutovearrmararan
ar

Sample Output 1:
ar,ar,ar,ar,ar,ar,ar

Sample Input 2:
Extremitiyasiifbrieakfaistagreement
i

Sample Output 2:
i,i,i,i,i,i


Напишите программу. Тестируется через stdin → stdout
Верно решили 10 729 учащихся
Из всех попыток 28% верных



function testRegExp(s, sub_s) {
    // Создаем регулярное выражение из подстроки sub_s с глобальным флагом, чтобы найти все совпадения
    var regex = new RegExp(sub_s, 'g');
    
    // Используем метод match для поиска всех совпадений
    var matches = s.match(regex);
    
    // Если совпадений нет, возвращаем пустую строку, иначе объединяем массив в строку через запятую
    return matches ? matches.join(',') : '';
}

