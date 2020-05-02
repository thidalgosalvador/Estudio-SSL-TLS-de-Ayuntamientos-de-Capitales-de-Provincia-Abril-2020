# Estudio SSL-TLS de Ayuntamientos de Capitales de Provincia - Abril-2020
Estudio SSL/TLS de la web oficial y sede electrónica de los ayuntamientos de las capitales de provincia de España. Abril 2020.

### Introducción
El presente estudio presenta un estado básico de la seguridad de las webs institucionales y sedes electrónicas de las capitales de provincia de España. Se han incluido en el mismo las ciudades autónomas de Ceuta y Melilla. Focalizado en configuración de protocolos de comunicaciones, cifrados utilizados y otros parámetros, se plantea desde un punto de vista general, meramente estadístico, sin entrar en el detalle de configuraciones particulares. Para profundizar en la seguridad aplicable a los servicios electrónicos de las Administraciones Públicas -y su posible mejora- se recomienda visitar la plataforma [EVENTS](https://www.ccn-cert.cni.es/evens/), que recopila todos los recursos del Esquema Nacional de Seguridad en un único entorno.

| Comunidad autónoma          | Capitales |
|----------------------------:|------:|
|  Andalucía                  | 8     |
|  Aragón                     | 3     |
|  Canarias                   | 2     |
|  Cantabria                  | 1     |
|  Castilla y León            | 9     |
|  Castilla\-La Mancha        | 5     |
|  Cataluña                   | 4     |
|  Ceuta  (\*)                | 1     |
|  Comunidad de Madrid        | 1     |
|  Comunidad Foral de Navarra | 1     |
|  Comunidad Valenciana       | 3     |
|  Extremadura                | 2     |
|  Galicia                    | 4     |
|  Islas Baleares             | 1     |
|  La Rioja                   | 1     |
|  Melilla  (\*)              | 1     |
|  País Vasco                 | 3     |
|  Principado de Asturias     | 1     |
|  Región de Murcia           | 1     |

(\*) = Ciudad Autónoma

### Webs y Sedes Electrónicas bajo HTTPS
De las 52 capitales de provincia,seis de ellas, en su web institucional, no ofrecen los contenidos bajo HTTPS.
| Uso de HTTPS   | Webs | %     | Sede Elec\. | %      |
|---------------:|-----:|------:|------------:|-------:|
| Configurado    | 46   | 88,5% |52          | 100,0% |
| No configurado | 6    | 11,5% |0|0,0%|

Hay añgunas webs institucionales y sedes electrónicas que no redireccionan directamente a contenido HTTPS cuando se invocan bajo HTTP.

| Redireccion | Webs | Sedes |
|------------:|-----:|------:|
| Código 200         | 9    | 1     |
| Código 30x         | 37   | 51    |

Así mismo, llama la atención la baja implantación de HSTS. HTTP Strict Transport Security (HSTS) es una política de seguridad web que permite a un servidor web imponer/forzar el uso de TLS para los User-Agent compatibles, como -por ejemplo- un navegador web. El HSTS permite una implementación más efectiva del TLS asegurando que toda la comunicación se lleve a cabo sobre una capa de transporte segura en el lado del cliente. En particular, el HSTS mitiga las variantes de los ataques de "hombre en el medio" (MiTM) en los que el TLS puede ser eliminado de las comunicaciones con un servidor, dejando al usuario vulnerable a mayores riesgos.
| HSTS           | Webs | %  | Sedes | %     |
|---------------:|-----:|------:|------:|------:|
| Configurado    | 7    | 15,2% | 9     | 17,3% |
| No configurado | 39   | 84,8% | 43    | 82,7% |

### HTTP/2.0
HTTP/2 es un protocolo que se ofrece tan solo bajo HTTPS y aporta una mejora significativa en eficiencia, velocidad y seguridad. Además, es compatible con la mayoría de los [navegadores web](https://caniuse.com/#search=http2) modernos. 
| Protocolo | Webs | %      | Sedes Elec\. | %      |
|----------:|-----:|-------:|-------------:|-------:|
| HTTP/1\.1 | 46   | 100,0% | 52           | 100,0% |
| HTTP/2\.0 | 10   | 21,7%  | 2            | 3,8%   |

El 21,7% de las webs institucionales ofrecen HTTP/2, cifra que cae al 3,8% (tan solo dos) en las sedes electrónicas.

### Server Signature
La firma del servidor (en inglés, Server Signature) es la identidad pública del servidor web. Contiene información sensible que -en general- como buena práctica de seguridad se suele desactivar para evitar la divulgación de las versiones de software utilizadas.
| Server Signature     | Webs | %     | sedes | %     |
|----------------------|------|-------|-------|-------|
| Apache v2\.2 / v2\.4 | 19   | 41,3% | 17    | 32,7% |
| Apache\-Coyote/1\.1  | 1    | 2,2%  | 8     | 15,4% |
| nginx                | 5    | 10,9% | 8     | 15,4% |
| Microsoft\-IIS/7\.5  | 1    | 2,2%  | 5     | 9,6%  |
| No especificado      | 8    | 17,4% | 5     | 9,6%  |
| Microsoft\-IIS/8\.5  | 2    | 4,3%  | 2     | 3,8%  |
| Bilbao WebServer     | 1    | 2,2%  | 1     | 1,9%  |
| Big IP               | 1    | 2,2%  | 1     | 1,9%  |
| inter@CEMI           | 1    | 2,2%  | 1     | 1,9%  |
| Microsoft\-IIS/10\.0 | 0    | 0,0%  | 1     | 1,9%  |
| Microsoft\-IIS/6\.0  | 2    | 4,3%  | 1     | 1,9%  |
| OpenCms/7\.5\.2      | 1    | 2,2%  | 1     | 1,9%  |
| WildFly/9            | 1    | 2,2%  | 1     | 1,9%  |
| AkamaiGHost          | 1    | 2,2%  | 0     | 0,0%  |
| cloudflare           | 1    | 2,2%  | 0     | 0,0%  |
| Lotus\-Domino        | 1    | 2,2%  | 0     | 0,0%  |


### Certificados digitales

#### Entidades Emisoras (CA’s)
Respecto a los PSCs (Prestadores de Servicios de Confianzan) que emiten certificados para las webs y sedes, la entidad Camerfirma -seguida de Digicert y FNMT- lideran esta lista, concentrando entre las tres entidades entre el 50-60%.

| Emisor CA           | Webs | %     |
|--------------------:|----:|------:|
| AC Camerfirma S\.A  | 13  | 25,0% |
| DigiCert Inc        | 10  | 19,2% |
| FNMT\-RCM           | 7   | 13,5% |
| Contenido bajo HTTP | 6   | 11,5% |
| Let's Encrypt       | 4   | 7,7%  |
| ACCV                | 3   | 5,8%  |
| IZENPE S\.A\.       | 3   | 5,8%  |
| GlobalSign nv\-sa   | 2   | 3,8%  |
| Sectigo Limited     | 2   | 3,8%  |
| CloudFlare, Inc\.   | 1   | 1,9%  |
| COMODO CA Limited   | 1   | 1,9%  |

En las sedes electrónicas de los 52 ayuntamientos, esta es la lista de Prestadores de Servicios de Confianza (PSC) que emiten los certificados digitales utilizados para securizar el servicio.
| Emisor CA           | Sede Elec\. | %     |
|--------------------:|------------:|------:|
| AC Camerfirma S\.A  | 21          | 40,4% |
| FNMT\-RCM           | 10          | 19,2% |
| DigiCert Inc        | 6           | 11,5% |
| ACCV                | 5           | 9,6%  |
| IZENPE S\.A\.       | 3           | 5,8%  |
| GlobalSign nv\-sa   | 2           | 3,8%  |
| Let's Encrypt       | 2           | 3,8%  |
| Firmaprofesional    | 1           | 1,9%  |
| GoDaddy\.com, Inc\. | 1           | 1,9%  |
| Sectigo   | 1           | 1,9%  |


#### Tamaño de Clave
Más del 90% de ayuntamientos, tanto para su web institucional como para su sede electrónica, apuestan por un certificado RSA de 2048 bits. Tan solo una institución utiliza un certificado con algoritmos de Curva Eliptica (ECDSA), mientras que un total de ocho (3 en web y 5 en Sede) utilizan una tamaño de clave de 4096 bits.
| Key Size      | Webs | %     | Sede Elec. | %     |
|--------------:|----:|------:|-----:|------:|
| RSA 2048 bits | 42  | 91,3% | 47   | 90,4% |
| RSA 4096 bits | 3   | 6,5%  | 5    | 9,6%  |
| ECDSA\_P256   | 1   | 2,2%  | \-   | 0%   |


#### Registro CAA
En lo que respecta a la implantación de mecanismos de control de emisión de certificados, tan solo dos instituciones del estudio implementa CAA en sus dominios. CAA (Certificate Authority Authorization) es un registro DNS que especifica aquella(s) CA(s) que pueden emitir un certificado digital para el nombre de dominio correspondiente. Los registros de CAA son verificados por las CA antes de emitir el certificado digital.
| CAA            | Webs | %     | Sede Elec\. | %     |
|---------------:|-----:|------:|------------:|------:|
| No configurado | 44   | 91,7% | 50          | 96,2% |
| Configurado    | 2    | 4,2%  | 2           | 3,8%  |


#### Cadena de confianza
Relacionado con los certificados digitales, la configuración en la parte servidor de la cadena de confianza, según las buenas prácticas, debe ofrece el certificado final junto con la jerarquía de certificados de la CA emisora (sin agregar la CA raíz, o rootCA). Un 41,3% de las webs (19 de ellas) y el 50% de las Sees Electrónicas (26) muestran errores a la hora de enviar la cadena de confianza.
| Jerarquía   | Webs | %     | Sede Elec\. | %     |
|------------:|-----:|------:|------------:|------:|
| Correcta    | 27   | 58,7% | 26          | 50,0% |
| Con errores | 19   | 41,3% | 26          | 50,0% |

#### Validación de certificados

En el inicio de la comunicación segura entre un cliente (navegador web) y el servidor web de la sede electrónica se realiza el proceso de validación del certificado digital facilitado por el servidor. Esta validación se puede realizar mediante protocolo OCSP o a través de listas CRL.

La opción más óptima para conocer el estado de revocación de un certificado digital consiste es configurar OCSP Stapling. En este caso, es el servidor quien realiza el proceso de validación del certificado, y el resultado se lo envía al cliente en la negociación inicial TLS, eliminando la necesidad de que los clientes se pongan en contacto con el CA.
| OCSP Stapling  | web | %     | sede | %     |
|---------------:|----:|------:|-----:|------:|
| No configurado | 39  | 84,8% | 45    | 86,5% |
| Configurado    | 7   | 15,2% | 7   | 13,5% |

### Protocolos y cifrados
#### Protocolos SSL/TLS
Por defecto, el 78,3% de las webs y el 86,5% de las S.E. negocian la comunicación bajo el protocolo TLS v1.2. Destaca en el estudio que seis webs y cuatro sedes ya ofrecen por defecto la version TLS v1.3. que mayor seguridad y rendimiento. Así mismo, aún hay webs y sedes que ofrecen a los sumo TLS v1.0.
| Protocolo por defecto | webs | %     | Sede Elec\. | %     |
|----------------------:|-----:|------:|------------:|------:|
| TLS1\.0               | 4    | 8,7%  | 3           | 5,8%  |
| TLS1\.2               | 36   | 78,3% | 45          | 86,5% |
| TLS1\.3               | 6    | 13,0% | 4           | 7,7%  |

La triada formada por los protocolos en su version 1.0, 1.1 y 1.2 es la opción preferida tanto en webs (33) como en sedes (39). La opciones que se podrían considerar más seguras (TLSv1.2 + TLSv.1.3) o (TLSv1.2) están configuradas en 6 (4+2) y 3 (1+2), respectivamente.
| Combinación Protocolos                    | Webs | %     | Sedes Elec\. | %     |
|------------------------------------------:|-----:|------:|-------------:|------:|
| TLSv1 \+ TLSv1\.1 \+ TLSv1\.2             | 33   | 71,7% | 39           | 75,0% |
| TLSv1                                     | 4    | 8,7%  | 3            | 5,8%  |
| TLSv1\.2 \+ TLSv1\.3                      | 4    | 8,7%  | 2            | 3,8%  |
| TLSv1\.1 \+ TLSv1\.2                      | 2    | 4,3%  | 4            | 7,7%  |
| TLSv1 \+ TLSv1\.1 \+ TLSv1\.2 \+ TLSv1\.3 | 2    | 4,3%  | 2            | 3,8%  |
| TLSv1\.2                                  | 1    | 2,2%  | 2            | 3,8%  |

#### Conjunto de Cifrados (Ciphersuite)
Tras el protocolo, el tipo de cifrado (ciphersuite) constituye un parámetro fundamental para la seguridad de la comunicación entre el servidor y el cliente. Chipersuite indica el tipo de cifrado simétrico que se usará entre ambos extremos para el ciofrado final de los datos.

Uno de los parámetros que refuerza el concepto de seguridad consiste en que el servidor fuerce su lista de ciphers en la negociación con el cliente; y no al revés. De esta forma se evita que un cliente quiera negociar con un cifrado débil antes que con uno más fuerte. En el estudio, el 25% de las sedes (13) y el 37% de las webs institucionales (17) no fuerzan en sus configuraciones que sea el servidor quien negocie la lista de ciphersuites.
| Orden Cipher | Webs | %     | Sede Elec\. | %     |
|-------------:|------|------:|------------:|------:|
| Servidor     | 29   | 63,0% | 39          | 75,0% |
| Cliente      | 17   | 37,0% | 13          | 25,0% |

Las últimas tendencias marcan el uso de cifrados fuertes con modos de operación en bloques (AEAD); TLS v1.3 ya solo utiliza ciphesuites del tipo AEAD. Pero por compatibilidad con clientes antiguos se siguen ofreciendo cifrados débiles.

| CipherList                       | Webs | Sede Elec\. |
|---------------------------------:|-----:|------------:|
| STRONG\+MEDIUM                   | 18   | 21          |
| STRONG\+MEDIUM\+3DES             | 12   | 14          |
| STRONG\+MEDIUM\+3DES\+LOW        | 9    | 8           |
| MEDIUM\+3DES                     | 1    | 2           |
| MEDIUM                           | \-   | 1           |
| MEDIUM\+LOW                      | \-   | 1           |
| STRONG\+MEDIUM\+LOW              | \-   | 1           |
| 3DES\+LOW                        | \-   | 1           |
| MEDIUM\+3DES\+LOW                | 2    | 1           |
| STRONG\+MEDIUM\+ANULL            | \-   | 1           |
| STRONG\+MEDIUM\+3DES\+LOW\+NULL  | \-   | 1           |
| STRONG                           | 2    | \-          |
| 3DES\+LOW\+EXPORT                | 1    | \-          |
| STRONG\+MEDIUM\+LOW\+3DES\+ANULL | 1    | \-          |

Destaca negativamente el uso de protocolos aNULL, que no aportan ni cifrado ni autenticación, en alguna web y sede. Del mismo modo se sigue usando tambien cifrados LOW (del tipo RC2, RC4 o DES).

El orden de los cifrados más usados tanto en webs institucionales como en sedes electrónicas es idéntico. El cifrado TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384 es el más utilizado como primera opción en webs (31) y en sede electrónica (34).
| Orden | Cipher\_Hex | CipherName                                   | Webs | Sedes |
|-------|-------------|----------------------------------------------|------|-------|
| 1     | xc030       | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 | 31   | 34    |
| 2     | xc028       | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_CBC\_SHA384 | 30   | 34    |
| 3     | xc014       | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_CBC\_SHA    | 30   | 34    |
| 4     | x9f         | TLS\_DHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384   | 24   | 27    |
| 5     | x6b         | TLS\_DHE\_RSA\_WITH\_AES\_256\_CBC\_SHA256   | 19   | 18    |

Los 10 ciphersuite más utilizados de forma general sería:
| Cipher\_Hex | CipherName                                   | Webs | Sedes |
|-------------|----------------------------------------------|------|-------|
| xc014       | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_CBC\_SHA    | 39   | 44    |
| xc013       | TLS\_ECDHE\_RSA\_WITH\_AES\_128\_CBC\_SHA    | 39   | 43    |
| x2f         | TLS\_RSA\_WITH\_AES\_128\_CBC\_SHA           | 38   | 41    |
| x35         | TLS\_RSA\_WITH\_AES\_256\_CBC\_SHA           | 38   | 41    |
| xc02f       | TLS\_ECDHE\_RSA\_WITH\_AES\_128\_GCM\_SHA256 | 38   | 38    |
| xc027       | TLS\_ECDHE\_RSA\_WITH\_AES\_128\_CBC\_SHA256 | 37   | 43    |
| xc028       | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_CBC\_SHA384 | 37   | 43    |
| xc030       | TLS\_ECDHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 | 37   | 38    |
| x3c         | TLS\_RSA\_WITH\_AES\_128\_CBC\_SHA256        | 33   | 40    |
| x3d         | TLS\_RSA\_WITH\_AES\_256\_CBC\_SHA256        | 33   | 39    |

### Cabeceras de Seguridad

Para la mejora de la seguridad de sitios webs, existen una serie de cabeceras de respuesta HTTP relacionadas con la seguridad que aportan niveles adicionales de protección. Una práctica recomendada consiste en implementar este tipo de cabeceras, siempre que sea posible. Servicios online gratuitos como [Security Headers](https://securityheaders.com/) proporciona un mecanismo para evaluar el estado actual del servidor, y desplegar aquellas cabeceras pendientes.

| Grado | Webs | %     | Sedes Elec\. | %     |
|------:|-----:|------:|-------------:|------:|
| A     | 3    | 6,5%  | 2            | 3,8%  |
| B     | 1    | 2,2%  | \-           | 0,0%  |
| C     | 1    | 2,2%  | 2            | 3,8%  |
| D     | 19   | 41,3% | 13           | 25,0% |
| E     | 1    | 2,2%  | \-           | 0,0%  |
| F     | 21   | 45,7% | 35           | 67,3% |

Las cabeceras de seguridad más utilizadas se muestran en la siguiente tabla:
| Cabecera                    | Webs | Sedes |
|----------------------------:|-----:|------:|
| X\-Frame\-Options           | 21   | 11    |
| X\-Content\-Type\-Options   | 20   | 8     |
| X\-XSS\-Protection          | 13   | 1     |
| Strict\-Transport\-Security | 7    | 9     |
| Content\-Security\-Policy   | 4    | 3     |
| Expect\-CT                  | 2    | 2     |
| Feature\-Policy             | 2    | 1     |
| Referrer\-Policy            | 2    | 1     |

### Herramientas y documentos

Para la obtención de los datos necesarios para realizar el estudio se han utilizado las siguientes herramientas:

- Script SSL Certificate Check - http://prefetch.net/code/ssl-cert-check 
- Script testssl.sh-3.0 – https://github.com/drwetter/testssl.sh
- SSL labs Test - https://www.ssllabs.com/ssltest/
- Hardenize - https://www.hardenize.com/
- Immuniweb SSL Security Test - https://www.immuniweb.com/ssl/
- Security Headers - https://securityheaders.com/
- Lista Ciphersuites en Hex - https://testssl.sh/openssl-iana.mapping.html
- Security/Server Side TLS - https://wiki.mozilla.org/Security/Server_Side_TLS
- Mozilla SSL Configuration Generator - https://ssl-config.mozilla.org/
- OWASP TLS - https://cheatsheetseries.owasp.org/cheatsheets/TLS_Cipher_String_Cheat_Sheet.html


### Anexo 1 - Webs y Sedes electrónicas de los ayuntamientos de Capitales de Provincia.

| Comunidad autónoma          | Ciudad                     | Web                          | Sede electronica                           |
|----------------------------:|---------------------------:|-----------------------------:|-------------------------------------------:|
|  Andalucía                  | Almería                    | www\.almeriaciudad\.es       | sede\.aytoalmeria\.es                      |
|  Andalucía                  | Cádiz                      | institucional\.cadiz\.es     | tramita\.cadiz\.es                         |
|  Andalucía                  | Córdoba                    | www\.cordoba\.es             | sede\.cordoba\.es                          |
|  Andalucía                  | Granada                    | www\.granada\.org            | sedeelectronica\.granada\.org              |
|  Andalucía                  | Huelva                     | www\.huelva\.es              | www\.huelva\.es                            |
|  Andalucía                  | Jaén                       | www\.aytojaen\.es            | sede\.aytojaen\.es                         |
|  Andalucía                  | Málaga                     | www\.malaga\.eu              | sede\.malaga\.eu                           |
|  Andalucía                  | Sevilla                    | www\.sevilla\.org            | www\.sevilla\.org                          |
|  Aragón                     | Huesca                     | www\.huesca\.es              | sedeelectronica\.huesca\.es                |
|  Aragón                     | Teruel                     | www\.teruel\.es              | sede\.teruel\.es                           |
|  Aragón                     | Zaragoza                   | www\.zaragoza\.es            | www\.zaragoza\.es                          |
|  Canarias                   | Las Palmas de Gran Canaria | www\.laspalmasgc\.es         | www\.laspalmasgc\.es                       |
|  Canarias                   | Santa Cruz de Tenerife     | www\.santacruzdetenerife\.es | sede\.santacruzdetenerife\.es              |
|  Cantabria                  | Santander                  | santander\.es                | sede\.santander\.es                        |
|  Castilla y León            | Ávila                      | www\.avila\.es               | sede\.avila\.es                            |
|  Castilla y León            | Burgos                     | www\.aytoburgos\.es          | sede\.aytoburgos\.es                       |
|  Castilla y León            | León                       | www\.aytoleon\.es            | sede\.aytoleon\.es                         |
|  Castilla y León            | Palencia                   | www\.aytopalencia\.es        | sede\.aytopalencia\.es                     |
|  Castilla y León            | Salamanca                  | www\.aytosalamanca\.es       | www\.aytosalamanca\.gob\.es                |
|  Castilla y León            | Segovia                    | www\.segovia\.es             | sede\.segovia\.es                          |
|  Castilla y León            | Soria                      | www\.soria\.es               | soria\.sedelectronica\.es                  |
|  Castilla y León            | Valladolid                 | www\.valladolid\.es          | www\.valladolid\.gob\.es                   |
|  Castilla y León            | Zamora                     | www\.zamora\.es              | zamora\.sedelectronica\.es                 |
|  Castilla\-La Mancha        | Albacete                   | www\.albacete\.es            | albacete\.sedipualba\.es                   |
|  Castilla\-La Mancha        | Ciudad Real                | www\.ciudadreal\.es          | www\.ciudadreal\.es                        |
|  Castilla\-La Mancha        | Cuenca                     | www\.cuenca\.es              | sede\.cuenca\.es                           |
|  Castilla\-La Mancha        | Guadalajara                | www\.guadalajara\.es         | guadalajara\.sedelectronica\.es            |
|  Castilla\-La Mancha        | Toledo                     | www\.toledo\.es              | sede\.toledo\.es                           |
|  Cataluña                   | Barcelona                  | ajuntament\.barcelona\.cat   | seuelectronica\.ajuntament\.barcelona\.cat |
|  Cataluña                   | Gerona                     | web\.girona\.cat             | seu\.girona\.cat                           |
|  Cataluña                   | Lérida                     | www\.paeria\.es              | seu\.paeria\.cat                           |
|  Cataluña                   | Tarragona                  | www\.tarragona\.cat          | seu\.tarragona\.cat                        |
|  Ceuta                      | Ceuta                      | www\.ceuta\.es               | sede\.ceuta\.es                            |
|  Comunidad de Madrid        | Madrid                     | www\.madrid\.es              | sede\.madrid\.es                           |
|  Comunidad Foral de Navarra | Pamplona                   | www\.pamplona\.es            | sedeelectronica\.pamplona\.es              |
|  Comunidad Valenciana       | Alicante                   | www\.alicante\.es            | sedeelectronica\.alicante\.es              |
|  Comunidad Valenciana       | Castellón de la Plana      | www\.castello\.es            | sede\.castello\.es                         |
|  Comunidad Valenciana       | Valencia                   | www\.valencia\.es            | sede\.valencia\.es                         |
|  Extremadura                | Badajoz                    | www\.aytobadajoz\.es         | www\.aytobadajoz\.es                       |
|  Extremadura                | Cáceres                    | www\.ayto\-caceres\.es       | sede\.caceres\.es                          |
|  Galicia                    | La Coruña                  | www\.coruna\.gal             | sede\.coruna\.gob\.es                      |
|  Galicia                    | Lugo                       | lugo\.gal                    | lugo\.gal                                  |
|  Galicia                    | Orense                     | www\.ourense\.gal            | sede\.ourense\.gob\.es                     |
|  Galicia                    | Pontevedra                 | www\.pontevedra\.gal         | sede\.pontevedra\.gal                      |
|  Islas Baleares             | Palma                      | www\.palma\.cat              | seuelectronica\.palma\.es                  |
|  La Rioja                   | Logroño                    | www\.xn\-\-logroo\-0wa\.es   | sedeelectronica\.logrono\.es               |
|  Melilla                    | Melilla                    | www\.melilla\.es             | sede\.melilla\.es                          |
|  País Vasco                 | Bilbao                     | www\.bilbao\.eus             | www\.bilbao\.eus                           |
|  País Vasco                 | San Sebastián              | www\.donostia\.eus           | www\.donostia\.eus                         |
|  País Vasco                 | Vitoria                    | www\.vitoria\-gasteiz\.org   | sedeelectronica\.vitoria\-gasteiz\.org     |
|  Principado de Asturias     | Oviedo                     | www\.oviedo\.es              | sede\.oviedo\.es                           |
|  Región de Murcia           | Murcia                     | www\.murcia\.es              | sede\.murcia\.es                           |

