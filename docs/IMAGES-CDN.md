# 📸 Images CDN - Références Unsplash

## Liste complète des images utilisées

### Hero Section
- **URL** : https://images.unsplash.com/photo-1559839734-2b71ea197ec2
- **Description** : Portrait cardiologue femme professionnelle, blouse blanche, stéthoscope
- **Photographe** : Unsplash (licence libre)
- **Utilisation** : Image principale du docteur dans la section hero
- **Dimensions** : 1920x1080 (desktop), 768x1024 (mobile)
- **Optimisation** : WebP, qualité 85%, recadrage intelligent

### Section À Propos
- **URL** : https://images.unsplash.com/photo-1594824476967-48c8b964273f
- **Description** : Médecin dans cabinet moderne, portrait professionnel
- **Photographe** : Unsplash (licence libre)
- **Utilisation** : Photo de profil du docteur
- **Dimensions** : 600x600
- **Optimisation** : WebP, qualité 85%, format carré

## Icônes Iconify utilisées

### Section Services
- **healthicons:stethoscope** - Consultation cardiologique (bleu #4A90E2)
- **healthicons:ecg** - Électrocardiogramme (vert menthe #7ED7C1)
- **healthicons:ultrasound** - Échocardiographie (pêche #FFE4D6)
- **healthicons:heart-organ** - Suivi thérapeutique (jaune doux #FFD89B)

### Section Réassurance
- **mdi:ear-hearing** - Écoute personnalisée (bleu #4A90E2)
- **mdi:shield-check** - Équipement moderne (vert menthe #7ED7C1)
- **mdi:clock-outline** - Disponibilité (pêche #FFE4D6)
- **mdi:map-marker** - Localisation pratique (jaune doux #FFD89B)

## Optimisations appliquées

### Paramètres Unsplash
- `&auto=format` : Format optimal (WebP si supporté)
- `&fit=crop` : Recadrage intelligent
- `&q=85` : Qualité optimale (80-90 recommandé)
- `&w={largeur}&h={hauteur}` : Dimensions exactes

### Attributs HTML
- `loading="lazy"` : Chargement différé (sauf hero: `loading="eager"`)
- `decoding="async"` : Décodage asynchrone
- `width` et `height` : Dimensions explicites pour éviter le CLS
- `onerror` : Fallback SVG en cas d'erreur de chargement

### Fallbacks SVG
En cas d'erreur de chargement, les images sont remplacées par des SVG avec :
- Fond coloré selon la palette du site
- Texte de remplacement
- Dimensions identiques à l'image originale

## Remplacement futur

Pour remplacer par les vraies photos du shooting :

1. **Uploadez les photos** sur un hébergeur (Cloudinary, ImageKit, etc.)
2. **Remplacez les URLs** Unsplash par les nouvelles URLs
3. **Conservez les paramètres** d'optimisation (?w=X&h=Y&q=85)
4. **Testez les fallbacks** SVG

### Exemple de remplacement
```html
<!-- Avant -->
src="https://images.unsplash.com/photo-1559839734-2b71ea197ec2?w=1920&h=1080&fit=crop&q=85"

<!-- Après -->
src="https://votre-cdn.com/docteur-photo.jpg?w=1920&h=1080&fit=crop&q=85"
```

## Performance

### Avantages CDN
- ✅ **Aucun téléchargement** nécessaire
- ✅ **Images HD** chargées via CDN Unsplash
- ✅ **Optimisation automatique** (WebP, compression)
- ✅ **Performance maximale** (lazy loading)
- ✅ **Zéro coût**, zéro limite de bande passante

### Métriques attendues
- **LCP** : < 2.5s (image hero chargée en priorité)
- **CLS** : < 0.1 (dimensions explicites)
- **FID** : < 100ms (lazy loading)

## Crédits

- **Images** : Unsplash (https://unsplash.com/license)
- **Icônes** : Iconify (https://iconify.design/)
- **Licence** : Gratuit pour usage commercial, attribution non requise

## Maintenance

### Vérifications régulières
1. **Testez les URLs** Unsplash (rare mais possible)
2. **Vérifiez les fallbacks** SVG
3. **Contrôlez les performances** (Lighthouse)
4. **Mettez à jour** les images si nécessaire

### Alternatives CDN
Si Unsplash devient indisponible :
- **Picsum** : https://picsum.photos/
- **Lorem Picsum** : https://picsum.photos/id/{ID}/
- **Placeholder.com** : https://via.placeholder.com/

---

*Documentation mise à jour le : [Date actuelle]*
*Version du site : 1.0*
