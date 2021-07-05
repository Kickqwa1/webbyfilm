
Запуск сервера:

npm install

npm start

Для запуска проекта необходимо войти в консоль, 
перейти в директорию webbyFilm, командой "npm instal" скачать все библиотеки, 
при помощи которых работает приложение, и запустить сервер командой "npm start"

Также у вас должна быть запущена база MongoDB.

Для работы с приложением следует воспользоваться программой Postman или аналогом

!!!В postman при загрузке файла через form-data, ключем должен быть 'fileData'!!!


Архитектура приложения:

При помощи "mongoose" в модуле models/film.js описывается модель документа, 
а используя "Joi" происходит его валидация.

Модель документа и функция валидации передаётся в модуль routes/movies.js, 
где происходит маршрутизация от express.Routes().

В зависимости от пути данные обрабатываются маршрутизатором от express.Routes().

Все маршруты из модуля routes/movies.js подключаются в главном модуле index.js,
который связывается с базой данных, подключает маршрутизацию и запускает сервер.
