# Claridad

App minimalista de conciencia financiera. Muestra ingresos y egresos mes a mes con jerarquía: últimos 2 meses detallados, trimestres y años anteriores colapsables.

## Ver la app
- GitHub Pages: habilitar en Settings → Pages → Source: `main` branch
- Local: abrir `index.html` directamente en el navegador

## Seguridad
Todos los datos están cifrados en el cliente con **AES-GCM 256** + **PBKDF2 (200.000 iteraciones)**. El HTML puede estar en un repo público y seguirá siendo ilegible sin la contraseña.

## Cómo regenerar
En el repositorio principal (`Extractos Bancarios`):

```bash
python3 scripts/build_claridad.py 'TU_PASSWORD'
cp reportes/Claridad.html /Users/danielgomez/Documents/claridad-app/index.html
cd /Users/danielgomez/Documents/claridad-app
git add index.html
git commit -m "update: datos al YYYY-MM-DD"
git push
```
