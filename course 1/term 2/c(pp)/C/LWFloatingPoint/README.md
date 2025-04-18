# Лабораторная работа №1. Представление чисел с плавающей точкой

Текущий статус тестирования GitHub Actions: [![CI/CD](../../actions/workflows/ci.yaml/badge.svg?branch=main&event=workflow_dispatch)](../../actions/workflows/ci.yaml).

> [!Note]
> Чтобы GitHub Workflow отработал верно, файл с [функцией `main`](https://en.cppreference.com/w/c/language/main_function) должен называться `main.c`.

Вам предоставляется возможность запуска базовых тестов локальным способом. Для этого нужно:

1. Установить [Python](https://www.python.org/).
2. Убедиться, что у Вас установлены следующие библиотеки: `hashlib`, `difflib`, `pyperclip` (в ином случае, установить через [`pip`](https://pypi.org/project/pip/)).
3. Склонировать репозиторий рекурсивно `git clone <repo_url> --recursive`. В противном случае `submodule` тестов не склонируется и счастье не наступит.
4. В корне репозитория запустить `python tests.py <path/to/executable>`.
5. Посмотреть логи тестирования.

По умолчанию, запускаются все *категориальные* тесты. Если нужны конкретные категории, в аргументы запуска необходимо подать наименования категорий (см. ниже). Внимание: если тест требует две категории и был подан только один из них, тест *не будет запущен*, необходимо подать обе категории.

Список категорий:

* **`0`** - округление к 0
* **`1`** - округление к ближайшему чётному
* **`2`** - округление к плюс-бесконечности
* **`3`** - округление к минус-бесконечности
* **`single_print`** - вывод числа (плавающая точка)
* **`single_multiply`** - умножение двух чисел (плавающая точка)
* **`single_sum`** - сложение двух чисел (плавающая точка)
* **`half_multiply`** - умножение двух чисел (плавающая точка с половинной точностью)
* **`special`** - специальные случаи

Пример запуска:

```bash
python tests.py main 0 1 single_print
# запуск тестов с двумя видами округлений (к 0 и ближайшем чётному) на вывод числа
```
