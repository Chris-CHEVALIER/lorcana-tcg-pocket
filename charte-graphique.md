# Charte graphique — Lorcana Pocket

Inspirée de l'identité visuelle officielle de Disney Lorcana (disneylorcana.com), adaptée pour une app mobile fan-made. Thème clair uniquement, comme validé.

⚠️ **Limite légale** : on s'inspire de l'esprit (couleurs d'ink, ambiance fantasy/conte) sans reproduire le logo officiel, le lettrage sur-mesure du titre "Lorcana" (propriété Ravensburger/Disney, dessiné par un studio de lettrage dédié) ni les illustrations de cartes. Nos écrans utilisent un logo et une typographie inspirés mais originaux.

---

## 1. Couleurs

### Couleur de marque
| Usage | Couleur | Hex |
|---|---|---|
| Marine profond (bandeaux, fonds immersifs, texte sur clair) | Navy Lorcana | `#131A24` |
| Marine clair (variante hover/secondaire) | Navy clair | `#1F2A3D` |

*Le `#131A24` est la couleur de thème utilisée par le site officiel disneylorcana.com — on la reprend comme ancrage de marque neutre, plutôt que le violet qu'on avait utilisé jusqu'ici dans les wireframes.*

### Couleurs d'ink (les 6 familles de cartes)
Référence communautaire (aucune charte hex officielle publiée par Ravensburger) :

| Ink | Hex | Usage dans l'app |
|---|---|---|
| Amber | `#F5B202` | Fond de carte, badges, filtres |
| Amethyst | `#81377B` | idem |
| Emerald | `#2A8934` | idem |
| Ruby | `#D3082F` | idem |
| Sapphire | `#0189C4` | idem |
| Steel | `#9FA8B4` | idem |

Pour chaque ink, prévoir une variante foncée (texte sur fond clair de cette couleur) et une variante claire (fond de badge/chip) — à générer en assombrissant/éclaircissant de ~30 %.

### Neutres et fonds (thème clair)
| Usage | Hex |
|---|---|
| Fond principal de l'app | `#F5F4F0` |
| Fond de carte/surface | `#FFFFFF` |
| Bordure discrète | `#E4E2DA` |
| Texte principal | `#131A24` |
| Texte secondaire | `#5F5E5A` |
| Texte désactivé/placeholder | `#B4B2A9` |

### Couleurs sémantiques
| Usage | Hex |
|---|---|
| Succès (carte obtenue, validation) | `#2A8934` (réutilise Emerald) |
| Alerte/nouveauté (badge "Nouvelle") | `#D3082F` (réutilise Ruby) |
| Info | `#0189C4` (réutilise Sapphire) |

---

## 2. Typographie

### Police d'affichage (titres, logo, en-têtes de section)
Style **fantasy/conte élégant**, en écho à l'esprit du lettrage officiel (serifs classiques, légèrement ornemental) sans le copier :
- **Choix recommandé** : `Cinzel` (Google Fonts) pour les titres marquants (écran de démarrage, noms d'extension), ou `Playfair Display` pour un rendu un peu plus doux/lisible.
- Usage : logo de l'app, titres d'écran type "The First Chapter", noms de cartes en grand format.

### Police fonctionnelle (UI, texte courant)
Neutre et très lisible, pour tout le reste (boutons, labels, texte de carte, navigation) :
- **Choix recommandé** : `Inter` (Google Fonts, gratuite, excellent support RN) ou la police système (San Francisco / Roboto) pour un rendu natif.

### Échelle typographique
| Style | Taille | Poids | Police |
|---|---|---|---|
| Logo / titre démarrage | 32–40px | Regular/Medium | Display |
| Titre d'écran (h1) | 22px | Medium | Display ou fonctionnelle |
| Titre de section (h2) | 17px | Medium | Fonctionnelle |
| Corps de texte | 14–15px | Regular | Fonctionnelle |
| Label / caption | 11–12px | Medium | Fonctionnelle |

---

## 3. Iconographie
- Style **outline** (traits fins, cohérent), pas d'icônes "filled" ni de pictos 3D.
- Une icône par ink pour les représenter en attendant les vraies illustrations de cartes (à définir precisément — actuellement placeholders : lune=Amethyst, feuille=Emerald, flamme=Ruby, goutte=Sapphire, soleil=Amber, couronne/bouclier=Steel).

## 4. Rayons et espacement
| Élément | Valeur |
|---|---|
| Cartes (grande taille, détail) | 14px |
| Cases de grille collection | 6px |
| Boutons / chips | 8–12px (pill pour les chips de filtre) |
| Marges d'écran | 14–16px |
| Grille collection (gap) | 2–4px (dense, beaucoup de cartes visibles) |

## 5. Composants clés
- **Bandeau d'en-tête** : fond `#131A24`, texte blanc cassé (`#F5F4F0`), hauteur 48px.
- **Barre de navigation basse** : fond blanc, icône + label actif en Navy, inactifs en gris (`#888780`).
- **Carte de collection** : dégradé de l'ink concernée (clair → foncé), icône centrée, badge quantité en incrustation.
- **Case non obtenue** : fond neutre, bordure pointillée, numéro de carte affiché en gris.
- **Effet foil** (dernière carte du booster) : reflet diagonal animé en boucle, indépendant de la rareté.

## 6. Ton et rédaction (UI en français)
- Phrases courtes, verbes à l'infinitif pour les actions ("Ouvrir le booster", pas "Vous pouvez ouvrir...").
- Pas de points d'exclamation sur les libellés système.
- Tutoiement ou vouvoiement à trancher — recommandation : **tutoiement**, cohérent avec le ton jeune/enthousiaste des TCG mobiles.
