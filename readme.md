Добрый день! Как работают программы:

1. Для начала, все классы у меня расположены в отдельных .py файлах для удобства - это файлы RadialPoint и RoomSnapshot

2. RotateRoom.py
   
    - читает файл csv, в котором находятся считаные лидаром реальные координаты комнаты
   
    - поворчивает эту комнату на указанный угол (угол может быть отрицательным)
 
    ![Пример работы программы 1](https://github.com/novik1908/UpdatedCodeSamples/raw/master/images/primer2_1.png)
    ![Пример работы программы 1](https://github.com/novik1908/UpdatedCodeSamples/raw/master/images/primer2_2.png)
3. VisualizeAllCoordsInDirectoryFronmTXT.py

    - читает все файлы txt с координатами в указанной директории(папке)
   
    - переводит координаты из радиальной системы исчисления в нормальную
   
    - на выбор выводит данные на консоль либо рисует получившуюся фигуру в mathplotlib

    ![Пример работы программы 1](https://github.com/novik1908/UpdatedCodeSamples/raw/master/images/primer3.PNG)
4. VisualizeVisorCoordsFromCSV.py

    - снимает значения из указанного файла csv (то, что снял лидар в реальной жизни), конвертирует координаты из из радиальной системы исчисления в нормальную и выводит результат на выбор: консоль либо визуально в mathplotlib

    ![Пример работы программы 1](https://github.com/novik1908/UpdatedCodeSamples/raw/master/images/primer4_1.png)
    ![Пример работы программы 1](https://github.com/novik1908/UpdatedCodeSamples/raw/master/images/primer4_2.png)

5. RealTimeRoomTracker.py
    - отслеживает положение комнаты в данный момент с определенным фреймрейтом

    - позволяет пользователю переместить ось координат вверх/вниз/вправо/влево с возможностью масштабирования

 
Прим.: 
1. В каждом файле csv - 5тыс. точек, первые версии программы очень долго обрабатывали такое количество, теперь обработка занимает примерно 0,5сек (считал с помощью библиотеки time)

2. Лидар - прибор, который показывает границы объектов, например границы комнаты, в которой он находится, в радиальной системе координат (угол, длина) и выводит результат в файл любого формата (я использовал txt и csv)
