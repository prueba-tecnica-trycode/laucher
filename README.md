## Dev

1. Clonar repositorio
```
git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_REPOSITORIO>
```
3. Configurar variables de entorno: `Crea un archivo .env copiando el .env.template`
4. Inicializar submódulos (si es la primera vez)

```
git submodule update --init --recursive
```

4. Construir y ejecutar el proyecto con Docker
```
docker compose up --build
```

## ENDPOINTS

AUTH

### 🔐 **Autenticación (AUTH)**
| Método | Endpoint                         | Descripción                      |
|--------|----------------------------------|----------------------------------|
| `GET`  | `/api/auth/get-user`            | Obtiene todos los usuarios |
| `GET`  | `/api/auth/getby-id/:idUser`    | Obtiene un usuario por su ID |
| `POST` | `/api/auth/login`               | Inicia sesión en la aplicación |
| `POST` | `/api/auth/register`            | Registra un nuevo usuario |

PRODUCTS

### 🔐 **Productos (PRODUCTS)**
| Método | Endpoint                         | Descripción                      |
|--------|----------------------------------|----------------------------------|
| `POST`  | `/api/products/create-product` | Crea un producto si el usuario está autenticado |
| `GET`  | `/api/products/get-products-for-user/:idUser` | Listar todos los productos de un usuario en especifico |
