# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #1
- Довгий Вадим Игоревич
- РИ-210942
Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

Структура отчета:

- Данные о работе: название работы, фио, группа, выполненные задания.
- Цель работы.
- Задание 1.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 2.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Задание 3.
- Код реализации выполнения задания. Визуализация результатов выполнения (если применимо).
- Выводы.

## Цель работы
Ознакомиться с основными операторами языка Python на примере реализации линейной регрессии.

## Задание 1
### Написать программы Hello World на Python и Unity
- Для Python в отчёте привести скриншоты с демонстрацией сохранения документа google.collab на свой диск с запуском программы, выводящей сообщение Hello world.
- 
![image](https://user-images.githubusercontent.com/45125347/192546585-e63302ff-c463-4ef8-9e58-29a1c32592ce.png)
![image](https://user-images.githubusercontent.com/45125347/192546774-09a25edb-838a-4f9b-b527-ebb91f64b15e.png)

![image](https://user-images.githubusercontent.com/45125347/192546975-6322bdcd-53cc-45f3-a39d-910192774c65.png)
![image](https://user-images.githubusercontent.com/45125347/192547100-cd4260f0-dbbc-4ff9-a0f1-5feb61991d89.png)


## Задание 2
### Пошагово выполнить каждый пункт раздела "ход работы" с описанием и примерами реализации задач
Ход работы:
1) Произвести подготовку данных для работы с алгоритмом линейной регрессии. 10 видов данных были установлены случайным образом, и данные находились в линейной зависимости. Данные преобразуются в формат массива, чтобы их можно было вычислить напрямую при использовании умножения и сложения.

```py

In [ ]:
#Import the required modules, numpy for calculation, and Matplotlib for drawing
import numpy as np
import matplotlib.pyplot as plt
#This code is for jupyter Notebook only
%matplotlib inline

# define data, and change list to array
x = [3,21,22,34,54,34,55,67,89,99]
x = np.array(x)
y = [2,22,24,65,79,82,55,130,150,199]
y = np.array(y)

#Show the effect of a scatter plot
plt.scatter(x,y)

```

![2022-09-27_19-01-17](https://user-images.githubusercontent.com/45125347/192549786-1e76ca4d-3054-4063-8f6c-803aaf1db367.png)

2) Определите связанные функции. Функция модели: определяет модель линейной регрессии wx+b. Функция потерь: функция потерь среднеквадратичной ошибки. Функция оптимизации: метод градиентного спуска для нахождения частных производных w и b.

![2022-09-27_19-03-25](https://user-images.githubusercontent.com/45125347/192549958-3f64bc41-dbd9-416a-a7fd-f2e8b7d76c9f.png)

3) Начать итерацию.
### Шаг 1 Инициализация и модель итеративной оптимизации

![2022-09-27_19-07-37](https://user-images.githubusercontent.com/45125347/192550065-95475fea-5fc1-475b-89e3-aecea8502349.png)

### Шаг 2 На второй итерации отображаются значения параметров, значения потерь и эффекты визуализации после итерации

![2022-09-27_19-07-48](https://user-images.githubusercontent.com/45125347/192550093-3b2a92e0-7b29-480d-9f48-acb3cfad7911.png)

### Шаг 3 Третья итерация показывает значения параметров, значения потерь и визуализацию после итерации

![2022-09-27_19-07-59](https://user-images.githubusercontent.com/45125347/192550154-2e1e07c3-d22c-44e4-8e10-a014f2dc7559.png)

### Шаг 4 На четвертой итерации отображаются значения параметров, значения потерь и эффекты визуализации

![2022-09-27_19-08-11](https://user-images.githubusercontent.com/45125347/192550208-e99f234d-9163-49f4-84e0-3875ad9f9f35.png)

### Шаг 5 Пятая итерация показывает значение параметра, значение потерь и эффект визуализации после итерации

![2022-09-27_19-08-22](https://user-images.githubusercontent.com/45125347/192550254-371b1a5b-a00a-4b05-8865-b5a35bbe3080.png)

### Шаг 6 10000-я итерация, показывающая значения параметров, потери и визуализацию после итерации

![2022-09-27_19-08-31](https://user-images.githubusercontent.com/45125347/192550287-7be31eb6-579b-4b04-a7df-3ff823e187db.png)

## Задание 3
### Должна ли величина loss стремиться к нулю при изменении исходных данных? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ.

Величина loss будет стремиться к 0, поскольку она зависит от a,b, которые в свою очередь зависят от times. Меняя значение times в большую сторону, loss будет уменьшаться. Прошу обратить внимание на скриншоты снизу. На них всё наглядно видно.

1)![2022-09-27_19-13-09](https://user-images.githubusercontent.com/45125347/192550855-f1118746-e91d-4bce-ac2d-32c723957999.png)
При times = 100, loss = 1172.3

2) ![2022-09-27_19-13-43](https://user-images.githubusercontent.com/45125347/192550995-df8e5c37-8fab-4317-8546-694c18302971.png)
При times = 1000, loss = 191.4

3) ![2022-09-27_19-32-35](https://user-images.githubusercontent.com/45125347/192555523-6516c6e4-7c4e-44dd-9d58-45e0851186cf.png)
При times = 1000000, loss = 181.8

### Какова роль параметра Lr? Ответьте на вопрос, приведите пример выполнения кода, который подтверждает ваш ответ. В качестве эксперимента можете изменить значение параметра.

Параметр Lr отвечает за угол прямой, которая изображена на графике.

1)![2022-09-27_19-36-51](https://user-images.githubusercontent.com/45125347/192556650-03845a86-3203-4c4e-81b8-06b69e2d9d4e.png)
При Lr = 0.000001 и times = 100

2)![2022-09-27_19-37-11](https://user-images.githubusercontent.com/45125347/192556711-dbfa6137-8219-4fc9-b142-2dc4b3dac28c.png)
При Lr = 0.0001 и times = 100

## Выводы

В ходе лабораторной работы я написал "Hello, World!" на Python в Google Collab и на C# в Unity(вывел в consol). Также, помимо всего прочего,
я познакомился с алгоритмом линейной регрессии и осуществил функции модели, потерь и оптимизации. Я провёл эксперименты над переменными loss и Lr, которые помогли мне определить их зависимости.

| Plugin | README |
| ------ | ------ |
| Dropbox | [plugins/dropbox/README.md][PlDb] |
| GitHub | [plugins/github/README.md][PlGh] |
| Google Drive | [plugins/googledrive/README.md][PlGd] |
| OneDrive | [plugins/onedrive/README.md][PlOd] |
| Medium | [plugins/medium/README.md][PlMe] |
| Google Analytics | [plugins/googleanalytics/README.md][PlGa] |

## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
