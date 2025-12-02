# Lab-2-Conception-du-sch-ma-et-contraintes-d-int-grit-
       # Étape 1 – Analyse du besoin métier
            Entités et attributs :
    Auteur : nom
    Ouvrage : titre, disponibilité
    Abonné : nom, email
    Emprunt : date_debut, date_fin
    Relations :
    Un auteur peut écrire plusieurs ouvrages
    Un abonné peut faire plusieurs emprunts
    Un emprunt lie un abonné à un ouvrage
    
    # Étape 2 – Normalisation
    
    1NF – Atomicité : toutes les colonnes contiennent des valeurs simples → OK
    2NF – Dépendance complète : pas de clé composée, tous les attributs dépendent entièrement de leur clé → OK
    3NF – Pas de dépendance transitive : aucun attribut non clé ne dépend d’un autre attribut non clé → OK

    # Étape 3 – Modélisation entité–relation (ER)

    Entités et attributs :

      Auteur : nom (PK)
      Ouvrage : titre (PK), disponibilité
      Abonné : nom (PK), email
      Emprunt : date_debut (PK), date_fin (optionnelle), Abonné_ID (FK), Ouvrage_ID (FK)
      Relations :
      Auteur → Ouvrage : 1 à n
      Abonné → Emprunt : 1 à n
      Ouvrage → Emprunt : 1 à n
      date_fin dans Emprunt est optionnelle
      Diagramme ER : utiliser rectangles pour entités, souligner les clés primaires, relier avec traits annotés 1 et n, noter l’optionnalité de date_fin.

    # Étape 5 – Définition des types de données et du moteur

              Moteur : InnoDB
          Types de données :
          Identifiants : INT AUTO_INCREMENT
          Textes courts : VARCHAR(n)
          Booléen : BOOLEAN
          Dates : DATE ou DATETIME

      # Étape 7 – Création de la table ouvrage
      
      <img width="565" height="437" alt="image" src="https://github.com/user-attachments/assets/766cc87e-56b9-4f5c-a0e8-739c331070ab" />

      
      
