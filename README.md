# memRamCache

Менеджер кеша в памяти на Golang, хранилище данных в формате ключ/значение


## Как установить?

  go get github.com/Catzilllla/memRamCache


## Как использовать?

Необходимо импортировать пакет

	import (
		memramcache "github.com/github.com/Catzilllla/memRamCache"
	)

Инициализировать кеш

	// Создаем кеш с временем жизни по-умолчанию равным 5 минут и удалением просроченного кеша каждые 10 минут
	cache := memorycache.New(5 * time.Minute, 10 * time.Minute)


Использовать

	// Установить кеш с ключем "myKey" и временем жизни 5 минут
	cache.Set("myKey", "My value", 5 * time.Minute)

	// Получить кеш с ключем "myKey"
	i := cache.Get("myKey")
