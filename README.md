# Traduce libros con GPT

Este proyecto aprovecha el poder de GPT-4 LLM para traducir libros electrónicos de cualquier idioma a tu idioma preferido, manteniendo la integridad y estructura del contenido original. Imagina tener acceso a un vasto mundo de literatura, independientemente del idioma original, al alcance de tus manos.

Esta herramienta no solo traduce el texto, sino que también compila cuidadosamente cada elemento del libro electrónico, incluidos los capítulos, las notas al pie y todo, en un archivo EPUB perfectamente formateado. Utilizamos el modelo gpt-4-1106-preview (GPT-4 Turbo) de forma predeterminada para garantizar traducciones de alta calidad. Sin embargo, entendemos la necesidad de flexibilidad, por lo que hemos facilitado cambiar los modelos en main.py según tus necesidades específicas.


## 🛠️ Instalación

Para instalar los componentes necesarios para nuestro proyecto, sigue estos sencillos pasos:

```bash
pip install -r requirements.txt
cp config.yaml.example config.yaml
```

Recuerda agregar tu clave de OpenAI a `config.yaml`.


## 🎮 Uso

Nuestro script viene con una variedad de parámetros para satisfacer tus necesidades. Así es como puedes sacarle el máximo provecho:

### Mostrar Capítulos

Antes de sumergirte en la traducción, se recomienda usar el modo `show-chapters` para revisar la estructura de tu libro:

```bash
python main.py show-chapters --input yourbook.epub
```

Este comando mostrará todos los capítulos, ayudándote a planificar tu proceso de traducción de manera efectiva.

### Modo de Traducción

#### Uso Básico

Para traducir un libro de inglés a polaco, usa el siguiente comando:

```bash
python main.py translate --input yourbook.epub --output translatedbook.epub --config config.yaml --from-lang EN --to-lang ES
```

#### Uso Avanzado

Para necesidades más específicas, como traducir del capítulo 13 al capítulo 37 de inglés a polaco, usa:

```bash
python main.py translate --input yourbook.epub --output translatedbook.epub --config config.yaml --from-chapter 13 --to-chapter 37 --from-lang EN --to-lang ES
```


## Convertir de AZW3 a EPUB

Para libros en formato AZW3 (Kindle de Amazon), utiliza Calibre (https://calibre-ebook.com) para convertirlos a EPUB antes de usar esta herramienta.


## DRM (Digital Rights Management)

Amazon eBooks (AZW3 format) are encrypted with your device's serial number. To decrypt these books, use the DeDRM tool (https://dedrm.com). You can find your Kindle's serial number at https://www.amazon.com/hz/mycd/digital-console/alldevices.


## 🤝 Contribuciones

¡Damos una cálida bienvenida a las contribuciones a este proyecto! Tus ideas y mejoras son invaluables. Actualmente, estamos particularmente interesados en contribuciones en las siguientes áreas:

Soporte para otros formatos de libros electrónicos: AZW3, MOBI, PDF.
Integración de una herramienta DeDRM incorporada.

¡Únete a nosotros para derribar las barreras del lenguaje en la literatura y mejorar la accesibilidad de los libros electrónicos en todo el mundo!
