# GLOSSAIRE

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)
- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général
1.  Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte
    - Pour exécuter un script PHP, il est nécessaire d’avoir un serveur PHP. Laragon et Xammp sont des logiciels permettant ceci.

2.  Qu’est-ce qu’un algorithme ?
    - Un algorithme est une suite logique d’instructions permettant d’atteindre un résultat à partir d’un objectif donné.

3.  Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?
    - Une variable est un stockage permettant de garder une donnée en mémoire dans un algorithme. Il faut premièrement la déclarer (initialiser), puis lui attribuer une valeur, qui peut être changée plusieurs fois au cours de l’algorithme. A chaque attribution, sa valeur précédente est écrasée.

4.  Qu’est-ce que la portée d’une variable ?
    - La portée d’une variable désigne la portion du code dans laquelle elle est accessible. 

5.  Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?
    - Une constante est un stockage de donnée dans un algorithme qui est fixe, on ne peut pas changer sa valeur une fois qu’elle est déclarée.

6.  Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation
    - Ce sont des variables internes qui sont toujours disponibles dans un programme. $GLOBALS, $_SERVER, $_GET, $_POST, $_FILES, $_COOKIE, $_SESSION, $_REQUEST, $_ENV 
    
7.  Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)
    - null : type à valeur unique, c’est souvent un type attribué par défaut sur une var indéfinie. 

    - bool : type booléen, dont la valeur est soit true soit false. 
    
    - int : type nombre entier. 
    
    - float (floating-point number) : type nombre décimal, inclue float, double & real numbers. 
    
    - string : type chaine de caractère. 
    
    - array : type tableau. 
    
    - object : type objet, appartenant à une classe. 
    
    - callable : type appel de fonction/méthode. 
    
    - resource : type spécial faisant référence à une ressource interne.     

8.  Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?
    - Il existe deux types de tableaux : les tableaux indexés, ou simples, qui associent une valeur à un index qui commence à 0, et les tableaux associatifs qui associent une valeur à une clé. 

    - Ex : FR -> bonjour, ENG -> hello 

9.  Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles
    - F, ELSE (SI, SINON) : structure de condition qui donne deux instructions alternatives. 
    - ESLEIF (SINON SI) : ajout au SI, SINON qui permet d’imbriquer plus de conditions. 
    - FOR (POUR) : boucle iterative permettant d’exécuter une tache autant de fois que prévu. 
    - WHILE (TANTQUE) : boucle permettant d’exécuter une tache tant que sa condition est remplie. Cela signifie qu’elle peut s’exécuter sans fin si la condition reste vraie. 
    - DO UNTIL (JUSQU’A) : boucle permettant d’exécuter une tache jusqu’à ce que la condition soit remplie. 

10. Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
    - Il s’agit de la fonction strlen($chaine); 

11. Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP
    - Une session est une méthode de stockage de données spécifiques à un utilisateur. On utilise alors un ID de session envoyé au navigateur via cookie. Pour démarrer une session en PHP, on utilise la fonction session_start();     

12. Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
    - Un cookie est un paquet de données communiquée entre le serveur et le client HTTP. Ils servent à créer et maintenir des sessions.
 
13. Quelle est la différence entre les instructions « require » et « include » en PHP
    - Elles font la même chose, mais impose une condition différente : si le fichier requis n’est pas présent, require retourne une fatal error, tandis que include renvoie un avertissement.

14. Comment effectuer une redirection en PHP ?
    - Une redirection en PHP se fait avec la fonction header(), qui prends en paramètre Location: suivi de l’url de la page vers laquelle on veut rediriger. 

15. Définir la partie « front-end » et « back-end » d’une application
    - Le front-end correspond à la partie visible à l’utilisateur : design, intégration, UI, UX.

    - Le back-end correspond à la partie "arrière" du site : les traitements de données, l’automatisation, la BDD ... etc. 

16. Définir le contrôle de version ? Qu’est-ce que Git ?
    - Le contrôle de version, ou versioning est une méthode de transfert et de stockage de fichiers non destructif, qui permet de garder plusieurs versions d’un projet, ainsi que d’avoir plusieurs branches de développement en parallèle, et de les fusionner au besoin. Git est la méthode de versioning la plus utilisée aujourd’hui.

17. Qu’est-ce qu’un CMS ? Citer au moins 2 exemples
    - Un CMS (content management system) ou SGC (système de gestion de contenu) est un logiciel, souvent en ligne, qui permet de créer et gérer un site web en utilisant uniquement l’IDE (integrated developpement interface).
    - Deux CMS populaires sont Wordpress (pour une utilisation générale) et Magento (pour le développement de site commerciaux).

## Front-end
18. Définir HTML
    - HTML, pour HyperText Markup Language, est un langage de balisage servant à structurer une page web. Il s’agit d’une structure sémantique, et ne comprends pas la mise en page.

19. Définir CSS
    - CSS, pour Cascade Style Sheet, est un langage web complémentaire au HTML qui sert lui à gérer le style d’une page. On utilise un sélecteur, auquel on passe des propriétés à qui on donne des valeurs. 
    - Ex : on passe à tous les éléments contenus dans une balise <p> la propriété “color : red;”, ce qui rendra le texte rouge. 

20. Définir Javascript
    - JavaScript est un langage de script orienté objet et est utilisé dans la plupart des cas à ajouter des éléments de logique algorithmique dans une page HTML. 

21. Définir JSON. Dans quel contexte ce format est-il utilisé ?
    - JSON (JavaScript Object Notation) est un format de donnée textuel.

22. Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?
    - On ne peut pas le faire avec JS native, cependant Node.js permet l’exécution de JavaScript coté serveur dans le contexte de son environnement.

23. Qu’est-ce qu’un sélecteur CSS ?
    - Un sélecteur CSS correspond à l’élément que l’on va affecter avec des propriétés. Il peut s’agir d’une balise en général, d’une classe (qui regroupera tous les éléments appartenant à cette classe) ou d’un ID (qui ne fera référence qu’a l’élément qui porte cet ID unique). 

24. Quelle balise HTML permet de créer un lien hypertexte ?
    - Il s’agit de la balise anchor, qui s’écrit <a href= “url”> texte auquel on applique le lien</a>.

25. Qu’est-ce qu’une requête AJAX ?

26. Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?
    - Pour une classe, on utilise le selecteur ‘.’ 
	- Pour un ID, on utilise le selecteur ‘#’ 

27. Définir le responsive design
    - Le responsive design correspond au développement d’un front end qui s’adapte au mieux pour supporter un maximum d’appareils, mais aussi d’utilisateurs qui peuvent avoir des 	besoins spécifiques (handicap, ...etc) 

28. Qu’est-ce que le templating ?
    - Le templating consiste à créer un fichier php “squelette” qui contiendra la structure statique 	de la page affichée (header, footer, wrapper) dans laquelle on insèrera une variable content, qui sera récupérée dans les autres fichiers de l’appli web via output buffer. Finalement, le template est appelé dans ces autres fichier avec un require. 

29. Qu’est-ce qu’une fonction anonyme en Javascript ?

30. Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
    - Il s’agit de la méthode Array.push(element).

31. Qu’est-ce qu’un « media query » ?
    - Un media query est une condition qui spécifie des dimensions d’affichage, et applique des propriétés uniquement lorsqu’un utilisateur rentre dans ce cas de figure. 

32. Qu’est-ce qu’un pseudo élément en CSS ?
    - Un pseudo élément est un mot clé ajouté à un élément et permet de cibler une partie spécifique, ou un contexte spécifique de l’élément. On lie un élément et un pseudo-élément par “::”, sans espaces. 

33. Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
    - Bootstrap est une librairie CSS & JS. C’est un des outils de développement frontend les plus populaires, et permet de mettre en page un site en très peu de temps. 

34. Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes
    - Ce sont les methodes GET et POST, la différence étant que GET envoie les données dans l'URL tandis que POST l'envoie directement au serveur.

## UX UI
35. Quelle est la différence entre UX Design et UI Design ?
    - Le UX (user experience) design consiste à concevoir l’expérience utilisateur, c’est à dire l’ergonomie du site, l’intuitivité des fonctions, mais aussi l’inclusivité sous tous ses aspects. 

    - Le UI (user interface) design consiste à concevoir l’interface de l’appli, donc en respect avec le UX design, et va développer l’aspect visuel de l’ergonomie et l’accessibilité du site. 

36. Qu’est-ce qu’un wireframe ?
    - Un wireframe est une maquette conceptuelle du site, qui va mettre en place l’organisation visuelle de la page (dimensionner les éléments, ajuster les polices). 

37. Qu’est-ce qu’un prototype ?
    - Un prototype, ou mockup, est une maquette complète, simulant entièrement la présentation visuelle du site, que ce soit les plages de couleurs, les polices custom ...etc. 

38. Qu’est-ce que la hiérarchie visuelle en UI Design ?

39. Qu’est-ce que l’accessibilité en UX Design ?
    - En UX design, l’accessibilité est le principe selon lequel l’application développée doit pouvoir être utilisée par le maximum de profils différents, en autre mots, être accessible à tout le monde. Cela consiste à prendre en compte la possibilité d’utilisation (accommodation 	aux handicaps, ...etc) mais aussi l’inclusivité aux profils marginalisés qui pourrait techniquement faire sans (pas impossible) mais qui se sentirais mal à l’aise (ex: prendre en compte les profils LGBTQ+ quand on réalise un formulaire d’inscription, si ces infos personnelles sont pertinentes bien entendu). 

40. Qu’est-ce qu’une grille de mise en page ?

41. Qu’est-ce que la notion d’affordance en UX Design ?

42. Qu’est-ce qu’un « mobile first design » ?
    - Le design mobile first consiste à commencer le développement front par la version mobile, la plus compacte, et d’élargir le design responsive jusqu’à la version desktop. 

## Programmation orientée objet (POO)
43. Donner une définition de la programmation orientée objet
    - La programmation orientée objet (POO) est un type de programmation défini par une organisation du code en classes (concept du sujet traité) et objets (instances du sujet traité). 

44. Qu’est-ce qu’une classe ? Comment la déclare-t-on ?
    - Une classe correspond à la catégorie générale de l’objet que l’on va traiter dans le code, son « concept », qui prendra en attribut les différentes caractéristiques de tout objet de ce type. 

    - Ex : Un objet Toyota sera de la classe Voiture, avec pour attribut $_marque. 

    - Une classe est déclarée avec Class Nomclasse {} 

45. Qu’est-ce qu’un objet ?
    - Un objet sera quant à lui l’instance spécifique d’une classe, l’objet précis sur lequel on travaille. On le génère à partir de la classe selon la sythaxe suivante :  

    - nomobjet= new Nomclasse(paramètres) ; 

47. Définir la notion de propriété / attribut / méthode
    - Une propriété correspond à une variable interne à une classe. 

    - Attribut est synonyme de propriété, mais on préfère l’utiliser en référence aux propriétés que l’on crée manuellement pour une classe spécifique. 

    - Une méthode correspond à une fonction appartenant à une classe, qui pourra être appliquée à n’importe quel objet de cette classe. 
    
48. Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité
    - les visibilités en POO sont :  

    a. Public : disponible dans toutes les classes et objets. 

    b. Private : disponible seulement dans la classe. 

    c. Protected : disponible dans la classe et toute autre qui en hérite. 

49. Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
    - Il s’agit de la méthode magique __construct, que l’on appelle ainsi : 

    - $objet = new classe(paramètres); 

50. Qu’est-ce que l’encapsulation ?
    - L’encapsulation est le principe de gestion de la visibilité des attributs et méthodes d’une classe. On mettra les attributs en private dans la majorité des cas, et on y accèdera via getter/setter si on veut les récupérer dans une autre classe. Les méthodes seront en public car on veut pouvoir les appeler partout dans le programme.

51. Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple
    - Etendre une classe emploie le concept d’héritage. Cela veut dire qu’on créer une hiérarchie de classe, entre une classe parent et une ou plusieurs classes filles. 

52. Définir l’opérateur de résolution de portée
	- L'opérateur de résolution de portée :: permet d'accéder à une constante, propriété statique ou méthode statique d'une classe ou de sa classe parent.

53. Définir une méthode / propriété statique
	- Une méthode ou propriété statique peut être appelée sans instancier la classe auxquels ils appartiennent.

54. Définir le polymorphisme en POO
	- Le polymorphisme est un concept visant à créer des methodes et fonctions hautement réutilisables qui s'adaptent en fonction des objets qui les appellent. Cela se fait grace à des classes abstraites et/ou des interfaces.

55. Définir une méthode / classe abstraite ?
	- Une classe abstraite est une classe qui ne peut pas être instanciée, son but étant d'être heritée par une classe contcrète. Une méthode abstraite ne peut être déclarée que dans une classe abstraite, et ne définie pas son implémentation.

56. Définir le chaînage de méthodes
    - Le chaînage de méthodes correspond à appeler une méthode d'une classe parant dans une autre méthode d'une classe fille.

57. Qu’est-ce que la méthode __toString() ? Existe-t-il d’autres méthodes « magiques » ?
    - La méthode toString est une méthode magique qui permet d’établir un affichage basique pour les objets d’une classe, que l’on pourra appeler simplement avec $this. 

58. Qu’est-ce qu’un « autoload » ?
    - L’autoload est une méthode permettant d’établir l’accès permanant à un fichier, souvent une classe parent, afin de ne pas avoir à l’appeler plusieurs fois. 

59. Comment appelle-t-on en français les « getters » et les « setters » ?
    - Getter = accesseur 

    - Setter = mutateur 

60. Qu’est-ce que la sérialisation en PHP ?

## Architecture 
60. Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence
	- L'architecture client / serveur désigne un mode de transfert de données entre un "client" (le navigateur) qui va envoyer des requêtes, et un serveur qui va les recevoir et y répondre. Cette communication se fait via des requêtes HTTP, ou Hyper Text Transfer Protocol. HTTPS est la version sécurisée (d'où le S) et va encrypter les requêtes HTTP émises par le client. Elle validera aussi un certificat d'authenticité fourni par le site.

61. Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
	- Un design pattern, ou patron de conception, est un modèle d'arrengement de fichiers et de modules permettant de répondre à un besoin général lors du développement d'un logiciel/application.

62. Qu’est-ce que l’architecture MVC ?
	- L'architecture MVC consiste à organiser le code de l'application en 3 parties : le modèle, les vues et les controlleurs. C'est à dire, classifier le code qui s'occupera de la connexion, de l'affichage et de la logique.

63. Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
	- le modèle contient les données, ou plus souvent la methode de connexion à la bdd
	- le controlleur contient toutes les instructions logiques liées au traitement des données
	- la vue contient toutes les pages d'affichage du site

64. Quels sont les avantages de l’architecture MVC ?
	- MVC permet d'organiser son code de façon plus lisible et facilite donc la maintenance. C'est particulièrement pertinant pour un site web qui peut être voué à un service prolongé, qui demandera donc de nombreuses interventions et souvent par des devs différents.	

65. Existe-t-il des variantes à l’architecture MVC ?
	- Il existe les patrons MVP et MVVM :
	- MVP diffère en remplacent le controlleur par la présentation, et change la dyamique avec la vue. La vue gère des évenements qu'elle transmet en traitement à la présentation.
	- MVVM, ou modèle-vue vue-modèle instaure une communication bidirectionnelle entre la vue et le modèle.

66. Qu’est-ce qu’une API ? Définir l’architecture REST
	- Une API (application programming interface, ou interface de programmation) est un "programme" (entendre : ensemble de classes, méthodes, fonctions et constantes) qui à pour but d'offire un service à un autre programme.
	- L'architecture REST (REpresentational State Transfer) est un ensemble de conventions (et pas réelement une tech en soi). Ses 5 règles sont : utiliser l'URI (passé dans l'URL) comme identifiant des ressources, utiliser les verbes HTTP (POST, GET) comme identifiant des operations, utiliser les réponses HTTP comme représentation des ressources, utiliser des liens comme relation entre ressources et utiliser un paramètre comme jeton d’authentification.

## Modélisation - Base de données
67. Qu’est-ce que la modélisation de données ? Définir la méthode Merise
68. Quelles sont les 3 étapes principales de la méthode Merise ?
    a.  Analyse, conception et réalisation
    b.  Planification, exécution et contrôle
    c.  Création, modification et suppression
69. Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
70. Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
71. Donner la définition des mots suivants :
	a.  Entité
	b.  Relation
	c.  Cardinalité
	d.  Clé primaire / clé étrangère
72. Que devient une relation de type « Many To Many » dans le modèle logique de données ?
73. Qu’est-ce qu’une base de données ?
74. Définir les notions suivantes :
    a.  SQL
    b.  MySQL
    c.  SGBD (donner 2 exemples de SGBD)
75. Dans une base de données, les données sont stockées dans des ___. Celles-ci sont constituées de lignes appelées ___ et de colonnes appelées ___
76. Quelle est la différence entre une base de données relationnelle et non relationnelle ?
77. Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
78. A quoi sert une vue dans une base de données ?
79. Qu’est-ce que l’intégrité référentielle dans une base de données ?
80. Quelles sont les fonctions d’agrégation en SQL ?
81. Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?
82. Quelles sont les clauses qui permettent de :
    a.  Insérer un nouvel enregistrement dans une table
    b.  Modifier un enregistrement dans une table
    c.  Supprimer un enregistrement dans une table
    d.  Supprimer la base de données
    e.  Filtrer les résultats d’une requête SQL
    f.  Trier les résultats d’une requête SELECT
    g.  Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
    h.  Concaténer 2 chaînes de caractères
83. Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?

## Symfony
84. Qu’est-ce que Symfony ?
85. Sur quel langage de programmation et design pattern repose Symfony ?
86. Quelle est la dernière version en date de Symfony ?
87. Qu’est-ce qu’un bundle ?
88. Quel est le moteur de template utilisé par défaut dans Symfony ?
89. Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
90. Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?
91. Que permet le bundle Maker au sein de Symfony ?
92. Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
93. Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?

## Sécurité
94. Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
95. Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
96. Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
97. Définir l’attaque par force brute et l’attaque par dictionnaire
98. Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
99. A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
100. Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
101. Qu’est-ce qu’une politique de mots de passe forts ?
102. Qu’est-ce que l’hameçonnage ?
103. Définir la « validation des entrées »

## RGPD
104. Qu’est-ce que le RGPD ?
105. Quel est son objectif principal ?
106. Quelle est la date d’entrée en vigueur du RGPD ?
107. Quelles sont les sanctions possibles en cas de non-respect du RGPD ?
108. En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?
109. Quel est le consentement valide selon le RPGD ?
110. Qu’est-ce qu’une politique de confidentialité ?
111. Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
112. Quels sont les droits des utilisateurs selon le RGPD ?
113. Qu’est-ce que le principe de minimisation des données selon le RGPD ?

## SEO
114. Qu’est-ce que le SEO ?
115. Quel est l’objectif principal du SEO ?
116. Existe-t-il plusieurs types de référencement ? Lesquels ?
117. Qu’est-ce que la densité de mots-clés en SEO ?
118. Qu’est-ce qu’une balise « alt » ?
119. Qu’est-ce que la balise « meta description » ?
120. Qu’est-ce que le « nofollow » en SEO ?
121. Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?
122. Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
123. Quelle est la recommandation pour les URL d'un site web bien référencé ?
124. Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
125. Qu'est-ce que l'optimisation des images pour le référencement ?
126. Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?

## Gestion de projets - DevOps
127. Qu’est-ce que la gestion de projet ?
128. Qu’est-ce qu’une méthode Agile de gestion de projet ?
129. Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
130. A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
131. Qu’est-ce que la planification itérative ?
132. Citer 3 méthodes Agiles dans le cadre d’un projet informatique
133. Qu’est-ce qu’une réunion de revue de projet ?
134. Qu’est-ce qu’un livrable dans un projet ?
135. Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
136. Qu’est-ce que le DevOps et quel est son objectif principal ?
137. Qu’est-ce que l’intégration continue ?
138. Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
139. Qu’est-ce qu’un test unitaire ?
140. Quelle est l'unité de code testée lors d'un test unitaire ?
141. Quelles sont les caractéristiques d'un bon test unitaire ?
142. Qu'est-ce qu'une assertion dans un test unitaire ?

## English
1) What does JavaScript enable you to do on a website ?
    a.  Add interactive behavior and dynamic content
    b.  Define the layout and design of web pages
    c.  Handle server-side operations
2) Which programming language is primarily used for server-side web development ?
    a.  PHP
    b.  JavaScript
    c.  HTML
3)  What is the purpose of a web browser ?
    a.  To render and display web pages
    b.  To execute serve-side code
    c.  To manage databases
4)  What is the difference between GET and POST methods in HTTP ?
    a.  GET retrieves data from a server, while POST submits data to a server
    b.  GET submits data to a server, while POST retrieves data from a server
    c.  GET and POST methods are interchangeable
5)  What is the purpose of version control systems (e.g., Git) in web development ?
    a.  To track changes and manage collaborative development
    b.  To optimize website loading speed
    c.  To handle server-side scripting
6)  What is the purpose of a framework in web development ?
    a.  To provide a structured environment for building web applications
    b.  To handle network protocols and data transfer
    c.  To create visual designs and layouts for websites
7)  What does NoSQL stand for ?
    a.  Not Only SQL
    b.  Non-Structured Query Language
    c.  New Object-Oriented Language
9)  Which of the following is a characteristic of NoSQL databases ?
    a.  Strict schema enforcement
    b.  Support for complex transactions
    c.  Scalability and flexible data models
