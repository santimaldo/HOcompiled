1. **Escriban qué esperan de cada uno de los pasos**  
paso 1 - *Pre-procesamiento*: obtener un archivo en el que se muestran las funciones usadas de librerias externas, y los errores que haya cometido en el main.  
paso 2 - *Compilacion I*: Obtener un codigo de assembler, en el cual se omptimiza el programa.  
paso 3 - *Compilacion II*: Obtener un archivo binario, en codigo maquina, pero que todavia no sabe donde de donde sacar las funciones.  
paso 4 - *Linkeo*: Obtener un ejecutable, el cual ya sabe de donde sacar las funciones.  
2. **¿Qué agregó el preprocesador?**

Agrego muchas lineas al principio dejando al final el main, tal cual estaba.  
Las lineas del principio tienen variables y funciones externas.  
*NO me tira errores del main*  

3. **Identificar en la rutina de assembler las funciones**  

Las funciones que reconoci en la rutina assembler son:  

Funcion que imprime en pantalla:  
```
.LC0:
	.string	"I know how to add! 31 + 11 is %d\n"
	.text
	.globl	main
	.type	main, @function
```  

funcion que suma los numeros:  
```
.LFE0:
	.size	main, .-main
	.globl	add_numbers
	.type	add_numbers, @function
```


4. **Explicar qué quieren decir los símbolos que se crean en el objeto**  
5. **¿En qué se diferencian los símbolos del objeto y del ejecutable?**
