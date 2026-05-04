# Ejercicio 1 – Docker Compose

## 1. Errores detectados

Error 1: Red mal definida
El servicio hacía referencia a una red con un nombre diferente al definido:

net_devXX (mal)
net_dev_XX (correcto)

Docker Compose no podía encontrar la red y daba error al ejecutar el archivo.


## Error 2: falt de un comando, que es el siguiente: 

command: tail -f /dev/null



## Error 3: Uso de atributo obsoleto

El archivo incluía:

version: "3.8"

Docker mostraba un aviso indicando que este atributo está obsoleto, para resolverlo lo elimino.


## Error 4: Puerto expuesto sin servicio
Se definía un puerto:

8090:3000

Pero dentro del contenedor no había ninguna aplicación funcionando en ese puerto.

No era posible acceder desde el navegador. Se elimina la parte del puerto



# 2. Pasos para el funcionamiento

Paso 1: Ejecutar el contenedor
docker compose up -d



Paso 2: Comprobar estado
docker compose ps

El contenedor debe estar en estado "Up".


Paso 3: Acceder al contenedor
docker exec -it srv_dev_XX bash



Paso 4: Verificar volumen. Esto se realiza para comprobar la persistencia del volumen, de manera que al salir del contenedor, comprobar que el archivo persiste al volver a entrar. 

ls /var/empresa

Crear archivo:
echo "Prueba de volumen persistente" > /var/empresa/prueba.txt

Comprobar:
ls /var/empresa
cat /var/empresa/prueba.txt



Paso 5: Comprobar persistencia
docker compose down
docker compose up -d

Entrar de nuevo:
docker exec -it srv_dev_XX bash

Verificar:
ls /var/empresa
cat /var/empresa/prueba.txt


Resultado final

- El contenedor funciona correctamente
- La red está bien configurada
- El volumen es persistente
- El sistema funciona correctamente tras las correcciones