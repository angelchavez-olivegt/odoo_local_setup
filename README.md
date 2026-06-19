# odoo17_setup

Sirve para levantar un servicio de odoo 17 local con docker, para poder testear los addons customizados.

# addons

Directorio para guardar los addons customizados.    

```bash
. 
├── docker-compose.yml
├── .env
└── addons/
    └── my_module/
```

# docker-compose.yml

Para iniciar el servicio:

```bash 
cp .env.example .env
cp docker-compose.yml.example docker-compose.yml
```

```bash
docker-compose up -d
```

Para detener el servicio:

```bash
docker-compose down
```

Para detener el servicio y eliminar los contenedores y redes:

```bash
docker-compose down -v
```

# .env

Archivo de variables de entorno para configurar el servicio de docker.
    
## .env.example

```bash
ODOO_DB_NAME=test
ODOO_VERSION=17.0
ODOO_MASTER_PASSWORD=admin
# SOLO REFERENCIA, EMAIL DE LOGIN
ODOO_EMAIL=admin
``` 