# Oписание проекта - Предсказание ядовитых грибов.

Данные взяты из kaggle-соревнования [Binary Prediction of Poisonous Mushrooms](https://www.kaggle.com/competitions/playground-series-s4e8). 

Набор данных для этого соревнования (как обучающий, так и тестовый) был создан на основе модели глубокого обучения, обученной на наборе данных [UCI Mushroom.](https://archive.ics.uci.edu/dataset/73/mushroom). В данные добавлены переменные, которых не было в оригинальном наборе данных.

## Данные

**Файлы**

- train.csv - обучающий набор данных
- test.csv - тестовый набор данных
- sample_submission.csv - образец файла для отправки в правильном формате

**Метрика:**  Matthews correlation coefficient (MCC).

**Описание переменных**

- `cap-shape` -> форма шляпки: bell=b,conical=c,convex=x,flat=f, kbbed=k,sunken=s
- `cap-diameter` -> диаметр шляпки в см
- `cap-surface` -> поверхность шляпки: fibrous=f,grooves=g,scaly=y,smooth=s
- `cap-color` -> цвет шляпки: brown=n,buff=b,cinnamon=c,gray=g,green=r, pink=p,purple=u,red=e,white=w,yellow=y
- `does-bruise-bleed` ->  после срезания грибы покрываются синяками или "кровоточат": bruises-or-bleeding=t,no=f
- `gill-attachment` -> крепление пластинок: attached=a,descending=d,free=f,tched=n
- `gill-spacing` -> расстояние между пластинками: close=c,crowded=w,distant=d
- `gill-color` -> цвет пластинок: black=k,brown=n,buff=b,chocolate=h,gray=g, green=r,orange=o,pink=p,purple=u,red=e, white=w,yellow=y
- `stem-height` -> высота стебля в см
- `stem-width` -> толщина стебля в мм
- `stem-root` -> корень стебля
- `stem-surface` -> поверхность стебля
- `stem-color` -> цвет стебля
- `veil-type` -> тип покрова: partial=p,universal=u
- `veil-color` -> цвет покрова: brown=n,orange=o,white=w,yellow=y
- `has-ring` -> наличие кольца
- `ring-type` -> тип кольца: cobwebby=c,evanescent=e,flaring=f,large=l, ne=n,pendant=p,sheathing=s,zone=z
- `spore-print-color` -> цвет спор: black=k,brown=n,buff=b,chocolate=h,green=r, orange=o,purple=u,white=w,yellow=y
- `habitat` -> среда обитания: grasses=g,leaves=l,meadows=m,paths=p, urban=u,waste=w,woods=d
- `season` -> сезон: spring=s, summer=u, autumn=a, winter=w

## Задача

Предсказать, будет ли гриб съедобным или ядовитым, исходя из его физических характеристик.

## Используемые библиотеки

*os*, *warnings*, *gc*, *math*, *pandas*, *matplotlib*, *numpy*, *seaborn*, *scipy*, *sklearn*, *statsmodels*, *phik*, *lightgbm*, *pytorch*

## Вывод

В результате проекта была разработана модель глубокого обучения по классификации, является ли гриб ядовитый или нет. В начале использовали RandomForestClassifier и уже на базовой модели достигли отличных результатов. Улучшили результат используя глубокое обучение. 
​
В дальнейшем проект можно улучшить выделив самые важные признаки, чтобы можно было определять ядовитость грибов зная меньше информации.