# Estudio SSL-TLS de Ayuntamientos de Capitales de Provincia - Abril-2020
Estudio SSL/TLS de las web oficial y sedes electrónica de los Aytos. Capitales de Provincia de España. Abril 2020

### Introducción

| Comunidad autónoma          | Capitales |
|----------------------------:|------:|
|  Andalucía                  | 8     |
|  Aragón                     | 3     |
|  Canarias                   | 2     |
|  Cantabria                  | 1     |
|  Castilla y León            | 9     |
|  Castilla\-La Mancha        | 5     |
|  Cataluña                   | 4     |
|  Ceuta                      | 1     |
|  Comunidad de Madrid        | 1     |
|  Comunidad Foral de Navarra | 1     |
|  Comunidad Valenciana       | 3     |
|  Extremadura                | 2     |
|  Galicia                    | 4     |
|  Islas Baleares             | 1     |
|  La Rioja                   | 1     |
|  Melilla                    | 1     |
|  País Vasco                 | 3     |
|  Principado de Asturias     | 1     |
|  Región de Murcia           | 1     |


### Webs y Sedes Electrónicas bajo HTTPS
#### Webs institucionales
De las 52 capitales de provincia,seis de ellas, en su web institucional, no ofrecen los contenidos bajo HTTPS.
| Uso de HTTPS   | Webs | %     |
|---------------:|-----:|------:|
| Configurado    | 46   | 88,5% |
| No configurado | 6    | 11,5% |

#### Sede Electrónicas
En el caso de las sedes electrónicas, el 100% se ofrecen bajo HTTPS.
| Uso de HTTPS | Sede Elec\. | %      |
|--------------|-------------|--------|
| Configurado  | 52          | 100,0% |


### Server Signature
La firma del servidor (en inglés, Server Signature) es la identidad pública del servidor web. Contiene información sensible que -en general- como buena práctica de seguridad se suele desactivar para evitar la divulgación de las versiones de software utilizadas.


### Certificados digitales

#### Entidades Emisoras (CA’s)
Respecto a los PSCs (Prestadores de Servicios de Confianzan) que emiten certificados para las webs y sedes, la entidad Camerfirma -seguida de Digicert y FNMT- lideran esta lista, concentrando entre las tres entidades entre el 50-60%.

| Emisor CA           | web | %     |
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
| Key Size      | web | %     | Sede Elec. | %     |
|--------------:|----:|------:|-----:|------:|
| RSA 2048 bits | 42  | 91,3% | 47   | 90,4% |
| RSA 4096 bits | 3   | 6,5%  | 5    | 9,6%  |
| ECDSA\_P256   | 1   | 2,2%  | \-   | 0%   |


#### Registro CAA


#### Cadena de confianza


### Anexo 1 - Webs y Sedes electrónicas de los ayuntamientos de Capitales de Pronvicia.

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

