# Espacio Ceniza · webs

Sitio de **espacioceniza.com.ar**. Lo arma y mantiene FÁRA.

## Qué hay en cada carpeta

| Dirección | Archivo | Qué es | Planilla que lee |
|---|---|---|---|
| espacioceniza.com.ar/ | `index.html` | Página "En construcción" (después, la landing) | CEN · Landing |
| espacioceniza.com.ar/menu/ceniza/ | `menu/ceniza/index.html` | Carta digital de la barra | CEN · Carta Ceniza |
| cualquier dirección mal escrita | `404.html` | "Esta página se hizo ceniza" | ninguna |

- `img/gato.png`: la verdadera dueña, sin fondo.
- `robots.txt` y `sitemap.xml`: para que Google encuentre las páginas. Cada web nueva se suma al sitemap.

## Cómo funcionan las planillas

Cada web lee su propia planilla de Google Sheets cada vez que alguien la abre. Los textos, precios y botones se cambian en la planilla y se ven al instante, **sin deploy**.

- Las planillas tienen que estar compartidas como **"Cualquier persona con el enlace: Lector"**.
- La conexión depende del número de la planilla (`SHEET_ID` en cada HTML), no del nombre: renombrarlas no rompe nada.
- No cambiar nombres de pestañas ni títulos de la fila 1.

| Planilla | SHEET_ID |
|---|---|
| CEN · Carta Ceniza | `1rxyhL-DvDZdc8bgR_W3I3laMquBYutnD_pCpDOB1hfE` |
| CEN · Landing | `1tQRIqG_XmDIsW2eLSiiRx9bEolFyDnfgWrWtOi9QrFw` |

## Cuándo hace falta deploy

Solo para cambios de diseño, la imagen que se ve al compartir por WhatsApp, el título de Google o una web nueva. Primero en una rama de prueba (la vista previa de Netlify no gasta créditos), después a `main`.

## Webs futuras

Cada una en su carpeta, con su planilla propia:

```
menu/<nombre-de-la-carta>/index.html
eventos/index.html
cumpleanos/index.html
```

Al publicar una nueva: sumarla a `sitemap.xml` y a esta tabla.
