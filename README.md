## Indice:
- [Git](https://github.com/Mueltex/cheatsheets/blob/main/git-cheat-sheet.pdf)
## Fases:
- En general: https://cyberhoot.com/cybrary/kill-chain/ https://www.incibe.es/empresas/blog/las-7-fases-ciberataque-las-conoces
- Webs: robots.txt, sitemap, fuzzeo...
- OSINT + Info tecnica y organizativa (LinkedIN, eventos, medium, repos...)
- Wayback machine sitios coorporativos
- Google hacking
- Posibles leaks de credenciales (Have i been pwned)
- Busqueda de máquinas expuestas (shodan)
- Análisis del dominio con whois y del posible ASN asociado a la empresa, rangos públicos para identificar maquinas
- Análisis de dominios y subdominios -> posibles entornos de pruebas o desactualizados, puntos de entrada VPN... (zoomeye, dnsdumpster)
- Phishing dirigido -> Empleados concretos, portales de atención al cliente, soporte... Crafteo de documentos con macros malas o creación de sitios webs especificos. Dar de alta dominios similares. Copiar firmas de empleados legitimos... Ejemplo Google
- Diferenciar si estamos accediendo desde un dispositivo propio o desde un equipo corporativo (virtualizado o no). Si es propio -> cargar credenciales AD (es el mejor caso, si no hay politica de certificados o similar). En cualquier caso, ver segmento de red, detectar hosts vivos, servidores DNS para volcado de entradas, DCs para hacer queries LDAP, ver SMBs con ficheros, posibles relay de correos, logisn default en sitios web, detectar vulnerabilidades, saltar de una bbdd a comandos, sqli...
- Siempre recorrer info hacia atrás
- Siendo admin:
-   Puertas traseras, desactivar EDRs, manipular archivo hosts, crear nuevos usuarios, modificación de archivos legítimos ej. DLL Hijacking, tareas programadas, habilitar nuevos servicios, acceder a contenido de otros usuarios, web shell, reverse shell
- Exfiltracion: DNS, ICMP, sitiow web, repos de codigo, correo, pasar a un pc propio y de ahi salir, FTP, ssh
- - Mitre
  - Baja "latencia" -> si desarrollamos el ataque de manera lenta y distribuida (repartir el escaneo de puertos, realizarlo poco a poco...) evitaremos que nos descubran. Si el ataque es prolongado en el tiempo, puede que la organización no tenga capacidad para almacenar logs durante tanto tiempo.
## Herramientas
| Herramienta      | Descripcion | API Oficial | Implementación|
| ----------- | ----------- | ----------- | ----------- |
| [DNSDumpster](https://dnsdumpster.com/)      | En base a un dominio busca todos sus subdominios visibles. Enumera puertos y servicios. Resultado descargable en formato Excel y con imágenes que relacionan los subdominios localizados       | No ❌ | [Sí ✔️](https://github.com/PaulSec/API-dnsdumpster.com) |
| [urlscan.io](https://urlscan.io/)      | Escanea y analiza sitios web mostrando: dominios e IPs relacionados, peticiones que realiza la web, contenido DOM y screenshot del sitio, redirecciones...       | [Sí ✔️](https://urlscan.io/docs/api/) | [Sí ✔️](https://urlscan.io/docs/integrations/) |
| VirusTotal | ----------- | ----------- | ----------- |
| JoeSandbox | ----------- | ----------- | ----------- |
| AbuseIpDb | ----------- | ----------- | ----------- |
| censys | ----------- | ----------- | ----------- |
| zoomeye | ----------- | ----------- | ----------- |
| [cyberchef](https://gchq.github.io/CyberChef/) | ----------- | ----------- | ----------- |
| [winpeas](https://github.com/carlospolop/PEASS-ng/tree/master/winPEAS) | ----------- | ----------- | ----------- |
| [linpeas](https://github.com/carlospolop/PEASS-ng/tree/master/linPEAS) | ----------- | ----------- | ----------- |
| [revshell generator](https://www.revshells.com/) | ----------- | ----------- | ----------- |
| [reverse shell pentest monkey](https://pentestmonkey.net/cheat-sheet/shells/reverse-shell-cheat-sheet) | ----------- | ----------- | ----------- |
| [webshells](https://github.com/BlackArch/webshells/tree/master/php) | ----------- | ----------- | ----------- |
linenum - https://github.com/rebootuser/LinEnum/blob/master/LinEnum.sh
Checklist escalada Linux - https://book.hacktricks.xyz/linux-hardening/linux-privilege-escalation-checklist
Checklist escalada Windows - https://book.hacktricks.xyz/windows-hardening/checklist-windows-privilege-escalation
Checklist persistencia Linux - https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Linux%20-%20Persistence.md - https://www.linode.com/docs/guides/linux-red-team-persistence-techniques/
Checklist persistencia Windows - https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/Methodology%20and%20Resources/Windows%20-%20Persistence.md https://www.linode.com/docs/guides/windows-red-team-persistence-techniques/
GTFOBINS Linux - https://gtfobins.github.io/gtfobins/vi/#sudo
LOLBAS Windows - https://lolbas-project.github.io/#
Vulnerabilidades - https://www.exploit-db.com
Windows File Transfer - https://juggernaut-sec.com/windows-file-transfers-for-hackers/#Downloading_and_Uploading_Files_Using_evil-winrm
Esquema movimientos AD Orange - https://orange-cyberdefense.github.io/ocd-mindmaps/img/pentest_ad_dark_2022_11.svg
Port forwarding with chisel - https://notes.benheater.com/books/network-pivoting/page/port-forwarding-with-chisel
Chisel - https://github.com/jpillora/chisel/releases/tag/v1.8.1
SQL Injection Cheatshet Portswigger - https://portswigger.net/web-security/sql-injection/cheat-sheet
Powershell port scan - https://medium.com/@nallamuthu/powershell-port-scan-bf27fc754585
Privileges to admin Windows - https://github.com/gtworek/Priv2Admin
OSINT Checklist - https://techjournalism.medium.com/osint-checklist-for-company-investigations-86c3752c095d
Busqueda google https://www.exploit-db.com/google-hacking-database
HAVE I BEEN PWNED - https://haveibeenpwned.com/
SHODAN - https://www.shodan.io/
Persistence sniper - https://github.com/last-byte/PersistenceSniper
FOCA y Maltego - https://github.com/ElevenPaths/FOCA - https://www.maltego.com/
ASN Lookup - https://hackertarget.com/as-ip-lookup/
WhoIs - https://who.is/
Contenedor Kali - https://www.kali.org/docs/containers/using-kali-docker-images/
Comprobar regex - https://regex101.com/
Regex Cheatsheet - https://www.datacamp.com/cheat-sheet/regular-expresso
Hacktricks
Hackplayers

