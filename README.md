# Flask Barcode Scanner

Este proyecto es una aplicación web desarrollada en Flask que utiliza OpenCV y Pyzbar para escanear códigos de barras y códigos QR en tiempo real a través de una cámara.

## 📌 Requisitos

Antes de ejecutar la aplicación, asegúrate de tener instaladas las siguientes dependencias:

- Python 3.x
- Flask
- OpenCV (`cv2`)
- Pyzbar

Puedes instalarlas ejecutando:

```sh
pip install flask opencv-python pyzbar
```

## 🚀 Uso

1. Clona este repositorio:
   ```sh
   git clone <URL_DEL_REPOSITORIO>
   cd <NOMBRE_DEL_REPOSITORIO>
   ```
2. Ejecuta el script de la aplicación:
   ```sh
   python app.py
   ```
3. Accede a la aplicación en tu navegador visitando:
   ```
   http://localhost:5000
   ```

## 📷 Funcionamiento

- La aplicación accede a la cámara principal (`cv2.VideoCapture(3)`). Si no funciona, prueba cambiando el índice (`0`, `1`, `2`, etc.).
- Detecta y decodifica códigos de barras y códigos QR en tiempo real.
- Dibuja un rectángulo alrededor del código detectado y muestra su tipo y contenido.
- La transmisión de video se maneja mediante `multipart/x-mixed-replace`.

## 🛠 Estructura del Proyecto

```
/
│── templates/
│   ├── index.html  # Página de visualización del video
│── app.py          # Código principal de la aplicación Flask
│── README.md       # Documentación del proyecto
```

## ⚠️ Notas

- Si la cámara no se abre, verifica los permisos y cambia el índice de la cámara en `cv2.VideoCapture(3)`.
- Asegúrate de que la cámara no esté siendo utilizada por otro proceso.

## 📜 Licencia

Este proyecto está bajo la licencia MIT. ¡Siéntete libre de contribuir y mejorar!

---
✉️ Para preguntas o mejoras, ¡abre un issue o un pull request en GitHub!

