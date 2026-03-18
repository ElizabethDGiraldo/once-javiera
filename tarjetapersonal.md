# 📄 Documentación Técnica - Tarjeta Personal

## 📌 Descripción general
Este documento describe la estructura y decisiones semánticas utilizadas en el archivo **presentacion.html**, el cual representa una tarjeta personal con información básica, habilidades y datos de contacto.

---

## 🧠 Decisiones semánticas

Se eligieron etiquetas HTML semánticas para mejorar la accesibilidad, organización y comprensión del contenido tanto para usuarios como para navegadores.

### 🔹 `<!DOCTYPE html>` y `<html lang="es">`
- Define que el documento es HTML5.
- Se usa `lang="es"` porque el contenido está en español, lo que mejora accesibilidad y SEO.

### 🔹 `<head>`
- `<meta charset="UTF-8">`: Permite el uso correcto de tildes y caracteres especiales.
- `<meta name="viewport">`: Hace que la página sea adaptable a dispositivos móviles.
- `<title>`: Define el nombre de la página en la pestaña del navegador.

---

### 🔹 `<header>`
- Contiene el nombre y una frase representativa.
- Se usa porque representa la introducción principal del contenido.
- `<h1>`: Es el título principal (nombre).
- `<em>`: Se usa para dar énfasis a la frase personal.

---

### 🔹 `<main>`
- Contiene el contenido principal de la página.
- Mejora la accesibilidad al separar el contenido relevante del resto.

---

### 🔹 `<section>`
Se usan dos secciones para organizar la información:

#### 1. Sobre mí
- Explica quién eres.
- `<strong>` se usa para resaltar características importantes como *empírica y emprendedora*.
- `<time>` se usa para representar una fecha relevante (inicio de tu enfoque profesional).

#### 2. Habilidades y Pasatiempos
- Presenta tus intereses.
- `<ul>` y `<li>` organizan la información en lista.
- `<strong>` resalta una habilidad clave (crochet).

---

### 🔹 `<footer>`
- Contiene información de cierre.
- Incluye contacto y ubicación.

### 🔹 `<address>`
- Se usa específicamente para información de contacto.
- Mejora la semántica y accesibilidad del documento.

---

## 🌳 Estructura del DOM (árbol)

A continuación se muestra una representación simplificada del árbol DOM:
