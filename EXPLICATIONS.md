# EXPLICATIONS – FONTAINE Albin

## Branches et commits
| Élément | Branche | Commit | Créée depuis |
|---|---|---|---|
| Départ | main / tag depart-cc | 67aeb4f | – |
| A – thème nocturne | feature/theme-nocturne | 3a5ee63 | 67aeb4f |
| B – confirmation | feature/confirmation-reservations | 7e84bb8 | 67aeb4f |
| Fusion A+B | main | dbbd8f8 | – |
| Hotfix | hotfix/lisibilite-confirmation | dbe2f94 | dbbd8f8 |
| Demande complémentaire | feature/nom-atelier-confirmation | 12126fa | dbe2f94 |

A, le hotfix et la demande complémentaire sont passés en fast-forward. B a eu un commit de fusion (dbbd8f8).

## Avant / après hotfix
- Avant (dbbd8f8) : Page de base, sans modification
- Après (dbe2f94) : Couleurs de la page changées

## Tests (main 12126fa)
| Test | Résultat |
|---|---|
| Ouverture | Compteur 0, confirmation masquée |
| 1 réservation | Compteur 1, confirmation lisible. Texte exact : Réservation confirmée | Places réservées : 1 |
| 3 réservations | Compteur et confirmation à 3 |
| Recommencer | Compteur 0, confirmation masquée |
| Réservation après remise à zéro | Texte remis en invisible ou « non vérifié » |
| 390 px | Lisible, pas de défilement horizontal |

## Réponses
1. **Base et branches** : je suis parti de 67aeb4f (tag depart-cc). A et B viennent de ce commit. Le hotfix part de dbbd8f8, la dernière branche de dbe2f94.
2. **Fusion** : aucun conflit, car A touche style.css et B app.js. Mais la confirmation était invisible : le fond (#17223b) et le bloc .receipt (#17223b) avaient la même couleur. Git ne voit pas ça, seul le navigateur l'a montré. Le hotfix l'a corrigé.