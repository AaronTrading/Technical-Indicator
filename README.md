# Indicateur Technique Multi-paramètres

Un indicateur technique avancé pour TradingView qui combine plusieurs indicateurs pour fournir des signaux de trading complets avec gestion du risque ainsi qu'un setup d'entrée avec un TP/SL calculé et un RR de 1.5

## Screens

![Screen1](https://media.discordapp.net/attachments/1280431720679870475/1378146964344012941/image.png?ex=683b8ae1&is=683a3961&hm=82941ed19a5d168e7d7589b6bab2f1258f13103d3bea08a67d922013812f4eb0&=&format=webp&quality=lossless&width=659&height=503)

## Fonctionnalités

### Moyennes Mobiles

- EMA 9 (Exponential Moving Average)
- EMA 21 (Exponential Moving Average)
- EMA 50 (Exponential Moving Average) - Filtre de tendance

### RSI (Relative Strength Index)

- Période: 14
- Signaux:
  - Achat: RSI < 30
  - Vente: RSI > 70
  - Neutre: Entre 30 et 70

### MACD (Moving Average Convergence Divergence)

- Paramètres standards: 12, 26, 9
- Signaux basés sur le croisement des lignes MACD et Signal

### Stochastique

- Période: 14
- Ligne de signal: 3
- Signaux basés sur les croisements et les niveaux 20/80

### Bandes de Bollinger

- Période: 20
- Écart-type: 2
- Signaux basés sur les percées des bandes

### Filtres et Pondération

- Filtre Volume: Compare le volume actuel à sa moyenne mobile sur 20 périodes
- Filtre Tendance: Utilise l'EMA 50 comme filtre de tendance
- Pondération des signaux:
  - EMA Cross: 40%
  - RSI: 15%
  - MACD: 15%
  - Bollinger: 15%
  - Stochastique: 15%

### Gestion du Risque

- Stop Loss (SL): Basé sur l'EMA 21
- Take Profit (TP): Ratio de risque/récompense de 1.5
- Affichage automatique des niveaux SL/TP dans le tableau

### Signal Global

Combine tous les indicateurs avec pondération pour fournir une recommandation globale:

- Achat: Score ≥ 0.3
- Vente: Score ≤ -0.3
- Neutre: Entre -0.3 et 0.3

## Installation

1. Ouvrez TradingView
2. Allez dans l'éditeur Pine Script
3. Copiez-collez le code
4. Cliquez sur "Ajouter au graphique"

## Utilisation

L'indicateur affiche un tableau en haut à droite du graphique avec:

- Les signaux individuels de chaque indicateur
- Le signal global combiné
- Les niveaux de Stop Loss et Take Profit
- Des icônes pour une meilleure lisibilité
- Des flèches miniatures sur le graphique pour les croisements EMA

## Auteur

Aaron Z.

## Licence

MIT
