# Conclusiones y recomendaciones 
## Conclusiones
La implementación de las IAs en una app móvil desarrollada con Flutter demostró ser eficiente y viable, especialmente considerando la distribución de responsabilidades entre Firebase para la app, Azure para el backend en Java, y MySQL como base de datos. Este enfoque modular permitió una integración fluida de los modelos de restauración de imágenes.  
Los modelos basados en la arquitectura U-Net lograron resultados satisfactorios al restaurar imágenes degradadas, gracias a un entrenamiento sólido y mejoras en el dataset. La inclusión de funciones como protección de áreas blancas, degradaciones controladas y una variabilidad más amplia en el dataset fueron clave para mejorar la capacidad de generalización del modelo.  
La exportación de los modelos a formatos ligeros, como TensorFlow Lite, permitió que las IAs fueran compatibles con dispositivos móviles sin sacrificar demasiado el rendimiento. Esto fue esencial para mantener una experiencia de usuario fluida.  
Se superaron los problemas de memoria durante el entrenamiento al ajustar el tamaño de lote y emplear técnicas de manejo eficiente de GPU. En el entorno móvil, las optimizaciones realizadas en los modelos garantizaron un rendimiento aceptable incluso en dispositivos con hardware limitado.  
El despliegue en Azure del backend y la base de datos permitió manejar eficientemente las solicitudes provenientes de la app móvil, mientras que Firebase Distribution facilitó la distribución de la app a los usuarios finales. La arquitectura modular asegura escalabilidad para futuros desarrollos.  
## Recomendaciones
1. Ampliar las Capacidades de las IAs  
Se recomienda agregar nuevas funciones, como la detección automática de tipos de degradación, para que el modelo ajuste dinámicamente las técnicas de restauración aplicadas.  
Sería beneficioso incorporar modelos complementarios que mejoren detalles específicos, como texturas o el reconocimiento de patrones en las imágenes restauradas.  
2. Entrenamiento Continuo y Dataset Realista  
Es aconsejable implementar un entrenamiento incremental que permita a los modelos adaptarse a casos de uso específicos mediante datos adicionales recolectados de usuarios reales.  
Ampliar el dataset con degradaciones más realistas y contextuales, basadas en las imágenes más comunes enviadas por los usuarios, contribuiría a una mayor robustez del modelo.  
3. Optimización para Dispositivos Móviles  
Se sugiere experimentar con técnicas de compresión de modelos, como pruning o quantization, para reducir aún más el tamaño de los modelos sin comprometer la calidad de las predicciones.  
Incluir opciones offline que permitan ejecutar las predicciones de las IAs localmente en dispositivos con hardware más potente podría mejorar la experiencia del usuario.  
4. Monitoreo y Actualización de Modelos  
Es importante implementar un sistema de monitoreo en tiempo real para evaluar el desempeño de las IAs en producción y detectar posibles áreas de mejora.  
Se recomienda planificar un proceso regular de actualización y mejora de los modelos, basado en métricas de uso y retroalimentación proporcionada por los usuarios finales.  
5. Exploración de Tecnologías Avanzadas  
Evaluar el uso de GPUs en dispositivos móviles, aprovechando tecnologías como Vulkan o NNAPI, podría mejorar los tiempos de inferencia de los modelos.  
Se sugiere explorar alternativas como ONNX para facilitar la interoperabilidad entre diferentes entornos de desarrollo y despliegue.  
6. Documentación y Escalabilidad  
Es crucial mantener una documentación clara y detallada para los modelos de IA, especificando cómo integrarlos, actualizarlos y adaptarlos a nuevos requerimientos.  
Diseñar la arquitectura de la aplicación y el backend con un enfoque en escalabilidad asegurará que el sistema pueda manejar un aumento de usuarios y solicitudes a las IAs en el futuro.  
# Video about the team
Video: [https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u202111473_upc_edu_pe/EeHBUvpIWDJFkDe6fM1n2H8BKKaH40jAg1BefbL2aIXFjw](https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u202111473_upc_edu_pe/EeHBUvpIWDJFkDe6fM1n2H8BKKaH40jAg1BefbL2aIXFjw)
# Video about de product
Video: [https://youtube.com/shorts/C8Y_LiXyZec?si=Sb1mhAyBS0A3wa3a](https://youtube.com/shorts/C8Y_LiXyZec?si=Sb1mhAyBS0A3wa3a)
# Expo TF
Video: [https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u202111473_upc_edu_pe/EcqTcuhIJDBOj9V_7TCiz7UBkwIz48cf2G01DdoCl7bIog?e=WSDukI](https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u202111473_upc_edu_pe/EcqTcuhIJDBOj9V_7TCiz7UBkwIz48cf2G01DdoCl7bIog?e=WSDukI)

# Bibliografía

Chamorro, S. R. (2024, febrero 5). Más allá del tiempo y del espacio: la digitalización como guardián del patrimonio cultural. UCV. https://www.ucv.edu.pe/noticias/la-digitalizacion-como-guardian-del-patrimonio-cultural

Día de las Fuerzas Armadas: Bienes culturales muebles que representan momentos históricos del Ejército, la Fuerza Aérea y Marina de Guerra. (2024 9). Gob.pe. https://www.gob.pe/institucion/cultura/noticias/1028611-dia-de-las-fuerzas-armadas-bienes-culturales-muebles-que-representan-momentos-historicos-del-ejercito-la-fuerza-aerea-y-marina-de-guerra

Ministerio de Cultura lanzó primera Hackathon para promover el uso de la tecnología en la conservación del Patrimonio Cultural. (2019, primavera 5). https://www.gob.pe/institucion/cultura/noticias/28619-ministerio-de-cultura-lanzo-primera-hackathon-para-promover-el-uso-de-la-tecnologia-en-la-conservacion-del-patrimonio-cultural

# Anexos

Link de video de exposición TB1:  
[https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u20201c163_upc_edu_pe/ERY_XHmBBCdBjzRnCP3oh1gBQWiKyzbCr6BKKI-b14gxig?e=SYsrsi&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D](https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u20201c163_upc_edu_pe/ERY_XHmBBCdBjzRnCP3oh1gBQWiKyzbCr6BKKI-b14gxig?e=SYsrsi&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

Link de Entrevistas Needfinding:  
[https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u20201c163_upc_edu_pe/EUA1bGMuXmJGt8kr7gde9HcBiBCtMpYKwZ\_\_b1O62Ai5IA?e=V9EbOz&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D](https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u20201c163_upc_edu_pe/EUA1bGMuXmJGt8kr7gde9HcBiBCtMpYKwZ__b1O62Ai5IA?e=V9EbOz&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)

Link de video de exposición TP1:  
[https://upcedupe-my.sharepoint.com/personal/u202111473_upc_edu_pe/\_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202111473%5Fupc%5Fedu%5Fpe%2FDocuments%2Fupc%2Dpre%2D202401%2Dsi728%2DWS82%2DImagIA%2Dexpo%2DTP1%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2E1d39692d%2D2558%2D493a%2D8f9e%2D7ee1b1ed252a](https://upcedupe-my.sharepoint.com/personal/u202111473_upc_edu_pe/_layouts/15/stream.aspx?id=%2Fpersonal%2Fu202111473%5Fupc%5Fedu%5Fpe%2FDocuments%2Fupc%2Dpre%2D202401%2Dsi728%2DWS82%2DImagIA%2Dexpo%2DTP1%2Emp4&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0&ga=1&referrer=StreamWebApp%2EWeb&referrerScenario=AddressBarCopied%2Eview%2E1d39692d%2D2558%2D493a%2D8f9e%2D7ee1b1ed252a)

Link de video del prototipo:  
[https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u202023137_upc_edu_pe/ETyhv7Zk401OvUul-TyZkDwBaTdF2OmvhmbpMlOU1RqoRQ?e=6BxKFO&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D](https://upcedupe-my.sharepoint.com/%3Av%3A/g/personal/u202023137_upc_edu_pe/ETyhv7Zk401OvUul-TyZkDwBaTdF2OmvhmbpMlOU1RqoRQ?e=6BxKFO&nav=eyJyZWZlcnJhbEluZm8iOnsicmVmZXJyYWxBcHAiOiJTdHJlYW1XZWJBcHAiLCJyZWZlcnJhbFZpZXciOiJTaGFyZURpYWxvZy1MaW5rIiwicmVmZXJyYWxBcHBQbGF0Zm9ybSI6IldlYiIsInJlZmVycmFsTW9kZSI6InZpZXcifX0%3D)
