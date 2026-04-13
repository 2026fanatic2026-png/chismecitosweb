# Chismecitos Web 🗨️

Versión web de Chismecitos - La red social anónima para chismes y gossip.

## Características

✅ Misma funcionalidad que la app mobile
✅ Sin Capacitor - Código HTML/JS puro
✅ Diseño responsive para web
✅ AdMob integrado para monetización
✅ Supabase como backend
✅ Deploy gratis en Vercel

## Setup

### 1. Clonar el repo (si usás GitHub)
```bash
git clone <tu-repo>
cd chismecitos-web
```

### 2. Crear un proyecto en Vercel

**Opción A - Vía CLI (recomendado)**
```bash
npm install -g vercel
vercel login
vercel
```

**Opción B - Vía Web**
1. Ir a https://vercel.com
2. Sign up con GitHub / Google
3. Crear nuevo proyecto
4. Seleccionar este repo

### 3. Archivos necesarios

Tu proyecto debe tener:
```
├── index.html          (el archivo principal)
├── vercel.json         (config para Vercel)
└── README.md           (este archivo)
```

### 4. Configuración de Supabase

Las credenciales de Supabase **ya están en el `index.html`**:
- URL: `https://guunbgwzfpeilkybjnun.supabase.co`
- Anon Key: (incluida en el código)

**⚠️ IMPORTANTE**: Si querés cambiar credenciales, edita directamente en `index.html` líneas ~387-388.

### 5. AdMob

El código usa el tu App ID de AdMob:
- **Publisher ID**: `ca-pub-3371788247358319`
- **Ad Unit ID**: `1580403146`

Para cambiar:
1. Vé a https://admob.google.com
2. Crea un nuevo App ID para web
3. Reemplaza el valor en línea ~14 del HTML:
```html
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-XXXXXXXXXXXXXXXX"
```

## Deploy en Vercel

### Opción 1: Command Line
```bash
vercel
```

### Opción 2: Via Git
- Push a GitHub
- Vercel auto-detecta cambios y redeploy

### Opción 3: Drag & Drop
1. Ir a https://vercel.com
2. Arrastrar la carpeta del proyecto

## URL después del deploy

Tu sitio estará en: `https://chismecitos-web.vercel.app` (o tu dominio personalizado)

## Customización

### Cambiar dominio
1. En Vercel Dashboard → Settings → Domains
2. Agregar dominio personalizado

### Cambiar tema
Editar las variables CSS en el `<style>` del HTML (línea ~14 en adelante).

### Cambiar texto
Buscar en el HTML:
- "CHISMECITOS" → tu nombre
- "Contalo sin miedo" → tu lema
- Los emojis por otros

## Monetización con AdMob

El banner aparece **automáticamente** en web. Para optimizar:

1. **Fill Rate**: Usa mediation con otras redes (Meta, AppLovin)
2. **CTR**: Coloca ads en lugares visibles
3. **CPM**: LATAM tiene CPM bajo, asegúrate de tener volumen

💡 **Tip**: Combina web + app = 2x ingresos AdMob

## Troubleshooting

### "Ads no aparecen"
- Verifica que el Publisher ID sea correcto
- Supabase debe estar accesible
- Verifica que no haya errors en console (F12)

### "Posts no cargan"
- Verifica conexión a Supabase
- Abre DevTools (F12) → Console
- Busca errores de CORS o auth

### "Splash screen no desaparece"
- Acepta los términos en el modal
- Limpia localStorage: `localStorage.clear()` en console

## Support

Si algo falla:
1. Abre DevTools (F12)
2. Ve a Console
3. Copia el error
4. Contacta soporte

## License

Creado por Polo con ❤️
