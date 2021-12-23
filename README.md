# Books

[![Build Status](https://travis-ci.org/rust-lang-ru/books.svg?branch=master)](https://travis-ci.org/rust-lang-ru/books)

Метарепозиторий для сборки и деплоя переводов книг.

Здесь собраны переводы книг сообщества: Rust by example, Async book, TRPL и другие.

Перевод каждой книги находится в своём репозитории, здесь же они добавлены 
сабмодулями.

Сейчас сборка происходит следующим образом:
1. в каждом сабмодуле запускается скрипт `<submodule>/scripts/pre-build.sh`, который 
подготавливает книгу к сборке (например, для async-book в директорию перевода копируется 
директория `examples` из оригинала)
2. происходит сборка каждой книги при помощи [mdbook](https://github.com/rust-lang-nursery/mdBook/)
3. собранные книги отправляются на сервер.

Так как деплой происходит на домен doc.rust-lang.ru, то мы стараемся создать такую же структуру 
документации, как и на https://doc.rust-lang.org. За счёт этого только лишь заменой "org" на "ru"
в оригинале и "ru" на "org" в переводе, мы получаем в первом случае перевод, а во втором - оригинал.

Если вы нашли какую-либо ошибку в книге, отпишитесь в репозитории соответствующего перевода. Если вы
нашли несоответствие в структуре деплоя, создайте [issue в этом репозитории](https://github.com/rust-lang-ru/books/issues/new)

## Переводы книг и где они обитают

| Название | Ссылка | Репозиторий |
|---|---|---|
| The Rust Programmin Language | https://doc.rust-lang.ru/book | https://github.com/rust-lang-ru/book |
| Rust by example | https://doc.rust-lang.ru/stable/rust-by-example | https://github.com/rust-lang-ru/rust-by-example |
| Async book | https://doc.rust-lang.ru/async-book | https://github.com/rust-lang-ru/async-book |
| Rust Cookbook | https://doc.rust-lang.ru/rust-cookbook | https://github.com/rust-lang-ru/rust-cookbook |
