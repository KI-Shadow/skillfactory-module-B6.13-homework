# B6.13 - Домашнее задание
Доброго времени суток. Данный репозиторий предназначен для проверки домашнего задания по курсу "Skillfactory - Full-stack веб-разработчик на Python".
## Инструкция
1) Скачайте zip архив по ссылке ниже и разархивируйте его на своем компьютере.
2) Через командную строку запустите файл my_album_server.py - это и есть наш сервер.
3) Откройте браузер и перейдите по следующей ссылке: http://localhost:8080/albums/Beatles - вы получить данные об альбомах исполнителя Beatles, имя исполнителя можно заменить. Таким образом вы получили ответ на свой GET запрос.
4) Запустить ещё одну командную строку, предварительно установив HTTPie, введите данный POST запрос: http -f POST http://localhost:8080/albums artist="New Artist" genre="Rock" album="Super"
В результате этого запроса должна появиться ошибка уведомляющая, что вы некорректно ввели данные, это связано с тем, что при попытке добавить новый альбом мы не указали год его написания, что является некорректным.
5) Исправим наш запрос и попробуем снова добавить новый альбом в базу данных: http -f POST http://localhost:8080/albums year=2020 artist="New Artist" genre="Rock" album="Super"
Вам должно придти уведомление, что данные успешно сохранены, поздравляю!
6) Попробуем снова ввести запрос из пункта 5, в результате запросы мы получим ошибку, что такой альбом уже имеется, это защита нашей программы от добавления одинаковых альбомов

P.S. В программе предусмотрена защита от ввода некорректного значения года допускается диапазон: 0 - 2200. А также защита от неправильного типа данных: Название альбома, название жанра или имя исполнителя не может состоять из одних цифр.

**Ссылка для скачивания программы: https://github.com/KI-Shadow/skillfactory-module-B6.13-homework/archive/main.zip**
