1. Назначение библиотеки:

  Библиотека необходима для создания документов .docx с помощью формата Office Open XML, без участия COM-объекта.
  
  Модули реализованы на основании Библиотеки стандартных подсистем 3.1.2, ничего лишнего, только программное формирование документов .docx
  
  Официальная страница https://its.1c.ru/db/bsp312doc
  
  Страница репозиторий https://github.com/1c-syntax/ssl_3_1
  
  Поддерживает создание сложных документов, а так же пакетное формирование с архивированием в zip архив.
  
2. Системные требования: Платформа 1С Предприятие не ниже 8.3.6
3. Основные процедуры и функции

Клиентские
```bsl
// Процедура - Новый документ в формате OOXML
//
// Параметры:
//  ИмяМакета - Строка - Наименования в общем макете
//  ДанныеПечати - Структура - Структура заполняемых парамертов в макете
//  ИмяПолучаемогоФайла - Строка - Наименование получаемого файла 
//
Процедура НовыйДокументВФорматеOOXML(ИмяМакета, ДанныеПечати, ИмяПолучаемогоФайла = "") Экспорт
```
```bsl
// Процедура - Новые документы в формате OOXML
//
// Параметры:
//  Документы - Массив - набор структур данных для печати, с ключами:
// 	 	* ИмяМакета - Строка - Наименования в общем макете
//   	* ДанныеПечати - Структура - Структура заполняемых парамертов в макете
//		* ИмяПолучаемогоФайла - Строка - Наименование получаемого файла
//  АрхивироватьВZip - Булево - Архивировать в архив zip или нет,
//									если нет тогда документы откроются из временного хранилища на клиенте
//
Процедура НовыеДокументыВФорматеOOXML(Документы, АрхивироватьВZip = Истина) Экспорт

```
Серверные
```bsl
// Функция - Новый документ OOXML
//
// Параметры:
//  ИмяМакета - Строка - Наименование общего макета
//  ДанныеПечати - Структура - Строковые представления данных для печати
// 
// Возвращаемое значение:
//   - Структура
//		* АдресВоВременномХранилище - Строка - 
//
Функция НовыйДокументOOXML(ИмяМакета, ДанныеПечати) Экспорт  

```
