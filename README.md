# Cómo Instalar tu propio nodo de Bitcoin y Lightning Network

Un nodo de Bitcoin puede usar las siguientes redes:

* Mainnet: Es la red principal donde están los bitcoins reales (peso de la blockchain 460 GB aproximadamente en el momento de hacer esta guía).
* Testnet: Es una red parecida a mainnet pero para hacer pruebas.(peso de la blockchain menos de 50 GB)
* Regtest: Es una red local en la cual puedes crear varios nodos en la misma máquina.

La recomendación es usar la red de testnet para aprender y no arriesgar satoshis reales.

Si vas a instalar un nodo de testnet sólo para probar y quieres hacerlo en el pc que usas habitualmente solo debes asegurarte que tengas mas de 50 GB de espacio disponible.

Cuando quieras usar un nodo en producción o sea en mainnet,  lo más aconsejable es destinar una cpu para tal efecto, y  debes si o si tener un disco adicional debido al peso actual de la cadena de bloques.



## Requisitos

### Hardware
Los requisitos para instalar un nodo de Bitcoin son particularmente bajos, el recurso más costoso para almacenar la cadena de bloques de la red de mainnet sería el disco duro ya que actualmente pesa 460 GB aproximadamente. 
Si el nodo se va usar sólo para pruebas en red de testnet solo es necesario tener 50 GB de espacio en disco.

A continuación se detallan cuáles serían los requisitos mínimos:

*  CPU con procesador corei3 o similares en adelante. También puede ser una raspberry pi 4. 
*  Memoria: Mínimo 4 GB
* Disco duro de 1 Tera SSD 



### Software
Debes tener instalada una distribución Linux basada en Debian preferiblemente Ubuntu.

Debes añadir un usuario diferente a root para la instalación de los nodos, en caso de que no lo tengas aquí te muestro como:

```
$adduser tusuario
$usermod -aG sudo tusuario
```

luego te loggeas con:

```
$su tusuario
$cd ~
```

## Instalando un nodo de Lightning Network 

Se eligió la simpleza y el desempeño, por eso el nodo de Bitcoin será Bitcoin Core, para el nodo de lightning se usará Core Lightning y para que los nodos de lightning externos se puedan comunicar usaremos tor como proxy.

### [Tutorial de Instalación de CLN usando Bitcoin Core y tor ](https://hackmd.io/NR3XXnAISbuqxC6fMr1FMQ?view)

### Instalación automática

Para ahorrarte trabajo escribí un script que ejecuta automaticamente todos los pasos del tutorial.
Abre una terminal y ejecuta los siguientes comandos:
```
$cd ~
$wget -O ln_installer.sh https://gist.githubusercontent.com/bitao36/be953bdea548f64d48ae50dcd9ecf2c0/raw/e526dd412184f257871817058c308d82d6834e4d/gistfile1.txt
$chmod +x ln_installer.sh
$./ln_installer.sh
```

