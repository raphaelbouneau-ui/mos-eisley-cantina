# Prompt utilisé avec Cursor (⌘K)

Modifie uniquement la section HTML sélectionnée. Le projet utilise HTML et Tailwind CSS via le Play CDN, sans fichier CSS ni JavaScript supplémentaire.

Crée une section features sous le héros. Conserve id="features" et aria-labelledby="features-title". Ajoute un petit surtitre "What you find inside", un h2 avec id="features-title" et le texte "A booth for every kind of trouble", puis une courte introduction.

Crée une grille gap-6 avec une colonne sur mobile et trois colonnes à partir de md. Utilise un <article> par carte, contenant une boîte d’icône, un <h3> et un paragraphe. Garde la palette sombre du héros : cartes légèrement translucides, bordure blanche discrète, coins arrondis et léger effet au survol.

Utilise exactement ces titres et textes :
1. Live music nightly. — Sunset to sunrise, loud enough to drown out a bounty hunter.
2. Smugglers welcome. — No questions asked. Back booths, no records kept.
3. Droids: see house policy. — Limits on the floor. Power-down recommended.

Si tu ajoutes des liens, donne-leur un focus-visible clairement visible. Ne modifie ni le header ni le héros.

# Corrections faites après la génération

- Ajout de `hover:-translate-y-1` aux trois cartes pour obtenir le mouvement demandé au survol.
- Agrandissement des trois boîtes d’icône avec `size-12`, ajout de `rounded-xl` et d’un contour `ring-1`.
- Suppression des classes répétées sur la deuxième carte.

La navigation affiche désormais uniquement les liens Features et Live music. Une section Live music a été ajoutée après Features pour donner une cible au lien correspondant. Le défilement doux respecte la préférence de réduction des animations. La première insertion de la section dans le header a été annulée, puis corrige

Ajout manuel de la classe Tailwind scroll-mt-32 aux sections Features et Live music afin de réserver une marge sous la navigation fixe lors des déplacements par liens d’ancrage. Vérification dans le navigateur : les deux liens ciblent les bonnes sections et les titres sont visibles.