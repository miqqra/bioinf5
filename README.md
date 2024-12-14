# Предсказание и парное выравнивание структур белков

## Последовательность, используемые программы

- **Последовательность**:
  `MDADVISFEASRGDLVVLDAIHDARFETEAGPGVYDIHSPRIPSEKEIEDRIYEILDKIDVKKVWINPDCGLKTRGNDETWPSLEHLVAAAKAVRARLDK`
- **Программы-предсказатели**: `ESMFold`, `AlphaFold2`
- **Программа для выравнивания**: `CLICK`

## Полученные ноутбуки

- Файлы ноутбуков с предсказаниями структур:
    - [AlphaFold2.ipynb](./Копия_блокнота__AlphaFold2_ipynb_.ipynb)
    - [ESMFold.ipynb](./Копия_блокнота__Копия_блокнота__ESMFold_ipynb__.ipynb)

Посмотрел какие параметры можно настроить, выяснил, что в моём случае последовательность короткая, поэтому обычных
параметров достаточно.

## Предсказания структур в формате PDB

- Полученные структуры:
    - [esmfold-prediction.pdb](./esmfold.pdb)
    - [alphafold2-prediction.pdb](./alphafold.pdb)

## Выдача программы выравнивания

- **Формат mmCIF/другой**:
    - [esmfold-spatial-alignment.pdb.A.cif](./esmfold.pdb.A.cif)
    - [alphafold2-spatial-alignment.pdb.A.cif](./alphafold.cif)

## Проект/сессия из программы визуализации

- CLICK решил не работать (кидал 500 ошибки), сделал выравнивание с помощью jFATCAT-rigid, который и сделал визуализацию

## Снимки экрана / запись видео

![img.png](./img.png)

## Выводы о совпадении предсказаний

**RMSD (среднеквадратичное отклонение) = 1.03** — структуры похожи, но есть маленькие различия, особенно в гибких
частях.

**TM-score = 0.94** — высокий уровень сходства, модели почти одинаковы.

**Identity = 100%** — последовательности полностью совпадают.

**Aligned residues = 100** — все остатки совпали при выравнивании.

**Length и Modeled residues = 100** — обе модели полностью покрывают белок.

**Визуальное сравнение** — Альфа-спирали в обеих структурах почти полностью совпадают — они одинаково расположены и
выглядят устойчиво. Бета-листы тоже похожи друг на друга, расхождений почти нет. В петлях есть более значительные
расхождения, потому что они гибкие и сложнее поддаются точному предсказанию. В целом, структуры очень похожи, особенно в
стабильных частях.