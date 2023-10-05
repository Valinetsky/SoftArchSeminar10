
# Архитектура ПО. Семинар 10. Структура приложения с пользовательским интерфейсом и базой данных

## Разработка архитектуры мессенджера
С приложением будут работать два типа пользователей: администратор, запускающий и останавливающий сервер, и некоторое количество людей, подключающихся к этому серверу, пишущих сообщения, и завершающих работу с сервером, отключившись от него.

По факту будет даже не одно приложение, а два (сервер и клиент), взаимодействующие друг с другом.

![Usecase diagram](/img/page01.png "Usecase diagram")


На следующей иллюстрации отображен полный цикл работы приложений:

![Flow diagram](/img/page02.png "Flow diagram")


Клиентскую и серверную части реализуем по модели MVC: это будет удобно для дальней разработки, например переходу от использования JFrame в UI к более продвинутым инструментам проектирования пользовательского интерфейса.

Обе части соеденим посредством Socket.

И при написании кода воспользуемся развернутой диаграммой классов, которая, если не считать деталей реализации, практически полностью описывает наши приложения:

![Class diagram](/img/page03.png "Class diagram")


## Работа с приложением
Администратор запускает сервер (файл `Server`), указывая его адрес и порт, который он будет слушать.

![Class diagram](/img/server01.png "Class diagram")

