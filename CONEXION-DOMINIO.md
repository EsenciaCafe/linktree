# Dominio de Esencia Café

Web: https://esenciacafe.es
Repositorio: https://github.com/EsenciaCafe/linktree
Alojamiento: GitHub Pages, rama main, carpeta raíz.

## Configuración aplicada el 23/09/2026

- GitHub Pages: dominio personalizado esenciacafe.es (archivo CNAME).
- DonDominio, raíz esenciacafe.es: ANAME a esenciacafe.github.io.
- DonDominio, www.esenciacafe.es: CNAME a esenciacafe.github.io.
- Se conservaron los servidores DNS de DonDominio y todos los registros de correo.

El ANAME sustituye los cuatro registros A manuales: DonDominio resuelve automáticamente las direcciones de GitHub. No añadir simultáneamente los registros del alojamiento anterior.

Valores anteriores, por si se necesita restaurar el parking:
- ANAME raíz: parkingsrv0.dondominio.com
- CNAME www: parkingsrv0.dondominio.com.

El 23/09/2026 el DNS autoritativo ya devolvía las cuatro IPv4 de GitHub Pages. HTTPS activado y comprobado. Tanto https://esenciacafe.es como https://www.esenciacafe.es responden correctamente; www y HTTP redirigen a https://esenciacafe.es. GitHub muestra DNS check successful y Enforce HTTPS activado.

Configuración de Pages: https://github.com/EsenciaCafe/linktree/settings/pages

