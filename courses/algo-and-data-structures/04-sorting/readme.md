# Сортировка  

Алгоритм сортировки — это алгоритм для упорядочивания элементов в списке. У сортировки элементов списка очень много   
применений, начиная со словарей, где слова отсортированы в алфавитном порядке, заканчивая огромными базами данных, где   
без сортировки поиск элементов занял бы очень много времени.


Давай рассмотрим один из самых простых видов сортировки - selection sort.
Алгоритм данной сортировки прямолинейный:
1. Если в списке 1 элемент, ничего не делаем, так как список с 1 элементом является отсортированным по определению.
1. Из всего списка ищем минимальный элемент и ставим его на начало списка.
1. Перемещаем начало списка на один элемент правее предыдущего и возвращаемся к первому шагу.
