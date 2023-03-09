# **Projet_Data_Zaoioui**
Pour réaliser le projet d'analyse de l'indice boursier CAC40, analyse et prévision du prix de l'action MC.PA, j'ai passé par plusieurs étapes :
## Etape 1 : Web Scraping des données
J'ai utilisé les données de l'indice boursier cac40 qui existent dans le site internet wikipedia, ensuite avec les Tickers des entreprises j'ai téléchargé les données de la capitalisation boursière des entreprises composantes du CAC40 à l'aide de la méthode get_quote_yahoo de la bibliothèque yfinance.
## Etape 2 : Analyse des données du CAC40
J'ai créé une dataframe à partir de ces données pour chercher le secteur le plus important dans le CAC40 et l'entreprise qui représente la plus grande capitalisation, ensuite j'ai analysé ces données à l'aide de la bibliothèque Pandas.
## Etape 3 : Analyse et prévision des données de l'action MC.PA
Après avoir déterminé le secteur le plus important dans le CAC40 et l'entreprise avec la plus grande capitalisation boursière, j'ai commencé l'analyse et la prévision de la série temporelle de l'action MC.PA de la Société Louis Vuitton.
Le nettoyage et l'analyse des données à été effectué avec la bibliothèque pandas, ensuite j'ai effectué la prévision du prix typique de l'action MC.PA (la moyenne arithmétique des prix haut, bas et de clôture pour une période donnée) avec la bibliothèque Prophet de Python.
Pour réaliser la prévision j'ai d’abord défini et configuré un objet Prophet(), puis je les ajusté sur l’ensemble de données avec la fonction fit() et en lui transmettant les données, et j'ai utilisé ensuite make_future_dataframe afin de spécifier la période de prévision.

## Etape 4 : Calcule de l'erreur de prévision
Pour réaliser un projet complet de prévision il faut absolument calculer les erreurs liées à la prévision.
Avec la méthode de la validation croisée j'ai pu générer plusieurs types d'erreurs dont le plus important est le RMSE (erreur quadratique moyenne), c'est l'écart-type des résidus de prévision (les écarts entre les valeurs prédites et les valeurs observées).
