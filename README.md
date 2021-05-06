​                                                                                   ![[image-20210506104427925](https://t.me/aitorroma)](https://tva1.sinaimg.cn/large/008i3skNgy1gq8sv4q7cqj303k03kweo.jpg)

## ![img](https://www.instagram.com/favicon.ico) Tú Radio en Instagram

Aprovechando [el post que hice el otro día en el canal](https://t.me/aitorroma/244) dando a conocer [YellowDuck](https://yellowduck.tv/) vamos a ver como retransmitir un stream de radio directamente en Instagram.

Para ello lo que vamos a hacer es descargarnos el repositorio.

```bash
$ git clone https://github.com/aitorroma/radioinsta
$ cd radioinsta
```

El repositorio esta compuesto por 3 ficheros.

```bash
➜  radioinsta tree -a
.
├── .env
├── docker-compose.yml
├── radio.jpg
└── README.md
```

- **.env** ( Fichero de configuración )

- **docker-compose.yml** ( Fichero de despliegue de la radio en docker )

- **radio.jpg** ( Imagen de la historia de instagram )

  

  <img src="https://tva1.sinaimg.cn/large/008i3skNgy1gq8xfx379pj30fk0rw18l.jpg" alt="image-20210506132247978" style="zoom:50%;" />

  

  La Imagen radio.jpg puedes crear-la en [Canva](https://canva.com) usando la template de historia de instagram.

Una vez dentro del directorio debemos editar varias cosas en el fichero *.env*

```bash
vim .env

KEY=17991555220327522?s_sw=0&s_vt=ig&a=Aby60bfS13fhYmlp
STREAM=https://alfarras.covid-remote.work/radio/8000/radio.mp3
```

El valor KEY se obtiene de **[YellowDuck](https://yellowduck.tv/)** el STREAM es algún servidor de radio en Icecast por ejemplo que tengas.

<img src="https://tva1.sinaimg.cn/large/008i3skNgy1gq8xhgxp9fj30kk0kaad4.jpg" alt="image-20210506132418797" style="zoom:50%;" />

Una vez tengas todos los datos completados debes ejecutar el comando.

```bash
docker-compose up -d
```

**Para parar la radio puedes ejecutar.**

```bash
docker-compose down
```

**Para reiniciar la radio.**

```bash
docker-compose restart
```

**Para ver logs**

```bash
docker-compose logs
```

---------------------------------

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/J3J64AN17)

