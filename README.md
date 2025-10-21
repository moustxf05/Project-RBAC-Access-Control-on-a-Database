# SAE 2.08 : Sécurité des Données et Implémentation RBAC
Ce projet a été réalisé dans le cadre de la SAE 2.08. Il porte sur la sécurisation et la gestion des accès aux données sensibles d'une base de données hospitalière.

Objectif du Projet
L'objectif principal était de mettre en place une politique de sécurité basée sur les rôles (RBAC - Role-Based Access Control). L'enjeu était de gérer efficacement les droits et responsabilités des différents corps de métier au sein d'un hôpital (médecins, secrétaires, administrateurs) pour garantir la confidentialité et l'intégrité des données des patients.

Contexte et Démarche
Le point de départ de ce projet fut un script de base de données Oracle existant. Notre première mission a été de migrer cette structure vers PostgreSQL.

Cette migration a nécessité :

L'analyse du script Oracle pour comprendre la structure et les relations.

L'adaptation technique du script aux spécificités de PostgreSQL (ajustement des types de données, modification des noms de tables).

La réorganisation de l'ordre des insertions pour respecter les contraintes d'intégrité (clés étrangères).

Implémentation du RBAC
Une fois la base de données migrée et fonctionnelle, nous avons configuré le système RBAC :

Création des rôles : Définition de rôles distincts (ex: role_medecin, role_secretaire, role_admin) correspondant aux différents métiers de l'hôpital.

Création des utilisateurs : Assignation des utilisateurs fictifs à leurs rôles respectifs.

Gestion des permissions : Attribution de droits granulaires (SELECT, INSERT, UPDATE, DELETE) à chaque rôle, en limitant strictement l'accès aux tables et vues nécessaires à leurs fonctions.

Technologies et Outils
SGBD : PostgreSQL

Administration : PgAdmin 4

Méthodologie : RBAC (Role-Based Access Control)

Langage : SQL (incluant l'adaptation de syntaxes Oracle en PL/pgSQL)

Acquis et Bilan
Ce projet nous a permis de développer plusieurs compétences techniques et méthodologiques :

Migration de SGBD : Nous avons appris à migrer un schéma SQL entre deux systèmes (Oracle vers PostgreSQL), en identifiant et en surmontant les différences syntaxiques et les contraintes propres à chacun.

Sécurité des données : Nous avons compris l'importance cruciale de la gestion des droits d'accès via RBAC pour assurer la sécurité et la confidentialité des données dans un environnement professionnel.

Gestion de projet : La gestion des contraintes d'intégrité lors de la migration a été un défi notable. Si nous devions refaire ce projet, nous prévoirions une phase de tests (potentiellement automatisés) plus robuste pour valider les insertions et les droits d'accès afin de gagner en efficacité.
