# Control y Trazabilidad de Proyecto para Agentes IA

Este repositorio contiene paquetes portables para instalar una estructura documental de control, trazabilidad y auditoria en proyectos de software. El objetivo es que un agente IA pueda entrar a un repositorio, entender su estado real, registrar cambios y mantener evidencia tecnica sin depender solo de la memoria conversacional.

## Paquetes incluidos

### 1. Codex Skill

Archivo:

```txt
codex-skill-control-trazabilidad-proyecto.zip
```

Uso:

Instala una skill global para Codex llamada:

```txt
control-trazabilidad-proyecto
```

Contenido principal:

```txt
.codex/skills/control-trazabilidad-proyecto/
  SKILL.md
  agents/openai.yaml
  scripts/install_control_docs.py
  templates/
    minimal/
    base/
    enterprise/
    fullstack-ia/
```

Instalacion en Windows:

```powershell
Expand-Archive .\codex-skill-control-trazabilidad-proyecto.zip -DestinationPath .\tmp-codex-skill -Force
.\tmp-codex-skill\install-global.ps1
```

Despues de instalar, reiniciar Codex.

Ejemplo de uso en Codex:

```txt
control-trazabilidad-proyecto: instala fullstack-ia en este repo
```

O por terminal:

```powershell
python $env:USERPROFILE\.codex\skills\control-trazabilidad-proyecto\scripts\install_control_docs.py --target . --variant fullstack-ia
```

### 2. Adaptador para Antigravity

Archivo:

```txt
antigravity-control-trazabilidad-proyecto.zip
```

Carpeta fuente:

```txt
antigravity-control-trazabilidad-proyecto/
```

Contenido principal:

```txt
antigravity-control-trazabilidad-proyecto/
  AGENTS.md
  GEMINI.md
  README_ANTIGRAVITY.md
  install-antigravity.ps1
  install-antigravity.sh
  .agent/rules/control-trazabilidad-proyecto.md
  scripts/install_control_docs.py
  templates/
    minimal/
    base/
    enterprise/
    fullstack-ia/
```

Instalacion en un repositorio desde Windows:

```powershell
Expand-Archive .\antigravity-control-trazabilidad-proyecto.zip -DestinationPath .\tmp-antigravity-control -Force
.\tmp-antigravity-control\install-antigravity.ps1 -Target "C:\ruta\del\repo" -Variant fullstack-ia
```

Uso esperado dentro de Antigravity:

```txt
Aplica control-trazabilidad-proyecto fullstack-ia en este repo.
```

## Variantes disponibles

### minimal

Para proyectos pequenos o personales. Incluye los archivos esenciales de control:

```txt
README.md
CONTROL_PROYECTO_AUDITADO.md
BITACORA_IA.md
HISTORIAL_CAMBIOS_PROYECTO.md
CHECKLIST_MAESTRO_PROYECTO.md
INSTRUCCION_PARA_IA.md
```

### base

Para proyectos de tamano medio que requieren mas contexto documental:

```txt
README.md
CONTROL_PROYECTO_AUDITADO.md
BITACORA_IA.md
HISTORIAL_CAMBIOS_PROYECTO.md
CHECKLIST_MAESTRO_PROYECTO.md
INSTRUCCION_PARA_IA.md
INVENTARIO_REAL_PROYECTO.md
DECISIONES_ARQUITECTURA.md
DEUDA_TECNICA_Y_NORMALIZACION.md
MEMORIA_CONTEXTUAL.md
```

### enterprise

Para proyectos con auditoria, riesgos, incidentes o cumplimiento:

```txt
README.md
CONTROL_PROYECTO_AUDITADO.md
BITACORA_IA.md
HISTORIAL_CAMBIOS_PROYECTO.md
CHECKLIST_MAESTRO_PROYECTO.md
INSTRUCCION_PARA_IA.md
INVENTARIO_REAL_PROYECTO.md
DECISIONES_ARQUITECTURA.md
DEUDA_TECNICA_Y_NORMALIZACION.md
REGISTRO_INCIDENTES_Y_SOLUCIONES.md
RIESGOS_Y_CONTROLES.md
```

### fullstack-ia

Para proyectos con backend, frontend, scripts, migraciones, Docker o trabajo frecuente con agentes IA:

```txt
README.md
CONTROL_PROYECTO_AUDITADO.md
BITACORA_IA.md
HISTORIAL_CAMBIOS_PROYECTO.md
CHECKLIST_MAESTRO_PROYECTO.md
INSTRUCCION_PARA_IA.md
INVENTARIO_REAL_PROYECTO.md
DECISIONES_ARQUITECTURA.md
DEUDA_TECNICA_Y_NORMALIZACION.md
MAPA_MODULOS_Y_RUTAS.md
REGISTRO_PROBLEMAS_Y_SOLUCIONES.md
```

## Flujo recomendado

1. Crear o abrir el repositorio destino.
2. Instalar el paquete con la variante adecuada.
3. Completar primero `CONTROL_PROYECTO_AUDITADO.md`.
4. Registrar hallazgos reales en `INVENTARIO_REAL_PROYECTO.md`.
5. Registrar decisiones en `DECISIONES_ARQUITECTURA.md`.
6. Registrar cambios en `HISTORIAL_CAMBIOS_PROYECTO.md`.
7. Registrar trabajo de agentes IA en `BITACORA_IA.md`.
8. Mantener pendientes y riesgos en los archivos correspondientes.

## Regla operativa

Todo cambio importante debe dejar evidencia minima:

```txt
1. Que se cambio
2. Donde se cambio
3. Por que se cambio
4. Como se valido
5. Que queda pendiente
```

## Reglas de seguridad

- No registrar credenciales, tokens, passwords ni secretos.
- No sobrescribir documentos existentes sin revisar su contenido.
- Diferenciar hechos confirmados de supuestos.
- Tratar el codigo real del repositorio como fuente principal.
- Si hay Docker o servicios vivos, validar contra el entorno real antes de documentar.

## Estructura sugerida del repositorio GitHub

```txt
control-trazabilidad-proyecto/
  README.md
  LICENSE
  codex-skill-control-trazabilidad-proyecto.zip
  antigravity-control-trazabilidad-proyecto.zip
  antigravity-control-trazabilidad-proyecto/
  docs/
    REFERENCIA_REPOSITORIO_GITHUB_CONTROL_TRAZABILIDAD.md
```

Este archivo puede usarse como base para el `README.md` principal del repositorio o como documento dentro de `docs/`.

