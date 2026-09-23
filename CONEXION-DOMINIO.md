# Conectar esenciacafe.es con GitHub Pages

Alojamiento actual: GitHub Pages.
Repositorio: https://github.com/EsenciaCafe/linktree
Web: https://esenciacafe.github.io/linktree/

Estas instrucciones sustituyen las anteriores de Sites. No uses las IP 162.159.143.30 y 172.66.3.26 ni los TXT de OpenAI/Cloudflare del alojamiento anterior.

## 1. Registrar el dominio en GitHub

Abre https://github.com/EsenciaCafe/linktree/settings/pages
En **Custom domain**, escribe `esenciacafe.es` y pulsa **Save**. GitHub creará un archivo CNAME. La dirección de GitHub empezará a redirigir al dominio, por lo que conviene hacer el paso siguiente inmediatamente después.

## 2. Cambiar los registros en DonDominio

Entra en **Dominios → esenciacafe.es → Parking & Zona DNS**. Conserva los servidores DNS de DonDominio.

Configura:

| Tipo | Nombre/Host | Destino |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | esenciacafe.github.io |

`@` significa el dominio raíz esenciacafe.es. Si el formulario no acepta @, usa la opción de raíz o el nombre completo según indique el panel. El destino de www no lleva https:// ni /linktree/.

Sustituye los registros web de parking que entren en conflicto con estos valores (A/AAAA del raíz o A/AAAA/CNAME de www). No borres registros de correo: MX, SPF, DKIM, DMARC ni otros TXT de servicios activos. Mantén el TTL predeterminado.

## 3. Activar HTTPS

Cuando el DNS se haya propagado, vuelve a GitHub → Settings → Pages. Usa **Check again** si aparece y activa **Enforce HTTPS** cuando esté disponible. La propagación y emisión del certificado pueden tardar hasta 24 horas.

Comprueba https://esenciacafe.es y https://www.esenciacafe.es sin iniciar sesión. Solo después cambia el enlace de Instagram a https://esenciacafe.es.

Fuente: https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
