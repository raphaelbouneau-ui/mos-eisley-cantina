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

## Exercice GitHub flow — navigation fixe

### Prompt 1 — Simplifier la navigation

Dans cette navigation, conserve la marque Mos Eisley Cantina et uniquement les liens Features et Live music, avec leurs href actuels. Conserve les styles et le focus clavier. Utilise uniquement HTML et les classes Tailwind, sans ajouter de JavaScript. Ne modifie pas le reste de la page.

Résultat : conservation des liens Features et Live music. Après une annulation qui avait rétabli les anciens liens, suppression manuelle de Menu, Sign in et Reserve dans la navigation.

### Prompt 2 — Ajouter la section musicale

Juste avant </main>, ajoute une section id="live-music" avec aria-labelledby="live-music-title", un h2 id="live-music-title" et un court paragraphe en anglais sur Figrin D’an & the Modal Nodes. Utilise uniquement HTML et Tailwind, avec des styles cohérents avec Features. Ne modifie rien d’autre.

Résultat : ajout de la section Live music après Features, à l’intérieur de main. Une première insertion incorrecte dans le header avait été annulée.

### Modifications manuelles

- Ajout de scroll-smooth et motion-reduce:scroll-auto sur html pour un défilement doux respectant la préférence de réduction des animations.
- Ajout de scroll-mt-32 aux sections Features et Live music pour tenir compte de la navigation fixe.
- Correction après relecture de la pull request : conservation de py-16 avec scroll-mt-32 sur Live music.

### Vérifications

Les liens conduisent aux ancres #features et #live-music. La navigation reste visible pendant le défilement et les titres des sections sont visibles dans le navigateur.

### Limite connue

Le bouton Reserve a booth du contenu principal pointe encore vers une section absente, hors du périmètre de cette modification.