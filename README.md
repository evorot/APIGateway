# APIGateway

1. Чтобы собрать проект, необходимо ввести docker-compose up --build
2. Gateway запускается на localhost:8000
3. Доступные endpoints:
    -	/news{?page=&s=} - выводит последние новости с объектом пагинации, возможно указание номера страницы, параметр "s" отвечает за поиск новостей по ключевому слову  
	- /news/latest{?page=} - выводит последние новости, возможно указание номера страницы 
	- /news/search{?id=} - поиск детальной информации новости по id с выводом комментариев
	- /comments/add - добавление комментария по id новости или id родительского комментария, проверка контента на слова из стоплиста (endpoint принимает POST запрос в формате JSON, пример: {"newsID": 35, "content": "Тест сообщение"})
