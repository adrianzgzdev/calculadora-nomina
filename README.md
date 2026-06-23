# 💶 Calculadora de nómina

Aplicación web ligera para estimar el **salario neto mensual** y el **bruto/neto anual** a partir de tus propios datos. Sin instalación, sin registro y sin enviar nada a ningún servidor: todo se calcula en el navegador y tus datos se guardan únicamente en tu dispositivo.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Sin dependencias](https://img.shields.io/badge/dependencias-0-1ba163)

## 🔗 Demo

👉 **[Ver la calculadora en vivo](https://adrianzgzdev.com/calculadora-nomina/)**

> La demo estará activa una vez habilites GitHub Pages (Settings → Pages).

## 📸 Captura

## 📸 Captura

![Captura de la calculadora](docs/captura.png)

## ✨ Características

- **Cálculo reactivo**: el neto se recalcula al instante mientras escribes, sin botones de "calcular".
- **Todo configurable por el usuario**: salario base bruto, IRPF, horas extra (con tarifa propia), dietas (días × importe), ingresos extra y un campo para simular una subida.
- **Pagas extra**: selector de **12 pagas** (extras prorrateadas) o **14 pagas** (dos extras), aplicando solo el IRPF a las pagas extraordinarias.
- **Importe a restar opcional**: casilla para descontar un importe fijo del bruto base antes de calcular.
- **Desglose visual**: barra de proporción neto/descuentos y resumen anual de bruto y neto.
- **Persistencia local**: los valores se guardan en `localStorage`, así que al volver a abrir la app siguen ahí. Nada sale del dispositivo.
- **Responsive y tipo app**: diseño adaptado a móvil, con metadatos para añadirla a la pantalla de inicio en iOS/Android.

## 🧮 Cómo se calcula

A partir del bruto introducido se suman horas extra, dietas, ingresos extra y simulación de subida para obtener el **bruto total mensual**. Sobre él se aplican:

- **Contingencias comunes** (Seguridad Social): 4,85 %
- **Desempleo y Formación Profesional**: 1,65 %
- **IRPF**: porcentaje editable por el usuario

El **neto anual** considera 12 mensualidades más las pagas extra seleccionadas, a las que se les aplica únicamente la retención de IRPF.

> ⚠️ **Aviso**: es una herramienta de **estimación**. Los tipos de cotización son valores de referencia simplificados y el IRPF lo introduce cada usuario. No sustituye a tu nómina oficial ni constituye asesoramiento fiscal o laboral.

## 🛠️ Tecnologías

- HTML5, CSS3 y JavaScript **vanilla** (sin frameworks ni librerías)
- `localStorage` para la persistencia
- `Intl.NumberFormat` para el formateo de moneda y porcentajes en `es-ES`
- Un único archivo `index.html` autocontenido

## 🚀 Uso en local

No necesita compilación ni dependencias. Basta con abrir el archivo:

```bash
# Clona el repositorio
git clone https://github.com/adrianzgzdev/calculadora-nomina.git
cd calculadora-nomina

# Abre index.html en el navegador (o usa un servidor local)
python3 -m http.server 8000
# y visita http://localhost:8000
```

## 📂 Estructura

```
calculadora-nomina/
├── index.html   # Aplicación completa (HTML + CSS + JS)
└── README.md
```

## 📄 Licencia

Distribuido bajo licencia [MIT](LICENSE). Úsalo y modifícalo libremente.
