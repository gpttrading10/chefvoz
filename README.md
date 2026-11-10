# ChefVoz
Aplicación estática de recetas, menú y compra. HTML, CSS y JavaScript sin compilación.

## GitHub Pages
1. Inicia sesión en GitHub con tu cuenta asociada a elgallego2001@gmail.com. El correo no determina tu nombre de usuario ni el dominio de Pages.
2. Crea un repositorio `chefvoz`.
3. Sube el contenido del ZIP (index.html, style.css, app.js y .nojekyll) a la raíz de la rama main.
4. En Settings > Pages elige Deploy from a branch > main > /(root).
5. GitHub te mostrará la URL final. Todos los recursos propios usan rutas relativas.

## Funciones operativas
CRUD y duplicado, fotos por URL o carga comprimida, categoría Varias, favoritos, escalado, calendario semanal de cuatro ingestas, selector visual, lista consolidada por pasillo con conversión kg/g y l/ml, checks, productos manuales, copias JSON, exportación iCalendar y modo cocina con voz si el navegador lo permite.

## Límites actuales
Los datos se guardan en localStorage. La sincronización entre pestañas del mismo origen funciona; no hay sincronización entre dispositivos. La marca pública es solo local. No están implementadas cuentas, autenticación ni repositorio social remoto. No hay OAuth Google ni CalDAV; .ics es una exportación manual. No se ha probado físicamente en Amazon Silk/Echo Show 11; la voz depende de las API disponibles. Las fotos de ejemplo y fuentes necesitan conexión.

## Ampliación recomendada
Para servicio familiar compartido: Supabase Auth + Postgres con tablas hogares, miembros, recetas, ingredientes, pasos, menú y compra. Aplicar RLS por hogar y por propietario; solo recetas publicadas visibles globalmente; importación debe copiar datos con nuevo propietario. Realtime por hogar y escritura por producto evitarán sobrescrituras completas. Requiere configurar un proyecto real y credenciales públicas con políticas RLS antes de activarlo. Para Google: OAuth cliente web, URI de origen del despliegue, scope calendar.events y eventos con IDs persistidos; no guardar tokens en repositorio. Apple: adaptador CalDAV futuro con proxy seguro si fuera necesario.

## Uso
Abre la web, crea recetas, añade comidas en Plan semanal, ajusta sus comensales y genera la compra. Exporta copias periódicas en Ajustes. Borrar datos del navegador borra los datos locales.

## Versión 1.1
Momento de receta con filtros en recetario, selector y comunidad local. Ingredientes y pasos en filas dinámicas; sector automático con selección manual. Compra por tarjetas de sectores y finalización. Se conservan productos manuales al recalcular. El archivo `guia-chefvoz.html` contiene los pasos de prueba y el orden de las funciones pendientes.

Para desplegar también son necesarios `updates.js` y `guia-chefvoz.html` junto a `app.js`, `style.css`, `index.html` y `.nojekyll`.
