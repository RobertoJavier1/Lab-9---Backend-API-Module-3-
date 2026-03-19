---

## Lab 9 - Parte 1 - Paginación

### Se implementó la paginación en el API

Se modificó el endpoint `GET /api/properties` para aceptar los parámetros `page` y `limit`, retornando un subconjunto de propiedades junto con metadata (total de registros, total de páginas y página actual).

**Video explicativo:** https://youtu.be/S_YhD77hcKg

> **Nota:** Probado en Brave Browser.
> Para instalar dependencias del backend usar: `npm install --legacy-peer-deps`

### Definition of Done

| Criterio | Descripción | Estado |
|----------|-------------|--------|
| Query params | `?page=1&limit=10` funciona correctamente | ✅ |
| Metadata retornada | Response incluye `{ data, meta: { total, page, limit, pages } }` | ✅ |
| Total count | `meta.total` muestra el conteo real de registros | ✅ |
| Cálculo de páginas | `meta.pages` = ceil(total / limit) | ✅ |
| Páginas vacías | Retorna array vacío, no error | ✅ |
| Valores por defecto | page=1, limit=10 si no se especifican | ✅ |
| Validación | Rechaza valores negativos o no numéricos | ✅ |
