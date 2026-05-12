# Informe de revisión de repositorio

## Resumen ejecutivo

Se revisó el repositorio autorizado con enfoque en mejoras prácticas de código, pruebas, configuración, CI/CD, dependencias y documentación.

Esta revisión se basa únicamente en evidencias presentes dentro del repositorio.

## Repositorio revisado

- Repositorio: `{{repo_url}}`
- Fecha: `{{review_date}}`
- Rama o commit: `{{commit_or_branch}}`
- Paquete contratado: `{{package_name}}`

## Alcance

Incluido en esta revisión:

- Revisión estática de código
- Revisión de dependencias desde manifests y lockfiles
- Revisión de configuración
- Revisión de pruebas
- Revisión de CI/CD
- Revisión de documentación
- Recomendación de un PR mínimo cuando aplica

## Qué no se probó

No se realizaron pruebas contra sistemas en vivo, explotación, uso de credenciales, escaneo externo, bypass de protecciones ni validación de infraestructura de terceros.

Esta revisión no es una prueba de penetración ni una auditoría completa de seguridad.

## Hallazgos principales

{{top_findings}}

Cada hallazgo debe incluir:

- Evidencia del repositorio
- Impacto práctico
- Recomendación
- Esfuerzo estimado
- Si es adecuado para un PR pequeño

## PR recomendado

- Título: `{{recommended_pr_title}}`
- Cambio propuesto: `{{recommended_pr_summary}}`
- Motivo: `{{recommended_pr_reason}}`
- Archivos previstos o modificados: `{{changed_files}}`
- Verificación: `{{verification_steps}}`
- Notas de reversión: `{{rollback_notes}}`

## Impacto de negocio

{{business_impact}}

Ejemplos de impacto:

- Menos fricción para futuros cambios
- Pruebas más fiables
- Configuración más clara
- Menor riesgo de regresiones
- Mejor documentación para el equipo

## Próximos pasos

1. Revisar el PR propuesto.
2. Ejecutar las verificaciones indicadas.
3. Aprobar, comentar o solicitar ajustes.
4. Priorizar los hallazgos restantes según impacto y esfuerzo.
5. Considerar una revisión mensual si el repositorio cambia con frecuencia.

## Descargo de responsabilidad

Esta revisión es únicamente una revisión de código y repositorio. No es una prueba de penetración, una auditoría de seguridad completa ni una validación de sistemas en producción.

Todas las observaciones se limitan a evidencias encontradas dentro del repositorio autorizado.
