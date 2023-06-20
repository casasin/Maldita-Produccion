# Preparando todo

Hay que tener unas cuantas cosas instaladas y actualizadas para que todo vaya bien. Son unos pasos sencillos y si algo no chuta, siempre podrás invitar a comer a tu amigo el informático.

## Instalando python3

Escribe en el **Terminal**: `which python3` y pulsa Enter.
Este comando comprueba si Python 3 ya está instalado. Si el Terminal responde con una ruta como `/usr/local/bin/python3`, entonces ya tienes la instalación y puedes continuar con la siguiente. Si la respuesta dice `python3 not found`, entonces necesitaremos instalarlo. 

En ese caso, obténgalo a través de una descarga desde [https://www.python.org/downloads/macos/](https://www.python.org/downloads/macos/) (desplácese hacia abajo y elija el instalador universal de macOS). Ábrelo, ejecuta el instalador y sigue las instrucciones en pantalla.

## Instalando pip3

Si tienes Python instalado, probablemente ya tengas pip3. `pip` es el *gestor de paquetes* para Python 3. Con él, puedes instalar complementos para Python 3, normalmente bibliotecas que te dan acceso a comandos adicionales de Python. Python tiene su propio comando para instalar pip:

`python3 -m ensurepip --upgrade`

Incluso si ya tienes instalado pip3, considera:

`pip3 install --upgrade pip`

…para asegurarte de que tienes la última versión.

Más sobre la instalación de `pip`: ![https://pip.pypa.io/en/latest/installation/#](https://pip.pypa.io/en/latest/installation/#)

## Instalando fonttools, brotli, zopfli, fontbakery

Ahora podemos usar pip3 para las siguientes instalaciones. Escribe:

```bash
pip3 install fonttools --upgrade
pip3 install brotli --upgrade
pip3 install zopfli --upgrade
pip3 install fontbakery --upgrade
```

Si las instalaciones con pip3 no funcionan, repite estas líneas con python3 -m pip al principio en vez de pip, así:

```bash
python3 -m pip install fonttools --upgrade
python3 -m pip install brotli --upgrade
python3 -m pip install zopfli --upgrade
python3 -m pip install fontbakery --upgrade
```

No hace está de más ejecutar este comando para una librería que ya está instalada, porque con el sufijo `--upgrade` comprueba el número de versión y actualiza a la última versión si procede.

## Preparando Glyphs

- Instalar la última versión de Glyphs.
- En "Window/Plugin Manager" desinstalar e instalar los Modules.
- En "Scripts", instalar los Mekkablue Scripts.
- En "Preferencias/Addons" escoger la versión de Python en la que pone "Glyphs".

