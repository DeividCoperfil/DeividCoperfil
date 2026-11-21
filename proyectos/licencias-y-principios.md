# Licencias y principios de producto

## Control de acceso a los programas
Los programas de escritorio se entregan con **licencia por programa y por equipo**. Un generador de licencias las emite y las registra. La licencia se verifica **en el propio equipo**, con una firma criptográfica: la llave pública va dentro del programa y la privada nunca se versiona. Así el programa no necesita internet ni un servidor para validarse.

## Principios con los que construyo
- **Funciona sin internet**, tal como se entrega.
- **Procesa en el equipo** y no guarda datos de los clientes.
- **Versiones claras desde la 1.0**, con historial de cambios.
- **Repos privados**, y nunca se versionan datos reales, licencias, llaves ni instaladores.
- **Auditoría antes de publicar:** reviso qué archivos van a subirse, busco patrones de datos reales (cédulas, NIT, cuentas) y ejecuto un detector de secretos.

## Una lección que me quedó
Al auditar los programas encontré que **tres de ellos cargaban librerías y fuentes desde internet**, aunque se anunciaban como offline: sin conexión no leían PDF ni Excel. Los clientes no lo habían notado porque tenían internet. Lo corregí en la versión 1.0.1 incluyendo todo dentro del programa, y esta vez lo **verifiqué** abriendo cada uno con todas las conexiones cortadas y contadas, y también empaquetado como corre ya instalado: cero peticiones a internet. Desde entonces no doy por cierto "funciona sin internet" sin haberlo comprobado.
