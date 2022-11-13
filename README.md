# Navigation
## Normal mode
`h` - влево

`j` - вниз

`k` - вверх

`l` - вправо

`^` `0` - перемещение в начало строки

`$` - перемещение в конец строки

`w` - перемещение в начало следующего слова

`e` - перемещение в конец слова, если курсор в конце, то в конец следующего слова

`b` - перемещение в начало слова, если курсор в начале слова, то в начало предыдущего слова

`<Shift-g>` - перемещение в конец файла

`<String number> <Shift-g>` - перемещение в указанную строку

`gg` - переход в начало файла

## Insert mode
`<Esc>` `<Ctrl-[>` - выход в Normal mode


# Save and Exit
## Normal mode
`:q!` - выход без сохранения

`:wq` - выход с сохранением

`:w <filename>` - запись в файл filename. Если есть выделение то сохранится часть файла (должна быть метка внизу :'<,'>w)


# Insert
# Normal mode
`:r filename` - вставка из файла под курсором

`:r !<Command>` - вставка результата выполнения команды


# Edit
## Normal mode
`x` - удаление символа под курсором

`i` - вставка перед курсором

`a` - вставка после курсора

`A` - вставка в конец строки

`dw` - удаление слова от символа под курсором до конца слова, включая пробел, не включая знаки препинания

`de` - удаление от символа под курсором до конца слова, не включая пробел

`d$` - удаление от символа под курсором до конца строки

`d^` - удаление от симовла перед курсором до начала строки

`dd` - удаление строки

`u` - отмена предыдущей команды

`U` - отмена во всей строке

`<Ctrl-r>` - отмена отмены

`p` - вставка, если вставляется целая строка, то вставится на следующей строке, если слово то перед кусором

`r<Symbol>` - заменяет сивол под курсором на Symbol

`R<Symbol>` - замена более одного символа

`ce` `cw` - удаление от курсора, включая символ под курсором, до конца слова и переход в Insert mode

`cb` - удаление от курсора до начала слова, не включая символ под курсором, и переход в Insert mode

`c0` `c^` - удаление от курсора до начала строки, не включая символ под курсором, и переход в Insert mode

`c$` - удаление от курсора, включая символ под курсором, до конца строки и переход в Insert mode

`o` - вставка строки под курсором и переход в Insert mode

`O` - вставка строки над курсором и переход в Insert mode

`yy` - копирование строки

`y` - копирование выделенного фрагмента (в Visual mode)

`yw` - копирование слова, можно комбинировать н с другими символами - e, $ и т.д.


# Info
## Normal mode
`<Ctrl-g>` - информация о файле и местоположении в нем


# Searching
## Normal mode
`/<word>` - поиск вперед

`n` - повтор поиска в прямом направлении

`<Shift-n> - повтор поиска в обратном направлении

`?<word>` - поиск назад

`<Ctrl-o` - переход назад

`<Ctrl-i` - переход вперед

`%` - поиск парной скобки для скобки под курсором


# String replace
## Normal mode
`:s/before/after` - замена первого вхождения в текущей строке

`:s/before/after/g` - замена всех вхождений в текущей строке

`:#,#s/before/after/g` - замена всех вхождений между строками # и #

`:%s/before/after/g` - замена всех вхождений в файле

`:%s/before/after/gc` - замена всех вхождений в файле с запросом подтверждения замены


# External commands
## Normal mode
`:!<Command>` - выполнение внешней команды


# Parameters
## Normal mode

`<:set <Parameter>` - установка параметров

`ic` `ignorecase` - игнорирование регистра при поиске
  
`is` `incsearch` - отображение частичных совпадений при поиске
  
`hls` `hlsearch` - подсветка всех совпадений при поиске
  
`noic` `` - no отключает параметр

# Help
## Normal mode
`<F1>` `:help` - вызов справки

`:q` - закрыть окно справки

`:help w` - вызов справки по команде
