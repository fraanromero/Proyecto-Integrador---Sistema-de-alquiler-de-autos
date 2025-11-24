# Proyecto-Integrador-LSI-en-C
#---Sistema-de-alquiler-de-autos

#Dscripción breve del proyecto
##creación de un Sistema de Alquiler de Vehículos que facilita la gestión eficiente de la disponibilidad de automóviles para los clientes. El sistema presentará al usuario una selección completa de vehículos disponibles, permitiendo aplicar filtros por marca, modelo, color y tipo de alquiler: ya sea por día, semana o mes, dependiendo de la disponibilidad real del automóvil.

##Ejecución
1. Asegurarse de que todos los archivos estén en la misma carpeta.
2. Abrir el archivo llamado menuAlquiler.c
3. Compilar ese archivo, y luego ejecutar.

##Uso
1. Si el archivo archivoAutos.dat no está en la misma carpeta que el archivo autosAlquiler.c al momento de eejcutarse, el programa lamará a una función que genera 20 vehículos que ya estaban cargados en el sistema previamente.
2. El programa muestra una lista de opciones: menuPrincipal(), donde el usuario puede seleccionar:
   a) alquilar un vehiculo.
   b) buscar vehículos.
   c) ver reportes y listados.
    d) salir del programa.
3. Cuando el usuario confirma el alquiler, el programa actualiza el registro y vuelve a grabarlo en el archivo:
 aux.estado =1;
 fseek(archivosAutos, pos, SEEK_SET);
 fwrite(&aux, sizeof(vehiculo), 1, archivoAutos);
4. Según el tipo de alquiler del vehiculo, por ejeplo aluila por dia o por semana, el archivo ejecutará:
total = dias * aux.PrecioDia;
o
total = semana * aux.PrecioSemana;
5. Si el usuario hace por ejemplo el pago del alquiler en efectivo, el sistema le calcula cuanto le
quedará el precio final con el descuento del 10%:
total = total - (total * 0.10);
6. Para mostrar los estados y las estadisticas de los vehiculos, el corte de control para
generar estos reportes, recorre el archivo completo y obtiene la cantidad de autos y camionetas alquiladas,  y la cantidad de vehiculos que etán disponibles:
while (fread(&aux, sizeof(vehiculo(, 1, archivoAutos)){
 #acá se cuentan los autos alquilados o disponibles por tipo (auto o camioneta)
}

##Autores
Romero Fernández Rubén Tiburcio. 
Romero, Matías Luciano. 
Romero, Franco Exequiel. 
Sandoval, Diego Ulises. 

