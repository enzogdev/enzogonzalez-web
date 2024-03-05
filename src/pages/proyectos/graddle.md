---
layout: 'src/layouts/ProyectLayout.astro'
title: 'Graddle'
link: 'https://graddle.vercel.app/'
description: 'Herramienta para crear degradados en css con una interfaz drag and drop muy sencila'
introduction: ''
sections: ['tecnologías', 'mockups', 'desarrollo']
image:
  url: '\assets\projects\graddle.webp'
  alt: 'El logotipo completo de Astro.'
tags: ['webapp', 'side project', 'tool design']
---

## Tecnologías

REACT / TYPESCRIPT / ZUSTAND / GIT / SHADCN UI

Para el desarrollo de este proyecto decidí utilizar herramientas que ya conocía así como alguna nueva como **Zustand** para el gestor de estado ya que había oido que era mas ligero en comparación con el clásico **Redux**. En una fase inicial decidí optar por una libreria de componentes como **Shadcn ui** para simplificar el proceso de creación de la interfaz, ya que trae todos los componentes que iba a necesitar y la opcion de solo importar los que se utilizan era algo que necesitaba para aligerar la carga del proyecto

## Mockups

Ya que la concepción del proyecto la tenia clara y era algo de cuestión personal decidí volcar directamente las ideas en un **Figma** para poder encontrar los posibles problemas que tuviese mi planteamiento.

![captura de pantalla de figma con los mockups de graddle](/assets/projects/graddle.webp)

## Desarrollo

Tras crear la estructura de la interfaz a base de componentes jsx tocaba darles la funcionalidad, para lo cual empecé creando el sistema de estados mediante el cual requería leer y escribir la información de la posicion y los colores determinadosdesde varios puntos de la aplicacion, p.e. al mover un punto de color del canvas tengo que actualizar la nueva posición y generar el css necesario para que los cambios se vean reflejados. así como en la lista para ordenar dichos puntos. Al ser un sistema bastante complejo, el hecho de haber utilizado zustand me facilitó la legibilidad en el código sin tener que crear complejos slices etc.

Por otra parte, ya que no quería guardar ningún tipo de dato no ví necesario crear un backend ya que este solo se utilizaría en cualquier caso para almacenar los degradados generados y compartirlos. Así que lo dejé para una posible futura actualización

Una de las partes más interesantes fué la gestión del color y los calculos necesarios para transformar entre las distintas nomenclaturas (HEXA, HSLA, etc..) así como pintar el area de selección de color, algo que aparentemente resulta sencillo pero tiene su miga.
