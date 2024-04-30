=====================
Матричная клавиатура
=====================

В этом уроке мы создадим матричную клавиатуру с помощью Arduino UNO. Матричная клавиатура - это тип клавиатуры, в которой кнопки соединены в матрицу из рядов и столбцов. Это эффективный способ подключения нескольких кнопок к Arduino с использованием минимального количества пинов. Для выполнения работы мы будем использовать сайт https://www.tinkercad.com , который имеет инструментарий для работы платы микроконтроллера Arduino UNO, но если у вас есть набор-комплект Ардуино вы можете собрать его самостоятельно по этому уроку. Для работы на сайте вам понадобиться

1. Зарегестрироваться на сайте

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
