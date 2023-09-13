# CWE-VS-CERT
Investigue el Common Weakness Enumeration Framework y los CERT Secure Coding Standards  Enliste las similitudes existentes entre ambos. Muestre 3 ejemplos de estándares del CERT que corresponda a un CWE. Justifique sus ejemplos con código, marcando las líneas donde se encuentra el problema.

# Similitudes entre CWE y CERT coding standards

- **Enfoque en la ciberseguridad:** Ambos conceptos se centran en la identificación y mitigación de debilidades en la seguridad del software. CWE enumera y describe debilidades comunes, mientras que los estándares de CERT proporcionan pautas para prevenir y abordar esas debilidades en el código.

- **Promueven mejores prácticas:** Se promueven mejores prácticas de seguridad en el desarrollo de software. CWE ayuda a los profesionales de la seguridad a identificar y clasificar debilidades, mientras que los estándares de CERT ofrecen indicaciones concretas para escribir código seguro y evitar esas debilidades.

- **Aplicación en múltiples lenguajes de programación:** Aunque de manera diferente, tanto CWE como los CERT se aplican y se reflejan en diferentes lenguajes de programación.

- **Recursos académicos:** Ambos proporcionan recursos educativos para ayudar a los desarrolladores y profesionales de la seguridad a comprender mejor las debilidades de seguridad y cómo abordarlas.

- **Aplicaciones en diferentes campos de TI:** Tanto los principios y recomendaciones de CWE, como los estándares de CERT son aplicables en diversos dominios de desarrollo de software, incluyendo aplicaciones web, aplicaciones móviles, sistemas embebidos y más.

- **Actualizaciones regulares:** Ambos sistemas se actualizan de manera regular para reflejar las cambiantes amenazas de seguridad y las nuevas debilidades que pueden surgir con el tiempo.

- **Uso en evaluaciones de seguridad:** Tanto CWE como los estándares de CERT son utilizados en evaluaciones de seguridad y auditorías de código para identificar y corregir debilidades. Es una práctica común de la seguridad recurrir a ambas fuentes para evaluar las aplicaciones y sistemas.

---

Para la siguiente sección tomé como base el documento “sei-cert-c-coding-standard-2016-v01”. Este documento es estándar de codificación para el lenguaje de programación C desarrollado por el Software Engineering Institute (SEI). Proporciona pautas y recomendaciones detalladas para escribir código C seguro y de alta calidad, con el objetivo de prevenir vulnerabilidades y debilidades de seguridad comunes.

### Ejemplos de estándares CERT que corresponden a un CWE:

**Ejemplo 1 - Estándar "EXP33-C":**

Este ejemplo de código no conforme al estándar “EXP33-C” de CERT está relacionado directamente con la CWE-457, que se refiere a la "Uso de datos no inicializados". 
![imagen "INT32-C](https://github.com/raulvillalpando/CWE-VS-CERT/blob/main/image_2023-09-12_201652588.png)
Aquí, la variable “error_log” se declara, pero no se inicializa antes de que se intente copiar su contenido en la cadena buffer utilizando “sprintf”. Debido a que “error_log” no tiene un valor definido, contiene un valor indeterminado y potencialmente peligroso.

**Ejemplo 2 - Estándar "ARR32-C":**

Este ejemplo de código no conforme al estándar "ARR32-C" de CERT está relacionado directamente con la CWE-131, que se refiere a el “Cálculo incorrecto del tamaño del búfer”. 
![imagen "INT32-C](https://github.com/raulvillalpando/CWE-VS-CERT/blob/1264f7889922623cfb0f67bbff78f41ab7527f82/image_2023-09-12_202034947.png)
En este código, se declara un "Variable Length Array (VLA)" llamado "vla" cuyo tamaño se basa en el parámetro "size". El estándar "ARR32-C" de CERT establece que se deben usar "rsize_t" o "size_t" para representar el tamaño de un objeto, y el uso de "size" como tamaño de un VLA podría resultar en un cálculo incorrecto del tamaño del búfer.

**Ejemplo 3 - Estándar "INT32-C":**

Este ejemplo de código no conforme al estándar "INT32-C" de CERT está relacionado directamente con la CWE-369, que se refiere a "División entre cero".
![imagen "INT32-C](https://github.com/raulvillalpando/CWE-VS-CERT/blob/main/image_2023-09-12_202336732.png)
Se presenta un error relacionado con la división por cero durante la operación de módulo en las variables "s_a" y "s_b". Si "s_b" es igual a 0, la operación de módulo resultaría en una división por cero, lo que es una operación indefinida y podría causar comportamientos impredecibles en el código.

---

**Referencias:**
- [Documento "sei-cert-c-coding-standard-2016-v01"](https://resources.sei.cmu.edu/downloads/secure-coding/assets/sei-cert-c-coding-standard-2016-v01.pdf)
- [CWE-457](https://cwe.mitre.org/data/definitions
- [CWE-457](https://cwe.mitre.org/data/definitions/457.html)
- [Estándares de CERT](https://wiki.sei.cmu.edu/confluence/display/seccode/SEI+CERT+Coding+Standards)
- [CWE-131](https://cwe.mitre.org/data/definitions/131.html)
- [Estándares de CERT en Wikipedia](https://en.wikipedia.org/wiki/CERT_Coding_Standards)
- [CWE-369](https://cwe.mitre.org/data/definitions/369.html)
