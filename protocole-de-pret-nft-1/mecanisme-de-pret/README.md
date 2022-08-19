# Mécanisme de prêt

### Impression d’actifs

Soup Finance akan memberi ruang finansial yang baru bagi pemilik NFT. Setiap NFT yang didepositkan akan disimpan didalam kontrak eskrow menggunakan tanda tangan digital yang tertruktur dan akan mencetak sebuah token FRC758 ('nToken'). Pengguna akan menerima nToken yang mencerminkan suatu koleksi NFT dan dapat mengubahnya kembali menjadi NFT yang asli dengan melakukan burn pada nToken tersebut.

### nTokens

Les nTokens ne sont pas des jetons à rendement mais seront par la suite facilement composables et compatibles avec notre protocole de prêt. Les utilisateurs pourront utiliser le prix plancher de leurs nTokens comme garantie pour les prêts.

**Par exemple :**

1. Alice possède un NFT Meebit.
2. Alice dépose le NFT Meebit dans nos contrats qui le bloque afin de frapper/créer le jeton nMeebit.
3. Alice peut fournir un jeton nMeebit en garantie dans notre pool de prêt.
4. Alice peut donc emprunter $FSN, $SOL, $ETH etc.

### L’oracle

Nous utiliserons différents oracles de prix NFT qui sont soutenus par certaines des places de marchés NFT les plus réputées afin connaitre leur prix.

### LTV (Ratio prêt/valeur)

Les nTokens auront un ratio de garantie ajustable basé sur la volatilité et la liquidité des collections NFT. Compte tenu de la faible liquidité, les paramètres fixés seront un LTV ouvert de 30 % et un seuil de liquidation de 50 % pour s'assurer qu'un glissement élevé n'a pas d'impact sur la santé globale du pool.

### Liquidation

Les emprunteurs doivent rester en dessous du seuil de liquidation de la garantie fournie, sinon ils subiront la liquidation. Nous calculons ce seuil de liquidation sur la base de la moyenne pondérée de tous les actifs déposés. Lorsqu'un "nToken" est liquidé, son NFT est mis aux enchères.
