# Escape Ratonil by Jonatandb

<p align="center"><img src="./Screenshot_EscapeRatonil_Jonatandb.gif" alt="Escape Ratonil by Jonatandb"></p>

---
### Agregado:
- Movimiento continuo
- Movimiento por turnos
- Capacidad de colisionar con los objetos del entorno

---


##### Pasos a ejecutar en Unity 2021.3.27f1 para crear un proyecto básico de VR con XR Iteraction Toolkit:

- Crear proyecto "3D"

- File -> Build Settings:
	- Elegir Andorid y click en Switch Platform
	- Elegir Texture Compression -> ASTC
	- Cerrar ventana (los cambios se guardan automáticamente)

- Edit -> Project settings:
	- XR Plug-in Management -> Install
	- En Mac, Linux, Windows -> Tildar Oculus
		* Esto es útil para vincular el Oculus por AirLink o cable y poder probar el juego
			desde Unity sin tener que instalarlo en el Oculus (También permite debugging)
	- En Andorid Settings -> Tildar Oculus
	- Cerrar ventana (los cambios se guardan automáticamente)

- Instalación de XR Interaction Toolkit (para poder usar los touch y movernos por la escena):
	- Window -> Package Manager -> Click en el + y elegir Add package by name
		- Escribir: com.unity.xr.interaction.toolkit
		- Click en Add (Se instalará y pedirá reiniciar el proyecto, click en Ok)
		- Luego click en la sección Packages -> XR Interaction Toolkit -> Samples y click en Import junto a "Starter Assets"

- Ir desde el panel "Project" a la carpeta de Assets: Assets\Samples\XR Interaction Toolkit\2.4.0\Starter Assets
	- Seleccionar "XRI Default Left Controller"
		- En el panel "Inspector" click en -> "Add to ActionBasedController default"
	- Seleccionar "XRI Default Right Controller"
		- En el panel "Inspector" click en -> "Add to ActionBasedController default"

- Ir al menú Edit -> Project Settings -> Preset Manager:
	- Escribir Right en el campo vacío junto a "XRI Default Right Controller"
	- Escribir Left en el campo vacío junto a "XRI Default Left Controller"
	- Cerrar ventana (los cambios se guardan automáticamente)

- Ir al panel "Hierarchy":
	- Click derecho en un espacio vacío -> Click en XR -> XR Origin VR (Se añade a la escena)
	- Elegir un nombre, por ej: Player
	- Expandir nodo -> expandir Camera Offset -> click en Left y Right Controller y verificar
		en el panel Inspector al clickearlos que en la sección XR Controller (Action based)
		aparezcan tildados los casilleros y en casi todos ellos diga "XRI LeftHand...."
	*	Con esto detectará automáticamente cuando presione un botón, mueva el joystick, etc.

- Añadiendo un suelo:
	- Click derecho en un espacio vacío -> Click en 3D Object -> Plane
	- En el panel Scene -> click y mover hacia abajo el plano un poco
		para que no quede pegado al player, sino más abajo

- Añadiendo detección de "inputs":
	- Click en el XR Origin (player)
	- En el panel de Inspector -> click en Add Component -> Escribir y seleccionar "Input action manager"
	- Abrir la sección "Action Assets" y clickear en el botón circular de la derecha para seleccionar
		un asset, doble click en "XRI Default Input Action"

- Desactivación de audio listener de la cámara principal:
	- En Hierarchy seleccionar Main camera
	- Inspector destildar abajo de todo: "Audio Listener"
	- Grabar los cambios con Ctrl+s

- Probando que funcione todo bien:
	- Simplemente vincular el Oculus con link (por cable o wifi)
		Una vez conectado a la PC, presionar el botón Play en Unity
		Se debe ver en el Oculus inmediatamente el entorno virtual recién creado :-)

---

### Referencias:
- [Crea un juego VR en Unity | Configura tu primer proyecto | XR Interaction toolkit | Oculus Quest](https://www.youtube.com/watch?v=apL9lIkKLHQ) (Gracias a MadAcorn! 🙏🏻)
- [Crea un juego VR en Unity | Movimiento continuo del jugador | XR Interaction toolkit | Oculus Quest](https://www.youtube.com/watch?v=706Bx0hutM0) (Gracias a MadAcorn! 🙏🏻)

