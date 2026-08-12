# Despliegue Web — GitHub Pages + Dominio Propio

**Dominio:** boris-bagemihl-formacion.com  
**Hosting:** GitHub Pages  
**Paquete listo:** [`../web-deploy-2026-08-11.zip`](../web-deploy-2026-08-11.zip) (también copia en esta carpeta)

---

## Subir ahora (11 ago 2026)

1. Abrir el repo GitHub Pages que sirve el dominio.
2. Descomprimir o arrastrar el contenido de `web-deploy-2026-08-11.zip` a la **raíz** del repo (reemplazar archivos).
3. Commit: `Web ago 2026: hero + perfil comercial ES/DE`
4. Esperar ~1 min y comprobar:
   - https://boris-bagemihl-formacion.com/
   - https://boris-bagemihl-formacion.com/de.html
   - https://boris-bagemihl-formacion.com/cv-boris-bagemihl.pdf
   - https://boris-bagemihl-formacion.com/lebenslauf-boris-bagemihl.pdf

**Incluye el zip (24 archivos):** `index.html`, `de.html`, fotos, perfiles/CV ES+DE, guías PDF, `CNAME`, `robots.txt`, `sitemap.xml`, `README-SUBIR-GITHUB.txt`.

---

## Inventario raíz Pages

| Archivo | Función |
|---------|---------|
| `index.html` | Web ES (hero nuevo) |
| `de.html` | Web DE |
| `fotoBB.jpg` | Foto perfil («Sobre mí»; hero ya sin foto) |
| `og-image.jpg` | Open Graph |
| `cv-boris-bagemihl.pdf` / `.html` | **Perfil comercial 1p ES** |
| `cv-completo-boris-bagemihl.pdf` / `.html` | CV largo SCE/FPE ES |
| `lebenslauf-boris-bagemihl.pdf` / `.html` | **Kurzprofil 1p DE** |
| `lebenslauf-komplett-boris-bagemihl.pdf` / `.html` | Lebenslauf largo DE |
| `perfil-comercial-*.html/pdf` | Fuentes duplicadas ES (mismo contenido que cv-*) |
| `profil-kommerziell-*.html/pdf` | Fuentes duplicadas DE |
| `guia-fundae-coste-cero.*` | Guía coste cero |
| `guia-plazos-fundae.*` | Guía plazos |
| `CNAME` | `boris-bagemihl-formacion.com` |
| `robots.txt` / `sitemap.xml` | SEO (lastmod 2026-08-11) |

---

## DNS / Pages (si aún no está)

| Tipo | Nombre | Valor |
|------|--------|-------|
| A | @ | `185.199.108.153` … `185.199.111.153` |
| CNAME | www | `boris-bagemihl-formacion.github.io` |

Settings → Pages → Custom domain + Enforce HTTPS.

---

## Contenido actual

- **Hero ES/DE:** marca Boris · 1 CTA Form · foto · Fraunces/Source Sans 3 · colores #2c3e50 / #e67e22
- **Sobre mí:** perfil comercial + enlace CV completo
- **Favicon:** monograma BB

---

## Mantenimiento

```bash
cd patrimonio/boris/fundae/web
weasyprint perfil-comercial-boris-bagemihl.html perfil-comercial-boris-bagemihl.pdf
cp perfil-comercial-boris-bagemihl.pdf cv-boris-bagemihl.pdf
cp perfil-comercial-boris-bagemihl.html cv-boris-bagemihl.html
# igual DE: profil-kommerziell → lebenslauf-boris-bagemihl.*
```

Regenerar zip:

```bash
python3 -c "..."  # ver sesión 11/8 o volver a empaquetar esta carpeta
```

---

*Última actualización: agosto 2026*
