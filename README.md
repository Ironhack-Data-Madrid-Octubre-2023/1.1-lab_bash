* Imprime en consola `Hello World`.

echo hello world

* Crea un directorio nuevo llamado `new_dir`.

mkdir new_dir

* Elimina ese directorio.

rm -rf new_dir

* Copia el archivo `sed.txt` dentro de la carpeta lorem a la carpeta lorem-copy. TIP: Puede ser necesario crear la carpeta lorem-copy primero.

mkdir lorem-copy
cd lorem
cp sed.txt /Users/joaquin/Developer/Iron_Hack/01/1.1-lab_bash/lorem-copy


* Muestra el contenido del archivo `sed.txt` dentro de la carpeta lorem.

cd lorem
cat sed.txt

* Muestra el contenido de los archivos `at.txt` y `lorem.txt` dentro de la carpeta lorem.

cat at.txt
cat lorem.txt

* Visualiza las primeras 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy

cd ..
cd lorem-copy
head -3 sed.txt

* Añade `Homo homini lupus.` al final de archivo `sed.txt` dentro de la carpeta lorem-copy.

echo homo homini lupus >> sed.txt

* Visualiza las últimas 3 líneas del archivo `sed.txt` dentro de la carpeta lorem-copy. Deberías ver ahora `Homo homini lupus.`.

tail -3 sed.txt

* Encuentra al usuario activo en el sistema.

w

* Encuentra dónde estás en tu sistema de ficheros.

pwd

* Lista los archivos que terminan por `.txt` en la carpeta lorem.

cd ..
cd lorem
find . -name '*.txt'

* Cuenta el número de líneas que tiene el archivo `sed.txt` dentro de la carpeta lorem.

wc -l sed.txt

* Cuenta el número de **archivos** que empiezan por `lorem` que están en este directorio y en directorios internos.

find . name "lorem*" | wc -l

* Cuenta el número de apariciones del string `et` en `at.txt` dentro de la carpeta lorem.

cd lorem
grep -o "et" at.txt | wc -l
cd ..


## Ficheros bash

Cualquier comando o comandos de bash se pueden almacenar en un fichero y ejecutar cuando queramos.
Obviamente puedes utilizar tu editor preferido. Creamos el fichero:
```
$ touch list_files.sh
```

E incluimos el contenido que queramos. En este caso listar ficheros:
```bash
#!/bin/bash
ls
```

Ejecutamos el script:
```
$ bash list_files.sh
```

Y veremos por consola el siguiente output.
```console
README.md lorem solutions.ipynb
```
touch list_files.sh
#!/bin/bash
echo "ls" >> list_files.sh
sh list_files.sh