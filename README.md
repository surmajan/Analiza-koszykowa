[README.md](https://github.com/user-attachments/files/33282447/README.md)
# Analiza koszykowa: Apriori, ECLAT i FP-Growth

Porównanie trzech algorytmów szukania reguł asocjacyjnych (które produkty klienci kupują razem) na transakcjach z Niemiec z 2011 roku ([Online Retail, UCI](https://archive.ics.uci.edu/dataset/352/online+retail)). Notebook zawiera też proste wyjaśnienie, jak działa każda metoda, i porównanie ich zalet oraz wad.

## Metody

| Metoda | Biblioteka | Min. support |
|:--|:--|:-:|
| Apriori | `mlxtend` | 0,05 |
| ECLAT | `pyECLAT` | 0,08 |
| FP-Growth | `mlxtend` | 0,06 |

## Wyniki

| Transakcje | Produkty | Częste zestawy (Apriori) | Reguły z lift ≥ 2,5 (FP-Growth) |
|:-:|:-:|:-:|:-:|
| 400 | 1644 | 86 | 10 |

Najsilniejsze powiązanie: dwa zestawy pudełek na przekąski (*Round Snack Boxes Set of 4 Fruits* i *Woodland*) trafiają razem do 14% koszyków, a lift wynosi ok. 3,2, czyli kupowane są razem ponad trzy razy częściej, niż wynikałoby z przypadku.

## Uruchomienie

```bash
pip install -r requirements.txt
jupyter notebook projekt_basket-2.ipynb
```

Interaktywny widżet (`ipywidgets`) i wykres `plotly` działają tylko po uruchomieniu notebooka lokalnie.
