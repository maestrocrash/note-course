## Task #1 - Note

1. Создайте файл `Note.swift`. В нём вам предстоит реализовать первый код для будущего приложения заметок — структуру Note. По ходу курса файлов будет становиться больше, и вы соберёте из них полноценный проект. 
2. Реализуйте заметку в виде структуры Note. Структура должна удовлетворять следующим условиям:
	* Она полностью иммутабельна. Это поможет вам легко обеспечить потокобезопасность и избежать проблем в дальнейшем.
	* Содержит уникальный идентификатор `uid`. Если не задан пользователем, генерируется с помощью `UUID().uuidString`. Это позволит легко сравнивать два экземпляра одной заметки и облегчить дедупликацию. 
	* Содержит обязательные строковые поля — `title` и `content`. Без заголовка и текста не обойтись.
	* Содержит цвет заметки - `color`. Пользователь сможет создать заметку любого цвета.  Если он его не задал, по умолчанию ставим белый (класс `UIColor` из `UIKit`). Так пользователи смогут структурировать заметки по темам с помощью цветовой раскраски.
	* Содержит обязательное поле важность (`importance `). Должно быть `enum` с тремя значениями: «неважная», «обычная» и «важная» (`unimportant`, `normal`, `important`). Так пользователь сможет расставлять заметкам приоритет.
	* Содержит необязательно поле «Дата самоуничтожения» (`selfDestructionDate`) типа `Date`. Может отсутствовать.
 