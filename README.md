# Financial Econometrics — Swiss Market Index (SMI)

Projet de mi-semestre du cours **M1 Financial Econometrics with Python** (2025-2026).
Analyse empirique de l'indice suisse **SMI (^SSMI)** sur la période 1999–2024, avec des données Yahoo Finance.

📓 **Notebook :** [smi_stylized_facts_capm_ff3.ipynb](smi_stylized_facts_capm_ff3.ipynb) · 📄 **Rapport :** [report.pdf](report.pdf)

## Partie 1 — Faits stylisés des rendements financiers

- Stationnarité des rendements (moyenne et volatilité glissantes, ACF)
- Asymétrie (skewness)
- Queues épaisses (kurtosis, QQ-plots vs loi normale et Student-t)
- Gaussianité agrégée (rendements journaliers / hebdomadaires / mensuels, test de Lilliefors)
- Absence d'autocorrélation des rendements
- Clustering de volatilité (ACF de |r| et r², bandes de Bartlett)
- Effet de levier (corrélation croisée entre rendements et volatilité future)

## Partie 2 — Modèles à facteurs : CAPM vs Fama-French 3 facteurs

- Régression des rendements excédentaires du SMI sur les facteurs *Developed Markets*
- Comparaison de l'ajustement (R² ajusté, RMSE), significativité de l'alpha
- Test de Wald `SMB = HML = 0` et F-test emboîté CAPM vs FF3
- Diagnostics des résidus : Jarque-Bera, Ljung-Box, Breusch-Pagan, White
- Coefficients estimés avec leurs intervalles de confiance à 95 %

## Stack

`pandas` · `numpy` · `yfinance` · `statsmodels` · `scipy` · `scikit-learn` · `matplotlib`

## Auteurs

Loup Kassis · Sohel Hallil · Alexandre Magnan

## Lancer le notebook

```bash
pip install -r requirements.txt
jupyter notebook smi_stylized_facts_capm_ff3.ipynb
```

Les données sont téléchargées automatiquement depuis Yahoo Finance (connexion internet requise).
