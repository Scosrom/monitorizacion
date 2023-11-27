## PROCESOS

``` 
top -b -n 3 >top.info

```

-b para realizar captura.
-n 3 es para hacer 3 refrescos.

``` 
top -b -n 3 -o %CPU -U 2asir | awk 'NR>=5 && NR<=15' > salida_top_sandra.txt
```
-o %CPU

Esta opción ordena la salida de top según el porcentaje de uso del CPU. 

-U 2asir:

Esta opción filtra la salida de top para mostrar solo los procesos del usuario "2asir". 