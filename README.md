Aquí tienes una versión mejorada y estructurada de lo que mencionaste, adaptada para el archivo `README.md`:

---

# Agradecimiento

Primero que nada, quiero agradecer por todo este proceso de selección. Fue un desafío muy interesante y enriquecedor, que aumentó aún más mis ganas de seguir trabajando con ustedes.  
Si tienen cualquier consulta, no duden en enviarme un mail a [leotarditi@gmail.com](mailto:leotarditi@gmail.com).

---

# Decisiones tomadas

1. **Mock de API**  
   Inicialmente intenté usar Google Sheets como mock API debido a su facilidad de implementación y porque no requiere instrucciones adicionales para los evaluadores. Sin embargo, al final opté por utilizar las API Routes de Next.js para cumplir con los requisitos.

2. **Diseño**  
   Decidí truncar el título en una sola línea y la descripción en dos líneas para mantener una apariencia compacta y consistente en el diseño. Si el usuario desea más información, puede hacer clic en el botón "Ver más" o directamente en la imagen del producto.

3. **Manejo de errores**

   - Usé `not-found.tsx` para manejar errores 404, mostrando un mensaje claro cuando el producto no se encuentra.
   - Usé `global-error.tsx` para manejar errores 500, mostrando un mensaje adecuado si hay problemas en el servidor.

4. **Optimización de imágenes**  
   Convertí todas las imágenes a formato `webp` para reducir su tamaño y mejorar el rendimiento de la aplicación.

5. **Scroll infinito y búsqueda**

   - Implementé la funcionalidad de scroll infinito evaluando librerías como React Query y SWR, además de intentar soluciones nativas de React (`useEffect` y `useState`). Aunque logré una implementación funcional con React, me faltó tiempo para optimizar completamente el comportamiento en Next.js.
   - Implementé la búsqueda con debounce de 500ms, cargando datos de manera eficiente desde el servidor.

6. **Testing y Storybook**

   - Logré integrar Storybook con un componente de botón básico. Por cuestiones de tiempo, no pude extender la cobertura a otros componentes como el SearchBox.
   - Planeé realizar más pruebas unitarias e integrales, pero prioricé la funcionalidad básica del proyecto debido a limitaciones de tiempo.

7. **Arquitectura del proyecto**

   - Usé principios de Clean Architecture y Screaming Architecture para organizar el código.
   - Documenté el proceso de desarrollo a través de commits bien estructurados.

8. **Gestión de paquetes**  
   Decidí utilizar Bun como administrador de paquetes en lugar de PNPM, considerando su rendimiento y simplicidad.

---

# Descripción del desafío

## Objetivo: Desarrollo de una aplicación web para listado y detalle de productos.

### Requerimientos técnicos

- **Framework:** Next.js (usando App Router para la navegación).
- **Estilos:** TailwindCSS.
- **Lenguaje:** TypeScript.
- **Fetching:** Prioridad a SSR según consideración del desarrollador.
- **Mock API:** Se recomienda JSON Server, aunque se permite el uso de otras soluciones.

### Páginas implementadas

1. **Página de Listado de Productos (PLP)**

   - Ruta raíz: `/`.
   - Funcionalidades:
     - Búsqueda por SKU o nombre (con debounce de 500ms).
     - Scroll infinito para la paginación (opcional con React Query).
     - Loader durante el procesamiento de la búsqueda.
     - Redirección a la página de detalle al hacer clic en "Ver Detalle".

2. **Página de Detalle de Producto (PDP)**
   - Ruta: `/products/:sku`.
   - Funcionalidades:
     - Mostrar información del producto (nombre, SKU, foto, categoría, marca, precio y especificaciones).
     - Manejo de errores 404 y 500 con mensajes personalizados.

---

# Instrucciones

### Clonar el proyecto

```bash
git clone https://github.com/leotarditi/nombre-del-repositorio.git
cd nombre-del-repositorio
```

### Instalar dependencias

Con Bun:

```bash
bun install
```

Con PNPM (opcional):

```bash
pnpm install
```

### Correr el servidor de desarrollo

```bash
bun dev
```

### Correr Storybook

```bash
bun storybook
```
