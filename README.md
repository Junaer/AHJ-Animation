[![Build status](https://ci.appveyor.com/api/projects/status/e28hdsp6575ac6lf?svg=true)](https://ci.appveyor.com/project/juaner/ahj-animation)
https://junaer.github.io/AHJ-Animation/

# Домашнее задание к занятию "9. Анимации и CSS"

Правила сдачи задания:

1. **Важно**: в рамках этого ДЗ можно использовать любой менеджер пакетов
1. Вы можете сделать все три задачи в одном репозитории и показать работу всех трёх виджетов на одной странице. Ключевое, чтобы все виджеты были оформлены в виде отдельных классов.
1. Всё должно собираться через Webpack (включая картинки и стили) и выкладываться на Github Pages через Appveyor
1. В README.md должен быть размещён бейджик сборки и ссылка на Github Pages
1. В качестве результата присылайте проверяющему ссылки на ваши GitHub-проекты
1. Авто-тесты писать не требуется



---

### Collapse

#### Легенда

В рамках реализации большого портала вам необходимо сделать виджет "collapsible"-контейнеров, который может разворачиваться и сворачиваться.

#### Описание

Подобный виджет есть в рамках Bootstrap, но как мы с вами "знаем": "jQuery не нужен", поэтому вам нужно реализовать такой же виджет на чистом JS.

![](./pic/collapse.gif)

Авто-тесты на данную задачу не нужны.

---

### Callback Chat* (задача со звёздочкой)
                                 
Важно: эта задача не является обязательной. Её (не)выполнение не влияет на получение зачёта по ДЗ.

#### Легенда

Вам поставили задачу сделать виджет обратной связи на портал компании. Необходимо это сделать. Ключевое тут, конечно же, анимации - поскольку всё остальное вы уже умеете.

#### Описание

Реализуйте показ и скрытие, как это отображено на картинке:

![](./pic/callback.gif)

Обратите внимание, что при нажатии на кнопку, сама кнопка тоже исчезает, а при скрытии формы - появляется.

Длительность анимации, использованная в оригинале, - 100ms, функция анимации - `linear`.

Организуйте код в виде виджета, готового к установке через базовый контейнер в html и инициализацию.

Авто-тестов на данную задачу не нужно.

---

### Liker* (задача со звёздочкой)
                                          
Важно: эта задача не является обязательной. Её (не)выполнение не влияет на получение зачёта по ДЗ.

#### Легенда

Все любят кнопки лайков, вам поручили реализовать одну из них.

#### Описание

Реализуйте поведение, указанное на картинке:

![](./pic/liker.gif)

Данные для анимации:
1. Изображение - ![heart.png](./pic/heart.png)
1. Высота, на которой исчезают лайки - 200px
1. Макс. отклонение влево/вправо - 50px
1. Скорость анимации - 500ms
1. Функция анимации - ease-out (можете использовать другую)
1. Возможные траектории (траектория выбирается рандомно):
    1. 0% - центр, 25% - влево, 50% - центр, 75% - вправо, 100% - центр
    1. 0% - центр, 25% - центр, 50% - вправо, 75% - влево, 100% - центр
    1. 0% - центр, 25% - центр, 50% - влево, 75% - вправо, 100% - центр
    1. 0% - центр, 25% - вправо, 50% - центр, 75% - влево, 100% - центр

**Важно**: обратите внимание, что элементы после "исчезания" должны удаляться из DOM. Используйте для этого соответствующие события, а не таймауты.