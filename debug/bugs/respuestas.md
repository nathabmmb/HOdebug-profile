Debug:

Corriendo segfault sin -g solo me tiró el error al final que fue un poquito más descriptivo, pero no mucho más...
No me deja ir pasito a pasito... me deja solo iniciar el programa y al darle "continue" muere con el error :D

Corriendo segfault con  -g: Al menos me dice cual es la linea en la que se produce el error.

Corriendo segfault con -Wall: Sugiere que a y b podrían no estar inicializadas! (me guía hacia el problema!). El problema en realidad era que no estaban definidos los tamaños de los arrays a y b :)

Resulta ser que eso era solo un parche. Luego descubrí yendo step by step que los for loops hacían demasiadas vueltas, y cargaban valores _random_ en las matrices a y b. Leyendo el código encontré que en los loops la condición estaba mal escrita (<= n+1 VS < n).


