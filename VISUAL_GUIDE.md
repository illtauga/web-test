# Guía Visual de Diseño - FixItNow

## Paleta de Colores

### Colores Principales
- **Púrpura Oscuro (Dark Purple)**: `#1A1F2C`
  - Uso: Encabezados, texto principal, acentos
- **Púrpura Primario (Primary Purple)**: `#9b87f5`
  - Uso: Botones principales, enlaces, elementos interactivos
- **Ámbar (Amber)**: `#FFB800`
  - Uso: Botones de acción, acentos, elementos destacados
- **Gris Neutral (Neutral Gray)**: `#8E9196`
  - Uso: Texto secundario, bordes, elementos de fondo

### Colores de Fondo
- **Blanco (White)**: `#FFFFFF`
  - Uso: Fondos principales, tarjetas, contenido
- **Gris Claro (Light Gray)**: `#F1F0FB`
  - Uso: Fondos de secciones, elementos de contraste
- **Gris Muy Claro (Very Light Gray)**: `#F8F9FA`
  - Uso: Fondos alternativos, estados hover

## Tipografía

### Fuentes
- **Títulos**: Inter (Bold, 600)
- **Texto**: Inter (Regular, 400)
- **Botones**: Inter (Medium, 500)

### Tamaños de Texto
- **H1**: 3rem (48px)
- **H2**: 2.25rem (36px)
- **H3**: 1.5rem (24px)
- **H4**: 1.25rem (20px)
- **Párrafo**: 1rem (16px)
- **Pequeño**: 0.875rem (14px)

## Espaciado

### Márgenes y Paddings
- **Base**: 1rem (16px)
- **Pequeño**: 0.5rem (8px)
- **Mediano**: 1.5rem (24px)
- **Grande**: 2rem (32px)
- **Extra Grande**: 3rem (48px)

### Grid System
- **Contenedor Máximo**: 1280px (max-w-7xl)
- **Gutter**: 2rem (32px)
- **Columnas**: 12 columnas responsivas

## Componentes

### Tarjetas
```css
.card {
  background: white;
  border-radius: 0.5rem;
  box-shadow: 0 1px 3px rgba(0,0,0,0.1);
  transition: all 0.3s ease;
}

.card:hover {
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  transform: translateY(-2px);
}
```

### Botones
```css
.button-primary {
  background: #FFB800;
  color: black;
  padding: 0.75rem 1.5rem;
  border-radius: 0.5rem;
  font-weight: 500;
  transition: all 0.2s ease;
}

.button-primary:hover {
  background: #E6A600;
  transform: translateY(-1px);
}
```

### Formularios
```css
.input {
  border: 1px solid #E2E8F0;
  border-radius: 0.5rem;
  padding: 0.75rem 1rem;
  transition: all 0.2s ease;
}

.input:focus {
  border-color: #9b87f5;
  box-shadow: 0 0 0 3px rgba(155, 135, 245, 0.1);
}
```

## Secciones

### Hero Section
- **Altura Mínima**: 80vh
- **Contenido**: Centrado verticalmente
- **Fondo**: Blanco o imagen con overlay
- **Espaciado**: Padding vertical de 4rem

### Grid de Servicios
- **Columnas**: 3 en desktop, 2 en tablet, 1 en móvil
- **Espaciado**: Gap de 2rem
- **Tarjetas**: Altura uniforme, sombra suave

### Sección de Contacto
- **Fondo**: Gris claro (#F1F0FB)
- **Formulario**: Máximo ancho de 600px
- **Espaciado**: Padding vertical de 4rem

## Animaciones

### Transiciones
- **Duración Base**: 0.2s
- **Easing**: ease-in-out
- **Hover**: transform: translateY(-2px)
- **Focus**: scale(1.02)

### Micro-interacciones
- **Botones**: Elevación al hover
- **Tarjetas**: Elevación y sombra al hover
- **Enlaces**: Cambio de color suave

## Diseño Responsivo

### Breakpoints y Media Queries
```css
/* Tailwind breakpoints */
sm: 640px    /* Pequeños dispositivos móviles */
md: 768px    /* Tablets y móviles grandes */
lg: 1024px   /* Laptops y tablets grandes */
xl: 1280px   /* Desktops */
2xl: 1536px  /* Desktops grandes */
```

### Estrategias de Layout

#### Mobile First
1. **Contenedores**
   - Padding base: `px-4`
   - Padding medio: `sm:px-6`
   - Padding grande: `lg:px-8`
   - Ancho máximo: `max-w-7xl`

2. **Grid System**
   ```css
   /* Mobile */
   grid-cols-1
   
   /* Tablet */
   sm:grid-cols-2
   
   /* Desktop */
   lg:grid-cols-3
   ```

3. **Espaciado Responsivo**
   ```css
   /* Mobile */
   gap-4
   
   /* Tablet y Desktop */
   sm:gap-8
   ```

### Componentes Responsivos

#### Header
```css
/* Mobile */
flex-col
items-center
gap-4

/* Desktop */
sm:flex-row
sm:items-center
sm:justify-between
```

#### Hero Section
```css
/* Mobile */
flex-col
text-center
space-y-4

/* Desktop */
md:flex-row
md:text-left
md:space-y-6
```

#### Tarjetas
```css
/* Mobile */
p-4
text-center

/* Desktop */
sm:p-6
```

### Tipografía Responsiva

#### Títulos
```css
/* Mobile */
text-3xl

/* Tablet */
sm:text-4xl

/* Desktop */
md:text-5xl
lg:text-6xl
```

#### Texto
```css
/* Mobile */
text-base

/* Tablet y Desktop */
sm:text-lg
```

### Imágenes y Media

#### Imágenes Responsivas
```css
/* Contenedor */
relative
w-full
h-auto

/* Imagen */
object-cover
rounded-md
```

#### Overlays y Badges
```css
/* Mobile */
p-3
text-xs

/* Desktop */
sm:p-4
sm:text-sm
```

### Botones y CTA

#### Botones Primarios
```css
/* Mobile */
w-full
text-center

/* Desktop */
sm:w-auto
```

#### Grupos de Botones
```css
/* Mobile */
flex-col
gap-4

/* Desktop */
sm:flex-row
```

### Navegación

#### Menú Principal
```css
/* Mobile */
flex-col
items-center
gap-4

/* Desktop */
sm:flex-row
sm:items-center
sm:gap-8
```

#### Enlaces
```css
/* Mobile */
text-center
block

/* Desktop */
sm:text-left
sm:inline
```

### Mejores Prácticas

1. **Contenedores**
   - Usar `max-w-7xl` para limitar el ancho máximo
   - Implementar padding responsivo
   - Mantener márgenes consistentes

2. **Grids**
   - Empezar con una columna en móvil
   - Aumentar columnas gradualmente
   - Usar `gap` responsivo

3. **Tipografía**
   - Reducir tamaños en móvil
   - Aumentar progresivamente
   - Mantener proporciones

4. **Espaciado**
   - Usar unidades relativas
   - Implementar espaciado responsivo
   - Mantener consistencia

5. **Imágenes**
   - Optimizar para móvil
   - Usar `object-fit`
   - Implementar lazy loading

6. **Componentes**
   - Diseñar mobile-first
   - Usar flexbox para alineación
   - Implementar breakpoints progresivos

### Checklist de Responsive

- [ ] Verificar breakpoints
- [ ] Comprobar contenedores
- [ ] Revisar tipografía
- [ ] Validar imágenes
- [ ] Probar navegación
- [ ] Verificar formularios
- [ ] Comprobar botones
- [ ] Validar espaciado
- [ ] Probar en diferentes dispositivos

### Herramientas de Testing

1. **DevTools**
   - Modo dispositivo
   - Emulación de red
   - Throttling de CPU

2. **Dispositivos Físicos**
   - Smartphones
   - Tablets
   - Laptops
   - Monitores grandes

3. **Servicios Online**
   - BrowserStack
   - Responsive Design Checker
   - Google Mobile-Friendly Test

### Optimización de Performance

1. **Imágenes**
   - Usar formatos modernos (WebP)
   - Implementar lazy loading
   - Optimizar tamaños

2. **CSS**
   - Minimizar media queries
   - Usar variables CSS
   - Implementar purge

3. **JavaScript**
   - Lazy loading de componentes
   - Code splitting
   - Optimización de bundles

### Accesibilidad en Móvil

1. **Touch Targets**
   - Mínimo 44x44px
   - Espaciado adecuado
   - Feedback visual

2. **Contraste**
   - Mantener ratios
   - Usar colores accesibles
   - Verificar en diferentes fondos

3. **Navegación**
   - Menú accesible
   - Skip links
   - Focus management

## Accesibilidad

### Contraste
- **Texto sobre fondo claro**: Mínimo 4.5:1
- **Texto sobre fondo oscuro**: Mínimo 7:1
- **Elementos interactivos**: Mínimo 3:1

### Tamaños
- **Botones**: Mínimo 44x44px
- **Enlaces**: Mínimo 16px
- **Espaciado**: Mínimo 8px entre elementos

## Iconografía

### Estilo
- **Línea**: 2px
- **Tamaño**: 24px base
- **Color**: Púrpura oscuro o gris neutral

### Uso
- **Acciones**: Lucide Icons
- **Servicios**: Emojis o iconos personalizados
- **Social**: Iconos de redes sociales

## Imágenes

### Formatos
- **Fotos**: JPG, WebP
- **Iconos**: SVG
- **Logos**: SVG

### Tamaños
- **Hero**: 1920x1080px
- **Tarjetas**: 800x600px
- **Avatares**: 100x100px

## Consistencia Visual

### Reglas Generales
1. Mantener el espaciado consistente
2. Usar la paleta de colores definida
3. Seguir la jerarquía tipográfica
4. Aplicar animaciones sutiles
5. Mantener el diseño limpio y minimalista

### Checklist de Implementación
- [ ] Verificar colores de la paleta
- [ ] Aplicar espaciado consistente
- [ ] Usar tipografía correcta
- [ ] Implementar animaciones
- [ ] Verificar responsive
- [ ] Comprobar accesibilidad 