# Nira - AI Personal Instructor & Biometric Interviewer

Nira es una aplicación diseñada para simular entrevistas de estrés analizando la biometría del usuario y generando respuestas dinámicas. 

## Arquitectura del Sistema

A continuación se detalla cómo interactúan los diferentes módulos de inteligencia artificial y procesamiento:

```mermaid
graph TD
    User([Usuario]) -->|Voz / Respuestas| AudioIn[Procesamiento de Audio]
    User -->|Cámara| Vision[Visión Computacional]
    
    Vision -->|Detección de parpadeos/atención| Core[Núcleo de Lógica - Python]
    AudioIn -->|Transcripción| Core
    
    Core -->|Prompt + Contexto Biométrico| LLM[(LLM Local: Llama 3)]
    LLM -->|Respuesta Generada| Core
    
    Core -->|Texto a Voz| AudioOut[Salida de Audio]
    Core -->|Actualización UI| UI[Interfaz de Usuario / Logo Animado]
    
    UI --> User
    AudioOut --> User
```

### Estructura del Proyecto
/src: Código fuente principal de la aplicación.

/assets: Recursos visuales (incluyendo el logo SVG animado estilo minimalista-creativo).

/docs: Documentación adicional y pruebas de LLM.
