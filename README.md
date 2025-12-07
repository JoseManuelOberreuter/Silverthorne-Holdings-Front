# Silverthorne Holdings - Frontend

Aplicación web frontend para **Silverthorne Holdings**, empresa dedicada a la prestación de servicios informáticos y venta de insumos tecnológicos. Desarrollada con Vue.js 3, Composition API y Vite.

## Características

- **Diseño Moderno y Responsive**: Interfaz intuitiva que se adapta a todos los dispositivos
- **Vue.js 3 con Composition API**: Código moderno y mantenible
- **Vite**: Desarrollo rápido con Hot Module Replacement (HMR)
- **Completamente Responsive**: Optimizado para móviles, tablets y desktop
- **Gestión de Estado**: Pinia para manejo de estado global
- **Carrito de Compras**: Sidebar deslizable con gestión completa
- **Autenticación**: Login, registro y gestión de perfil
- **Catálogo de Productos**: Búsqueda, filtros y categorías
- **Sistema de Pagos**: Integración con Transbank (Webpay Plus)
- **Órdenes**: Seguimiento de pedidos y historial
- **Panel de Administración**: Gestión de productos, órdenes y estadísticas
- **Notificaciones**: Sistema de notificaciones en tiempo real
- **Formulario de Contacto**: Comunicación directa con la empresa

## Requisitos Previos

### Software Requerido

- **Node.js**: Versión 14.0.0 o superior (recomendado: v18 LTS o v20 LTS)
- **npm**: Versión 6.0.0 o superior (incluido con Node.js)
- **Git**: Versión 2.20.0 o superior

### Servicios Externos

- **Backend API**: Backend de Silverthorne Holdings desplegado (local o en Vercel)
- **Vercel** (OBLIGATORIO para producción): Hosting del frontend
  - Cuenta gratuita disponible en: https://vercel.com/

### Navegadores Soportados

- Google Chrome: Versión 90 o superior (recomendado)
- Mozilla Firefox: Versión 88 o superior
- Microsoft Edge: Versión 90 o superior
- Safari: Versión 14 o superior (macOS)
- Opera: Versión 76 o superior

## Instalación Local

### Paso 1: Clonar el Repositorio

```bash
git clone <url-del-repositorio>
cd ProyectoDeTitulo/Frontend
```

### Paso 2: Instalar Dependencias

```bash
npm install
```

### Paso 3: Configurar Variables de Entorno (Opcional)

Para desarrollo local, las variables de entorno son opcionales ya que el frontend usa `http://localhost:4005` por defecto para conectarse al backend.

Si necesitas configurar una URL diferente del backend, crea un archivo `.env.local` en la carpeta `Frontend/`:

```env
VITE_API_BASE_URL=http://localhost:4005
```

### Paso 4: Iniciar el Servidor de Desarrollo

```bash
npm run dev
```

El frontend estará disponible en: `http://localhost:5173`

**Nota:** Asegúrate de que el backend esté corriendo en `http://localhost:4005` o configura `VITE_API_BASE_URL` con la URL correcta.

## Estructura del Proyecto

```
Frontend/
├── src/
│   ├── components/          # Componentes reutilizables
│   │   ├── admin/           # Componentes del panel de administración
│   │   │   ├── CategoryManager.vue
│   │   │   ├── OrderDetailsModal.vue
│   │   │   ├── OrderFilters.vue
│   │   │   ├── OrderTable.vue
│   │   │   ├── ProductForm.vue
│   │   │   ├── ProductTable.vue
│   │   │   └── ...
│   │   ├── AuthModal.vue    # Modal de autenticación
│   │   ├── CartSidebar.vue  # Sidebar del carrito
│   │   ├── Footer.vue       # Pie de página
│   │   ├── Header.vue       # Barra de navegación
│   │   ├── ProductCard.vue  # Tarjeta de producto
│   │   └── ...
│   ├── views/               # Vistas/páginas principales
│   │   ├── Home.vue         # Página de inicio
│   │   ├── Shop.vue         # Catálogo de productos
│   │   ├── ProductDetail.vue # Detalle de producto
│   │   ├── Cart.vue         # Página del carrito
│   │   ├── Checkout.vue     # Proceso de pago
│   │   ├── Profile.vue       # Perfil de usuario
│   │   ├── UserOrders.vue   # Órdenes del usuario
│   │   ├── AdminDashboard.vue # Panel de administración
│   │   ├── AdminProducts.vue  # Gestión de productos
│   │   ├── AdminOrders.vue    # Gestión de órdenes
│   │   └── ...
│   ├── stores/              # Stores de Pinia
│   │   ├── auth.js          # Estado de autenticación
│   │   ├── cart.js          # Estado del carrito
│   │   ├── notifications.js # Sistema de notificaciones
│   │   └── routes.js        # Rutas protegidas
│   ├── services/            # Servicios API
│   │   ├── api.js           # Cliente HTTP principal
│   │   └── transbank.js     # Integración Transbank
│   ├── router/              # Configuración de rutas
│   │   └── index.js         # Definición de rutas Vue Router
│   ├── composables/         # Composables reutilizables
│   │   └── useNotifications.js
│   ├── utils/               # Utilidades
│   │   ├── formatters.js    # Formateo de datos
│   │   ├── logger.js        # Sistema de logging
│   │   └── preloader.js     # Preloader
│   ├── assets/              # Recursos estáticos
│   │   └── styles/          # Estilos globales
│   │       ├── colors.css
│   │       ├── variables.css
│   │       └── ...
│   ├── plugins/             # Plugins de Vue
│   │   └── fontawesome.js   # Iconos FontAwesome
│   ├── App.vue              # Componente raíz
│   └── main.js              # Punto de entrada
├── public/                  # Archivos públicos
│   └── favicon.ico
├── index.html               # HTML principal
├── vite.config.js           # Configuración de Vite
├── vercel.json              # Configuración de Vercel
└── package.json             # Dependencias y scripts
```

## Funcionalidades Principales

### Para Usuarios

- **Navegación**: Explorar catálogo de productos con búsqueda y filtros
- **Carrito de Compras**: Agregar, actualizar y eliminar productos
- **Autenticación**: Registro, login y gestión de perfil
- **Órdenes**: Crear órdenes, ver historial y cancelar pedidos pendientes
- **Pagos**: Proceso de checkout con integración Transbank
- **Perfil**: Actualizar información personal y dirección de envío

### Para Administradores

- **Dashboard**: Estadísticas en tiempo real (ventas, productos, usuarios)
- **Gestión de Productos**: Crear, editar, eliminar productos con imágenes
- **Gestión de Órdenes**: Ver todas las órdenes, actualizar estados
- **Control de Stock**: Gestionar inventario de productos
- **Estadísticas**: Reportes de ventas y análisis

## Scripts Disponibles

- `npm run dev` - Inicia el servidor de desarrollo con HMR
- `npm run build` - Construye la aplicación para producción
- `npm run preview` - Preview de la build de producción localmente
- `npm test` - Ejecuta tests unitarios

## Despliegue en Vercel

### Paso 1: Conectar con Vercel

1. Ve a [Vercel](https://vercel.com/)
2. Inicia sesión con tu cuenta de GitHub/GitLab/Bitbucket
3. Haz clic en "Add New Project"
4. Selecciona tu repositorio
5. Configura el proyecto:
   - **Framework Preset**: Vite
   - **Root Directory**: `Frontend`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
   - **Install Command**: `npm install`

### Paso 2: Configurar Variables de Entorno

Ve a **Settings → Environment Variables** y agrega:

```env
VITE_API_BASE_URL=https://tu-backend.vercel.app
```

**Importante:** Reemplaza `https://tu-backend.vercel.app` con la URL real de tu backend desplegado en Vercel.

### Paso 3: Verificar el Despliegue

Una vez desplegado, visita la URL proporcionada por Vercel. Deberías ver la aplicación funcionando correctamente.

**Verificaciones:**
1. La página de inicio carga correctamente
2. Los productos se muestran desde el backend
3. El login y registro funcionan
4. El carrito persiste entre sesiones

## Personalización

### Colores y Estilos

Los estilos principales se encuentran en:
- `src/assets/styles/colors.css` - Paleta de colores
- `src/assets/styles/variables.css` - Variables CSS
- `src/App.vue` - Estilos globales

### Contenido

El contenido principal se encuentra en:
- `src/components/Header.vue` - Navegación y logo
- `src/components/Footer.vue` - Información de contacto y enlaces
- `src/views/Home.vue` - Página principal con información de servicios
- `src/views/Shop.vue` - Catálogo de productos

### Configuración de la API

La URL base del backend se configura mediante:
- Variable de entorno `VITE_API_BASE_URL` (producción)
- Valor por defecto: `http://localhost:4005` (desarrollo)

El cliente HTTP está configurado en `src/services/api.js`.

## Rutas Protegidas

El sistema incluye protección de rutas basada en roles:

- **Rutas públicas**: Home, Shop, ProductDetail, Contact
- **Rutas de usuario**: Cart, Checkout, Profile, UserOrders
- **Rutas de administrador**: AdminDashboard, AdminProducts, AdminOrders, AdminUsers

Las rutas protegidas redirigen automáticamente al login si el usuario no está autenticado.

## Responsive Design

La aplicación está completamente optimizada para:

- **Móviles**: 320px - 768px
- **Tablets**: 768px - 1024px
- **Desktop**: 1024px+

El diseño se adapta automáticamente usando CSS Grid, Flexbox y media queries.

## Testing

Para ejecutar los tests:

```bash
npm test
```

Los tests están configurados con Vitest y cubren los servicios principales de la aplicación.

## Solución de Problemas

### El frontend no se conecta al backend

**Solución:**
- Verifica que el backend esté corriendo en `http://localhost:4005`
- Verifica que `VITE_API_BASE_URL` esté configurada correctamente
- Revisa la consola del navegador (F12) para ver errores específicos
- Verifica que CORS esté configurado correctamente en el backend

### Error al hacer build

**Solución:**
- Verifica que todas las dependencias estén instaladas: `npm install`
- Revisa los errores en la consola durante el build
- Asegúrate de que todas las importaciones sean correctas

### Las imágenes no se cargan

**Solución:**
- Verifica que las rutas de las imágenes sean correctas
- Asegúrate de que las imágenes estén en la carpeta `public/` o se importen correctamente
- Verifica que el backend esté sirviendo las imágenes correctamente

### Problemas con el carrito

**Solución:**
- Verifica que el usuario esté autenticado
- Revisa la consola del navegador para errores de API
- Verifica que el token JWT sea válido
- Limpia el localStorage y vuelve a iniciar sesión

## Tecnologías Utilizadas

- **[Vue.js 3](https://vuejs.org/)** - Framework JavaScript progresivo
- **[Vite](https://vitejs.dev/)** - Build tool y dev server ultrarrápido
- **[Vue Router](https://router.vuejs.org/)** - Router oficial para Vue.js
- **[Pinia](https://pinia.vuejs.org/)** - Store para gestión de estado
- **[Axios](https://axios-http.com/)** - Cliente HTTP para peticiones API
- **[FontAwesome](https://fontawesome.com/)** - Iconos vectoriales
- **[VueUse](https://vueuse.org/)** - Colección de composables utilitarios

## Recursos Adicionales

### Documentación

- [Vue.js Documentation](https://vuejs.org/guide/)
- [Vite Documentation](https://vitejs.dev/guide/)
- [Vue Router Documentation](https://router.vuejs.org/)
- [Pinia Documentation](https://pinia.vuejs.org/)
- [Vercel Documentation](https://vercel.com/docs)

### Soporte

Si encuentras problemas que no están cubiertos en este README:

1. Revisa los logs en Vercel (si está desplegado)
2. Revisa la consola del navegador (F12)
3. Consulta el `MANUAL_INSTALACION.txt` en la raíz del proyecto
4. Verifica que el backend esté funcionando correctamente
5. Revisa la documentación de Swagger del backend en `/api-docs`

---

**Silverthorne Holdings** - Servicios e Insumos Informáticos de calidad
