# 📄 Archivos de Ejemplo para Probar Study Vault

## Archivo 1: Introducción a AWS Lambda

Guarda este texto en un archivo llamado `aws-lambda-intro.txt`:

```
AWS Lambda es un servicio de computación sin servidor que ejecuta código en respuesta a eventos y administra automáticamente los recursos informáticos subyacentes.

Con Lambda, puede ejecutar código para prácticamente cualquier tipo de aplicación o servicio backend, sin necesidad de administración. Solo tiene que cargar su código y Lambda se encargará de todo lo necesario para ejecutar y escalar su código con alta disponibilidad.

Lambda ejecuta su código en una infraestructura de computación de alta disponibilidad y realiza toda la administración de los recursos informáticos, incluido el mantenimiento del servidor y del sistema operativo, el aprovisionamiento y escalado automático de capacidad y el registro.

Las principales ventajas incluyen cero administración de servidores, escalado automático continuo, y pago por milisegundo de tiempo de computación consumido.
```

---

## Archivo 2: Presentación Personal (Para LinkedIn)

Guarda como `presentacion.txt`:

```
Hola, soy un desarrollador enfocado en soluciones cloud con AWS.

Recientemente completé un proyecto llamado Study Vault, una aplicación serverless que convierte archivos de texto a audio utilizando Amazon Polly, Lambda y S3.

El proyecto demuestra mi experiencia en arquitecturas sin servidor, integración de servicios AWS, y desarrollo de interfaces modernas con JavaScript.

La infraestructura completa está gestionada con Terraform, siguiendo las mejores prácticas de infraestructura como código.

Estoy buscando oportunidades para aplicar mis habilidades en cloud computing y desarrollo serverless.
```

---

## Archivo 3: Explicación Técnica

Guarda como `arquitectura-serverless.txt`:

```
La arquitectura serverless de Study Vault utiliza una combinación de servicios AWS completamente gestionados.

Cuando un usuario sube un archivo de texto al bucket de S3 de entrada, este evento desencadena automáticamente una función Lambda.

La función Lambda lee el contenido del archivo, lo procesa y utiliza Amazon Polly para generar audio de alta calidad con voces neuronales.

El archivo MP3 resultante se almacena en el bucket de S3 de salida, donde el usuario puede descargarlo inmediatamente.

Todo el proceso es completamente automático, escalable y solo genera costos cuando realmente se utiliza.

La infraestructura está definida como código usando Terraform, lo que permite un despliegue reproducible y versionado.
```

---

## Archivo 4: Caso de Uso Real

Guarda como `caso-uso-estudio.txt`:

```
Study Vault es ideal para estudiantes y profesionales que necesitan convertir material de lectura en formato de audio.

Imagina tener que estudiar un documento extenso pero querer aprovechar el tiempo de transporte o ejercicio.

Con Study Vault, simplemente subes tu documento de texto y en segundos obtienes un archivo de audio profesional que puedes escuchar en cualquier dispositivo.

Es perfecto para repasar apuntes, memorizar definiciones, o escuchar artículos mientras realizas otras actividades.

La voz generada por Amazon Polly es natural y clara, haciendo la experiencia de escucha muy cómoda.
```

---

## Archivo 5: Descripción para README

Guarda como `descripcion-proyecto.txt`:

```
Study Vault es una aplicación web serverless desarrollada con AWS que transforma archivos de texto en archivos de audio MP3 de alta calidad.

El proyecto demuestra el uso de servicios AWS modernos incluyendo S3 para almacenamiento, Lambda para procesamiento sin servidor, y Amazon Polly para síntesis de voz avanzada.

La aplicación cuenta con una interfaz frontend profesional desarrollada con JavaScript vanilla y el SDK de AWS, permitiendo una experiencia de usuario fluida y moderna.

Toda la infraestructura está definida como código usando Terraform, facilitando el despliegue reproducible y la gestión de versiones.

Este proyecto es ideal para el portfolio de cualquier desarrollador cloud, demostrando conocimientos prácticos de arquitecturas serverless y mejores prácticas de AWS.
```

---

## Instrucciones de Uso

### Crear los archivos:

**Opción 1 - Manualmente:**
1. Abre un editor de texto (Notepad, VS Code, etc.)
2. Copia el contenido de uno de los ejemplos
3. Guarda como archivo `.txt`

**Opción 2 - PowerShell:**

```powershell
# Crear carpeta para ejemplos
mkdir test-files

# Crear archivo de ejemplo
@"
AWS Lambda es un servicio de computación sin servidor que ejecuta código en respuesta a eventos y administra automáticamente los recursos informáticos subyacentes.

Con Lambda, puede ejecutar código para prácticamente cualquier tipo de aplicación o servicio backend, sin necesidad de administración.
"@ | Out-File -FilePath "test-files\aws-lambda-intro.txt" -Encoding UTF8
```

### Probar con el Frontend:

1. Inicia el servidor local
2. Abre `http://localhost:8000`
3. Arrastra uno de los archivos `.txt` al área de upload
4. Click "Upload & Convert"
5. Espera la conversión (10-30 segundos)
6. Descarga el MP3 generado

---

## Tips para Crear Buenos Archivos de Prueba

### ✅ Recomendado:
- Textos de 50-500 palabras
- Contenido profesional o educativo
- Frases completas y bien estructuradas
- Sin caracteres especiales complejos
- Texto en español o inglés (Polly soporta ambos)

### ❌ Evitar:
- Archivos muy largos (>10MB)
- Solo números o códigos
- Mucho contenido técnico con símbolos
- Lenguajes no soportados por Polly

---

## Personalizar la Voz

Si quieres experimentar con diferentes voces de Polly, puedes modificar tu función Lambda para aceptar parámetros de voz.

**Voces en Español disponibles en Polly:**
- Lupe (Femenina, Español US)
- Miguel (Masculina, Español US)
- Penélope (Femenina, Español US)
- Conchita (Femenina, Español España)
- Enrique (Masculina, Español España)
- Mia (Femenina, Español México)

**Ejemplo de modificación en Lambda:**

```python
# En tu función Lambda, línea de Polly:
response = polly.synthesize_speech(
    Text=text_content,
    OutputFormat='mp3',
    VoiceId='Mia',  # ← Cambiar aquí
    Engine='neural'  # Usar motor neural para mejor calidad
)
```

**¡Pruebalo! 🚀**
