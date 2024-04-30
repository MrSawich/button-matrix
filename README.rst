=====================
Матричная клавиатура
=====================

В этом уроке мы создадим матричную клавиатуру с помощью Arduino UNO. Матричная клавиатура - это тип клавиатуры, в которой кнопки соединены в матрицу из рядов и столбцов. Это эффективный способ подключения нескольких кнопок к Arduino с использованием минимального количества пинов. Для выполнения работы мы будем использовать сайт https://www.tinkercad.com , который имеет инструментарий для работы платы микроконтроллера Arduino UNO, но если у вас есть набор-комплект Ардуино вы можете собрать его самостоятельно по этому уроку. 

Введение
---------

Для работы на сайте вам понадобиться зарегестрироваться на сайте и создать новый проект.

.. image:: tinker/1.jpg
    :alt: Global map with sparse data
    :width: 600
.. image:: tinker/2.jpg
    :alt: Global map with sparse data
    :width: 600
.. image:: tinker/3.jpg
    :alt: Global map with sparse data
    :width: 600

Далее нам нужно взять из меню справа необходимые компоненты а именно "Arduino Uno R3" и уже собранную матричную клавиатуру "Keypad 4x4"

.. image:: tinker/4.jpg
    :alt: Global map with sparse data
    :width: 600

Схема матричной клавиатуры представляет собой способ подключения 16 кнопок в виде матрицы 4x4 к микроконтроллеру Arduino. Вместо того, чтобы подключать каждую кнопку к отдельному пину Arduino, матричная клавиатура использует эффективную схему, которая позволяет сократить количество необходимых пинов.

Вот как выглядит типичная схема матричной клавиатуры 4x4

.. image:: tinker/5.jpg
    :alt: Global map with sparse data
    :width: 600

В этой есть 4 строки (ряда) и 4 столбца. Каждая кнопка находится на пересечении строки и столбца. Чтобы подключить эту клавиатуру к Arduino UNO, вам нужно будет подключить строки к пинам цифрового вывода Arduino, а столбцы - к пинам входа.

Подключите строки клавиатуры (Row 1 - Row 4) к пинам цифрового вывода Arduino, например, к пинам 8, 9, 10, 11.
Подключите столбцы клавиатуры (Column 1 - Column 4) к пинам входа Arduino, например, к пинам 4, 5, 6, 7.

.. image:: tinker/6.jpg
    :alt: Global map with sparse data
    :width: 600

Используя эту схему, вы можете контролировать состояние 16 кнопок с помощью только 8 пинов Arduino. Микроконтроллер сканирует строки и столбцы, чтобы определить, какая кнопка нажата. Это достигается путем подачи напряжения на одну строку за раз и проверки состояния столбцов, чтобы определить, какая кнопка на пересечении была нажата.

Для обработки нажатий клавиш и определения, какая кнопка была нажата, можно использовать библиотеку Keypad для Arduino. Эта библиотека упрощает процесс считывания и интерпретации нажатий клавиш в матричной клавиатуре.

В целом, схема матричной клавиатуры 4x4 для Arduino UNO позволяет эффективно подключать и считывать несколько кнопок, что делает ее популярным выбором для проектов, требующих ввода пользователя.

Компоненты
----------

* Global data plot

.. image:: docs/img/global_sparse.png
    :alt: Global map with sparse data
    :width: 600

* Global map plot

.. image:: docs/img/global_regular.png
    :alt: Global map on regular grid
    :width: 600

* Regional data plot

.. image:: docs/img/regional_sparse.png
    :width: 600
    :alt: Regional map with sparse data 

* Distance-time plot (under development)

.. image:: docs/img/distance_time.png
    :width: 600
    :alt: Distance time plot

* `Round Earth projection <https://github.com/gnss-lab/simurg_plotter/blob/master/scripts/plot_sphere.py>`_ (under development)

.. image:: docs/img/round_earth_projection.png
   :width: 400
   :alt: Animation plots

* `Animation plots <https://github.com/gnss-lab/simurg_plotter/blob/master/scripts/animate_sphere.py>`_ (under development)

.. image:: docs/gif/animation_plots.gif
   :width: 400
   :alt: Animation plots

Installation
------------

Make virtual environment with conda (optional):

.. code-block:: bash

    conda create -n simurg_plotter python=3.10
    conda deactivate
    conda activate simurg_plotter

Install `poetry`:

.. code-block:: bash

    pip install poetry

Install project:

.. code-block:: bash

    poetry install

Support
-------

If you are having issues, please let us know.
We have a mailing list located at: artemvesnin@gmail.com

License
-------

The project is licensed under the MIT license.
