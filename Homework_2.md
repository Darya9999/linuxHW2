Task №2
Задание: Используя команду cat, создать два файла с данными, а затем объединить их. Просмотреть содержимое созданного файла. Переименовать файл, дав ему новое имя. Создать несколько файлов. Создать директорию, переместить файл туда. Удалить все созданные в этом и предыдущем задании директории и файлы. Создать файл file1 и наполнить его произвольным содержимым. Скопировать его в file2. Создать символическую ссылку file3 на file1. Создать жесткую ссылку file4 на file1. Посмотреть, какие айноды у файлов. Удалить file1. Что стало с остальными созданными файлами? Попробовать вывести их на экран. Дать созданным файлам другие, произвольные имена. Создать новую символическую ссылку. Переместить ссылки в другую директорию.

Результат: Текст команд, которые применялись при выполнении задания. Присылаем в формате текстового документа: задание и команды для решения (без вывода). Формат - PDF (один файл на все задания).

Solution №2
Используя команду cat, создать два файла с данными
cat > data_file_1.txt
This is data file number 1
CTRL+D

cat > data_file_1.txt
And this onether one data file
CTRL+D


А затем объединить их
cat data_file_1.txt data_file_2.txt > combined_data_file.txt


Просмотреть содержимое созданного файла
cat combined_data_file.txt


Переименовать файл, дав ему новое имя
mv combined_data_file.txt new_combined_data_file.txt
Создать несколько файлов
touch file1
touch file2
touch file3


Создать директорию
mkdir dir1


Переместить файл туда
mv file1 ~/Homeworks/Task_2/dir1


Удалить все созданные в этом и предыдущем задании директории и файлы
cd ~
rm -r Homeworks
Создать файл file1 и наполнить его произвольным содержимым
cat > file1
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
CTRL+D


Скопировать его в file2
cp file1 file2


Создать символическую ссылку file3 на file1
ln -s file1 file3


Создать жесткую ссылку file4 на file1
ln file1 file4


Посмотреть, какие айноды у файлов
ls -i
790281 file1  790672 file2  789741 file3  790281 file4


Удалить file1
rm file1
Что стало с остальными созданными файлами?
ls -i
790672 file2  789741 file3  790281 file4
file3 стал помечен красным, и его содержимое пусто. Остальные файлы не изменились.


Дать созданным файлам другие, произвольные имена
mv file2 new_file_two
mv file3 new_file_three
mv file4 new_file_four


Создать новую символическую ссылку
ln -s new_file_four new_softlink_file_four


Переместить ссылки в другую директорию
mv new_softlink_file_four ~/Homeworks/new_dir