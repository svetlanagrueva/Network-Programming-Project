# Network-Programming-Project
Проект по Мрежово Програмиране
Създаване на клиент-сървър приложение
 
1.Тема:

Проектът реализира клиент-сървър приложение: Клиентът изпраща на сървъра лог файл чрез UDP протокола във формат
<Time,Event context,Component,Event name,Description,Origin,IP address>
Сървърът използва DefMe алгоритъма и изпраща на клиента резултата.

2.Описание на решението:

Клиентът чете данните от лог файла чрез Scanner и изпраща ред по ред информацията на сървъра чрез UDP( посредством дейтаграми).
При първото получено съобщение, сървърът запазва Inet адреса и порта във файл “address.txt”.
Сървърът получава съобщенията и екстрактва user id-то на потребителя от всеки ред получена информация и го
записва във файла „log_results.txt”. След това използва DefMe алгоритъма върху този файл за да определи за всеки потребител 
колко е бил активен – броят на срещанията на id-то му в лога. Резултата се записва във файл “output.txt” и се изпраща на Клиента отново
чрез дейтаграми.

3.Проектиране

3.1 Създадени са два класа – Клиент и Сървър. Допълнително е добавен и класа за DefMe алгоритъма

3.1 Input file – лог файла

3.2 По време на изпълнение се създават файловете:
“address.txt”, “log_results.txt”, “output.txt”
