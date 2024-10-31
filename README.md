# Documentación ejercicio GitHub
Esta es la documentación paso por paso del ejercicio de **creación y gestión** de un **repositorio** en **GitHub**. 

*Ejercicio hecho por **Guillermo** y **Karen***

## 1. Crear el repositorio en GitHub
El primer paso es **crear** el repositorio. Para ello se debe acceder tu perfil de **[GitHub](https://github.com/)** y entrar donde dice **Repositories** (o *Repositorios* en español).

![Captura de pantalla del apartado "Repositorios" de GitHub](https://i.imgur.com/HfHbcHg.png)

Una vez estamos en la parte de nuestro repositorios, debemos ir a la parte derecha y entrar donde dice **New** (*Nuevo*).

![Captura de pantalla del apartado "New" de tus repositorios en GitHub](https://i.imgur.com/4aUM0Q2.png)

### Configuración del repositorio

Una vez estamos en el apartado de creación del nuevo repositorio, debemos ponerle un **nombre**, una **descripción** (opcional) y elegir si queremos que nuestro repositorio sea **público** o **privado**. 

- Si lo hacemos **público**, cualquier persona podría ver el contenido de dicho repositorio.

- Si lo hacemos **privado**, solo la persona que crea el repositorio, colaboradores del mismo o personas con acceso autorizado podrán ver lo que contiene.

### Opciones de creación del repositorio

Después de haber puesto un *nombre*, una *descripción*, y escoger entre *público* o *privado*, se nos abre una nueva página donde lo primero que nos dicen es si queremos añadir **colaboradores** en nuestro repositorio. No hay que hacerlo necesariamente ahora, ya que mas adelante se pueden añadir desde el apartado de *Ajustes* del repositorio. 

Más adelante, nos da diferentes opciones a la hora de crear el repositorio:

- **Crear** el nuevo repositorio en nuestra **consola de comandos**, usando los siguientes comandos:

	`echo "# ejemplo" >> README.md`
	`git init`
	`git add README.md` 
	`git commit -m "first commit"`
	`git branch -M main`
	`git remote add origin https://github.com/guillermopereez/ejemplo.git`
	`git push -u origin main`

- **Importar** un repositorio ya creado, usando los siguientes comandos:
	`git remote add origin https://github.com/guillermopereez/ejemplo.git`
	`git branch -M main`
	`git push -u origin main`
- O la opción que vamos a usar en este ejercicio que es **clonando** el repositorio en nuestra **máquina local**. Para ello vamos a usar los siguientes comandos:
	`git clone [url]`
	`git add archivo.txt`
	`git commit -m "Primer commit"`
	`git push origin main`

Una vez hecho esto, ya tendríamos nuestro repositorio listo para empezar a trabajar.
## 2. Creación de Ramas y Pull Request
Una vez está creado el repositorio, vamos a crear dos **ramas**, una para cada archivo.
### Creación de la primera rama
La primera **rama** es para la parte de la listas de amigos, y se **crea** usando el siguiente **comando**:
![Captura del comando para crear una rama](https://i.imgur.com/h5yCHj9.png)
Y ahora para **entrar en la rama**, usamos este comando:
![Captura del comando para entrar en una rama](https://i.imgur.com/8I2dXni.png)
Una vez estamos en la rama. podemos empezar a hacer los **cambios** en el **archivo**. En este caso, voy a poner los **nombres** y los *supuestos* **números** de teléfono de 3 amigos:
![Captura de los datos introducidos en el archivo](https://i.imgur.com/JTPLO5v.png)

Una vez hechos los cambios los guardamos usando el comando `git add nombre_archivo.txt` y hacemos el [commit](https://github.com/guillermopereez/ejercicio_github_guillermo_y_karen/pull/1/commits/dd329f637f9dd886a9883cdb4ed538560081a25d) con  `git commit -m "texto del commit"` .

Ahora, para poder **subir** este cambio desde nuestro repositorio local a GitHub, usamos el siguiente comando:
![Captura del comando para subir los cambios](https://i.imgur.com/bJTjA6o.png)


### Pull Request

Ahora, al hacer el *push* hacia el repositorio remoto, en GitHub saltará un aviso de un **Pull Request**:
![Captura del Pull request](https://i.imgur.com/M9QxPDw.png)

Aquí, los demás **colaboradores** de mi repositorio podrán **votar** si el cambio que estoy proponiendo les parece bien y podrán **comentar** al respecto. Una vez se haya **votado** y aceptado el cambio, los cambios pasarán a la rama **main**.

### Creación de la segunda rama
La segunda **rama** es para la parte de los cuentos, y se **crea**  y se accede usando los mismos **comandos** que para la primera:
![Captura de la creación de la rama](https://i.imgur.com/r81FX2C.png)

Una vez estamos en la **rama**, igual que en la anterior, hacemos los **cambios** pertinentes en el **archivo**, que en este caso es añadir **dos párrafos** de un **cuento**, y usamos los mismos comandos que antes: `git add`,
![Captura de añadir comandos](https://i.imgur.com/Io50J1u.png)
y [`git commit`](https://github.com/guillermopereez/ejercicio_github_guillermo_y_karen/commit/b4042fb9e931b31f358a95659c6d2c3cb60eafec).

Ahora, para poder **subir** este cambio desde nuestro repositorio local a GitHub, usamos el siguiente comando:
![Captura de comando push](https://i.imgur.com/ypdWNLt.png)

### Pull Request

Ahora, al igual que en la primera rama, al hacer el *push* hacia el repositorio remoto, en GitHub saltará un aviso de un **Pull Request**:
![CAptura pull request](https://i.imgur.com/lO7jj6g.png)

Y aquí esta el **Pull Request** una vez **resuelto**:
![Captura pul request resuelto](https://i.imgur.com/JTODsaV.png)

## 3. Resolución de conflictos

Para esta parte vamos a crear dos nuevas **ramas** para hacer cambios en el archivo que previamente había editado el compañero. 

### Primer conflicto

El primer **conflicto**  consistía en que Guillermo editara la parte de Karen, es decir, el archivo **cuentos.txt**.
Para ello, se creó una rama llamada **cambios_guillermo_cuentos** y se hicieron los siguientes cambios:
![Conflicto cuentos](https://i.imgur.com/FkbSy5b.png)
En este caso, lo que decidimos fue quedarnos con todos los cambios de la nueva rama, quedando así el archivo después del **merge**:
`NO ME GUSTAN LOS CUENTOS`
`EL LOBO PUSO SU CESTA EN LA HIERBA Y SE ENTRETUVO CONGIENDO FLORES: -EL LOBO SE HA IDO- PENSÓ, NO TENGO NADA QUE TEMER. LA ABUELA SE PONDRÁ MUY CONTENTA CUANDO LE LLEVE UN HERMOSO RAMO DE FLORES ADEMÁS DE LOS PASTELES.`

Y, para dejar constancia de ello, se realizó un **[commit](https://github.com/guillermopereez/ejercicio_github_guillermo_y_karen/commit/ac433bf6f45a4e288d0815ba7abdf89a8a7aa84e)**.

### Segundo conflicto

El segundo **conflicto**  consistía en que Karen editara la parte de Karen, es decir, el archivo **lista_amigos.txt**.
Para ello, se creó una rama llamada **cambios_karen_amigos** y se hicieron los siguientes cambios:

 - Añadir apellidos a todos los amigos y agregar nuevos amigos en la rama **main**.
 - Eliminar un amigo (*Carlos*) y añadir uno nuevo (*Sonia*) en la rama **cambios_karen_amigos**.

Después de hacer estos **cambios**, se trato de hacer el **merge**, dando como resultado el siguiente conflicto:
![conflicto amigos](https://i.imgur.com/Ag13mfi.png)

Este **conflicto** se solucionó **eliminando a Carlos** y **agregando los nuevos amigos**.
Y para dejar constancia de ello, se realizó un **commit**:
![commit final](https://i.imgur.com/xgISJOQ.png)
