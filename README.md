# AutoGreen - Sistema de Monitoreo y Control de Invernadero

**Arquitectura de Computadoras I**  
**Universidad Mariano Gálvez de Guatemala**

---

## Descripción

AutoGreen es un sistema embebido que monitorea y controla automáticamente las condiciones ambientales de un invernadero: **temperatura**, **humedad del suelo** y **luminosidad**.

El proyecto demuestra la aplicación práctica de los principios de arquitectura de computadoras en sistemas de tiempo real, utilizando un microcontrolador como núcleo del sistema.

---

## Contenido del repositorio

| Archivo | Descripción |
|---------|-------------|
| `AutoGreen.ino` | Código fuente del proyecto |
| `diagram.json` | Diagrama de conexiones para Wokwi |
| `proyecto anduino arqui Copy.zip` | Archivo comprimido con todo el proyecto |
| `README.md` | Documentación del proyecto |

---

## Componentes utilizados

### Actuadores
| Componente | Función | Pin Arduino |
|------------|---------|-------------|
| Motor DC (ventilador) | Enfriamiento activo | 9 |
| Motor DC (bomba) | Riego automático | 10 |
| LED amarillo | Simula calefactor | 11 |
| LED blanco | Simula luz auxiliar | 12 |

### Sensores (simulados en demo)
- Temperatura (simulada internamente)
- Humedad de suelo (simulada internamente)
- Luminosidad (simulada internamente)

---

## Lógica de control automático

| Condición | Acción | Actuador |
|-----------|--------|----------|
| Temperatura > 30°C | Activar ventilador | Motor DC pin 9 |
| Temperatura < 15°C | Activar calefactor | LED amarillo pin 11 |
| Humedad suelo < 40% | Activar bomba de riego | Motor DC pin 10 |
| Luminosidad < 200 lux | Activar luz auxiliar | LED blanco pin 12 |

---

## Requisitos

- **Plataforma**: Wokwi (simulación en línea) o Arduino físico
- **Placa**: Arduino UNO (compatible)
- **Librerías**: No requiere librerías adicionales para la versión demo
- **IDE**: Arduino IDE 1.8.x o superior (si se usa hardware físico)

---

## Cómo usar (en Wokwi)

1. Abrir [Wokwi.com](https://wokwi.com/projects/new/arduino-uno)
2. Copiar el contenido de `AutoGreen.ino` en el editor
3. Copiar el contenido de `diagram.json` en el archivo del mismo nombre
4. Presionar "Start Simulation"
5. Observar cómo cambian las condiciones cada 10 segundos y los actuadores se activan automáticamente

---

## Demostración de funcionalidades

El programa cambia automáticamente las condiciones cada 10 segundos para demostrar:

| Escenario | Temperatura | Humedad suelo | Luminosidad | Actuador activado |
|-----------|-------------|---------------|-------------|-------------------|
| Normal | 25°C | 60% | 5000 lux | Ninguno |
| Calor | 35°C | 60% | 5000 lux | Ventilador |
| Frío | 10°C | 60% | 5000 lux | Calefactor |
| Suelo seco | 25°C | 25% | 5000 lux | Bomba de riego |
| Oscuro | 25°C | 60% | 100 lux | Luz auxiliar |

---

## Video de demostración

[Enlace al video en Google Drive]

---

## Integrantes

-Jose Antonio Ortega
Rene Alejandro Ramirez
---

## Curso

Arquitectura de Computadoras I  
Facultad de Ingeniería en Sistemas de Información y Ciencias de la Computación  
Universidad Mariano Gálvez de Guatemala

---

## Repositorio

[GitHub - jortegal2-gif/proyecto-arquitectura-de-computadoras](https://github.com/jortegal2-gif/proyecto-arquitectura-de-computadoras)
