# Apis-deploy

Repositorio monorepo con tres mini APIs listas para despliegue:

- `Api-Node`
- `Api-SpringBoot`
- `Api-Django`

## Despliegue con Render + GitHub Actions

1. Crea tres servicios web en Render usando este repositorio.
2. Usa `render.yaml` como blueprint o crea cada servicio por separado con estas rutas raíz:
   - `Api-Node`
   - `Api-SpringBoot`
   - `Api-Django`
3. Copia el deploy hook de cada servicio y guárdalo en GitHub Secrets con estos nombres:
   - `RENDER_DEPLOY_HOOK_NODE`
   - `RENDER_DEPLOY_HOOK_SPRING`
   - `RENDER_DEPLOY_HOOK_DJANGO`
4. Cada push a `main` dispara el workflow, que valida el proyecto y luego llama el hook de Render.
