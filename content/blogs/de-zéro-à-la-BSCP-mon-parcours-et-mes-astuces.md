---
title: "De zéro à la BSCP : Mon parcours et Mes astuces ⚡"
# date: 2022-04-08T23:15:00+07:00
slug: De zéro à la BSCP -> mon parcours et mes astuces ⚡ 
category: blog 
summary:
description: 
cover:
  image: images/photo1.jpeg
  alt:
  caption:  
  relative: true
showtoc: true
draft: false
---

<img src="/images/bscp.svg" style="margin-left:30%;border:solid;border-color:#885FFF;">

- - -


#  Introduction : 


Je suis parti de rien, et après plusieurs mois de travail, j'ai décroché la certification **Burp Suite Certified Practitioner**.

Dans cet article, je partage les stratégies, astuces, et erreurs à éviter pour que toi aussi, tu puisses obtenir cette certification, même si tu pars de zéro !

Mon objectif est de te fournir une stratégie claire avec des étapes précises pour t'aider à passer l'examen efficacement.

- - - 
### Live avec [Laluka](https://x.com/TheLaluka)
Plus d'info sur la BSCP et Tips sur le Lifetsyle


<img src="/images/laluka.png" style="border:solid;border-color:#885FFF;">


**📽️👉**[Optimize Your BSCP -> Part 1](https://www.youtube.com/watch?v=eNYIq1Rc_08)

**📽️👉**[Optimize Your BSCP -> Part 2](https://youtu.be/62M5hRS673Y?feature=shared)

- - -

## 📌 Tu es intéressé par la BSCP mais tu ne sais pas par où commencer ? [Clique ici](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#kesako-la-bscp-)

## 📌 Tu vas bientôt passer la BSCP ? [Clique ici](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#les-meilleures-ressources-pour-préparer-la-bscp)

## 📌 Visiteur de l'ombre, juste curieux ? [Clique ici](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#kesako-la-bscp-)

- - -
- - -

### Kesako la BSCP ?

La Burp Suite Certified Practitioner (BSCP) est une certification officielle délivrée par les créateurs de Burp Suite. 

**"Becoming a Burp Suite Certified Practitioner demonstrates a deep knowledge of web security vulnerabilities, the correct mindset to exploit them, and of course, the Burp Suite skills needed to carry this out.**"  — *Port Swigger*

- - -

## 📊 Ce que vous devez savoir sur la BSCP : les notions clés

- **4 heures / 2 apps / 3 steps par apps** 
- **Step 1** : "Get access to any user" *(donc pas forcément Carlos)*
- **Step 2** : "Promote yourself to an administrator or steal admin's data" *(regarder les nouvelles features que vous avez avec votre utilisateur)*
- **Final step** : "Using the admin panel, read the contents of /home/carlos/secret on the application's file system" *(la vuln se trouve donc sur l'admin panel ou en rapport avec celui-ci !)*
- Vous êtes obligé d'exploiter chaque step dans l'ordre
- Il n'y a qu'un "active user" par application *(donc si premier steps vous l'avez utilisé, par exemple pour une XSS alors la vuln pour le deuxième steps ne pourra être en lien avec l'utilisateur actif et l'exploit server)*

- - -
- - -

# 🛤️ Mon parcours et ma méthodologie    From Zero to Certified BSCP

Zero Background
**En février 2024**, j'ai découvert Burp Suite et commencé les learning paths de PortSwigger sans plan précis (ce qui était une erreur). Mon seul objectif était d'apprendre le web.

Au début, tout semblait incompréhensible, mais avec de la persévérance, chaque pièce du puzzle a commencé à s'emboîter.

**Fin juin**, après avoir complété **plus de 50 %** des labs de PortSwigger, j'ai décidé de me concentrer sur la certification et de **créer un plan d'action de trois mois**. Cela a été la meilleure décision pour réussir la BSCP, me permettant de garder le focus, progresser étape par étape, et rester sur la bonne voie, même quand la motivation chutait.

*Mon plan d'action*

![image de mon plan d'action](/images/action-plan1.svg)

- - -

![image de mon plan d'action](/images/action-plan2.svg)

## 📝 L'importance d'un Plan d'Action :

**"An idiot with a plan can beat a genius without a plan."**  — *Warren Buffett*

**"If you fail to plan, you are planning to fail."**  — *Benjamin Franklin*

Parce qu'une vision sans plan est juste un rêve, mais une roadmap transforme ce rêve en réalité concrète, étape par étape. 

Le plan d'action permet de rester sur la bonne voie, même quand la vie devient difficile ou que la motivation vacille. Il sert de boussole, te rappelant les étapes à suivre, peu importe les obstacles. En te focalisant sur le process plutôt que sur l'émotion du moment, tu avances, pas à pas, vers tes objectifs, sans perdre de vue la direction.

- - -

## Mon Plan de Préparation :

J'ai divisé ma préparation en plusieurs étapes :

D'après mon expérience ainsi que ces ressources, il y aurait 23 types de vulnérabilités sur lesquels nous pouvons tomber :

<img src="/images/23vuln.png" style="margin-left:10%;border:solid;border-color:#b36481;">

[source](https://jacobcyber.medium.com/study-exam-guide-for-the-burp-suite-certified-practitioner-bscp-a64abdebfd38)
- - -
### J'ai donc listé ces 23 topics :

1. Compléter tous les labs du topic *(sauf ceux de niveau expert)*
2. Faire un Mystery Lab sur le topic ***pour vérifier ma maîtrise***
3. Créer une roadmap d'exploitation claire et comme on les aime ;)



![image de mon process / Zero to hero -> In progress -> Just mystery](/images/Process-bscp-start.png)

Chaque sujet est divisé en quatre catégories :

- **Zero to Hero** : Pas commencé
- **In Progress** : En cours
- **Just Mystery** : Mystery Lab uniquement
- **Full Done** : Complété


- - -
- - -
## Des Road quoi ?? (les fameuses Roadmaps d'exploitation)

Vous connaissez sûrement déjà les fameuses Roadmap d'exploitation **Immense** pour l'Active Directory d'[Orange](https://orange-cyberdefense.github.io/ocd-mindmaps/)

![LIttle Image of the AD orange road map](/images/pentest_ad_dark_2023_02.svg)

Notre cerveau est par défaut visuel : il assimile et retient **beaucoup mieux** les informations présentées sous forme de mindmap. En utilisant des **roadmaps**, j'ai structuré mon apprentissage pour ne jamais oublier comment exploiter une vulnérabilité. J'utilise [**Excalidraw**](https://excalidraw.com/) pour créer celles-ci.

- - -
### Exemple de Roadmap SSTI :

![Exemple visuel ici](/images/ssti.png)

je n'ai pas trouvé de solution afin de vous partagez mes notes avec la roadmap

🛑 Mettre en Noir la roadmap ! -> `CTRL + /` -> dark -> `Enter`

👉[Lien de la Roadmap sans mes notes ](https://excalidraw.com/#json=JjypEaWNFXGPs2yhwV9kS,mkJgF-Y0D2cHa1cvrL_IPg)


Elles contiennent :

- Des notes des labs réalisés
- Une cheat sheet spécifique
- Des images pour améliorer la rétention

Légende :

- **Bleu** = Phase de Reconnaissance
- **Rouge** = Phase d'Exploitation


Ces roadmaps m'ont permis d'organiser mes connaissances de manière efficace, rendant chaque exploitation plus intuitive et rapide pendant l'examen.

- - -
# Ma BSCP Roadmap

![Preview de la roadmap BSCP](/images/BSCP-ROADMAP.png)


🛑 Mettre en Noir la roadmap ! -> `CTRL + /` -> dark -> `Enter` 

👉[Click ici -> Lien de Ma ROADMAP BSCP](https://excalidraw.com/#json=wsXZjNIUK2mYBcBMdv69i,O18VLULtD4J5fDzTXHtqvA)


<img src="/images/youtube.png" style="margin-left:30%;border:solid;border-color:#885FFF;">

**📽️👉 [Explication vidéo de ma roadmap SSTI + Roadmap BSCP + Process By elimination](https://youtu.be/QaKsUK2EItI?si=f7oFuyegQbjDU7of)**  
_(🎯 Dans cette vidéo, je vais prendre l'exemple concret de la roadmap SSTI, et présenter Ma roadmap pour la BSCP)_

- - - 
## Voici par exemple une roadmap plus complexe et étoffée : celle des XSS

![My Big XSS Roadmap](/images/xss.png)

👉[Click ici -> Lien roadmap XSS (sans mes notes)](https://excalidraw.com/#json=olc_SyA3xCmOvYnHZJAb6,h75MbZMjap12LElWdaWoNA)

👉[Lien vers mes tips & tricks pour créer de bonnes roadmaps](blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#tips--tricks--comment-faire-les-meilleures-roadmaps)

---
- - -
# Ma Prise de Notes

Chaque lab que j'ai effectué se retrouve dans mes notes.

Et oui, **CHAQUE LAB** parce que **"Prendre des notes prend du temps, mais ne pas en prendre, c’est perdre son temps."**
— Elliot Meunier

La rétention de l'information est la clé pour apprendre.
N'oubliez pas la courbe de l'oubli.

![Image de la courbe de l'oubli](/images/Courbe_de_l'oubli.png)

- - -
### Mon Setup de Prise de Notes pour la BSCP

Un bon Obsidian sous stéroïdes et un template pour chaque lab PortSwigger.

![Image du template](/images/lab-template.png)

[📥 Téléchargez le Template](https://github.com/Atom-U/My-BSCP-tools/)

- - -
- - -
# Fin Août : Préparation juste avant la BSCP / La clé pour réussir la BSCP

Une fois les 23 topics terminés, je passe à la meilleure partie, celle qui va permettre de concrétiser tout mon savoir -> **faire 20 Mystery Labs (tous les sujets)**

<img src="/images/port-swigger-mystery-lab.png" style="border:solid;border-color:#885FFF;">

**J'ai donc créé une méthodologie en m'inspirant de ce site, avec les différentes possibilités de vulnérabilités en fonction des fonctionnalités.**

![Image de ma roadmap pour les Mystery Labs](/images/mysterly-lab.png)


🛑 Mettre en Noir la roadmap ! -> `CTRL + /` -> dark -> `Enter` 

👉[Click ici -> Lien de la roadmap mystery labs](https://excalidraw.com/#json=vRppITajm2KbzouWWcWPE,uD8cxQeL0Ln8yJCqUhG23Q)


- - -
## On passe aux choses sérieuses : Le Passage de l'Examen

<img src="/images/my-account-port-swigger.png" style="border:solid;border-color:#885FFF;">

<img src="/images/hall-of-fame.png" style="margin-left:30%;border:solid;border-color:#885FFF;">

### 14 Septembre : La Claque de la Vie


Alala, je m'y attendais, beaucoup de gens me l'avaient dit, la BSCP est dure. Je l'avais lu dans tous les blogs, la plupart des personnes échouent. Mais rien ne pouvait vraiment me préparer à cette claque. **Des centaines d'heures de travail, pour finalement se retrouver face à l'échec...**

C'était une phase psychologique  difficile, une remise en question de tout ce que j'avais fait, de chaque choix, de chaque minute passée à travailler. **Mais l'abandon n'était pas une option**. J'avais un plan, un plan qui me guidait malgré les doutes et la fatigue.

Alors, "what else ?" Si je rate, j'adapte puis je recommence. Parce que je crois en ce processus.  **Car chaque échec est une opportunité d'apprendre, de devenir plus fort.**&#x20;

**Test and Learn** Mindset

Ce n'était **pas seulement un examen**, c'était un **test de ma persévérance**, de ma capacité à me relever à chaque chute.


### 27 Septembre : Failed

- Understand -> Adapt -> Learn -> Try again

  **"You only fail when you stop trying."**\
  — *Thomas Edison*

### 2 Octobre : Failed

- Understand -> Adapt -> Learn -> Try again

  **C'est mathématique : tant que je n'abandonne pas, je ne peux pas perdre.**

### 5 Octobre : Failed

- Understand -> Adapt -> Learn -> Try again

  **C'est une question de temps avant que je l'obtienne.**

### 11 Octobre 💥 Succeed

Kawabunga 💥 Oh que oui, bonhomme !

<img src="/images/atom-quote.png" style="width: 512px; height: 512px; margin-left: 10%; border: solid; border-color: #885FFF;">

**"Success is not the absence of failure; it's the persistence through failure."**\
— *Aisha Tyler*

(J'ai reçu le certificat 7 jours après avoir passé l'examen, alors ne panique pas)

-- - 
-- - 
## Mon **Lifestyle** durant la Préparation de la BSCP (et actuel)
### Comment Maximiser ton Efficacité en Évitant le Burnout

L'utilisation du time blocking est un véritable gamechanger dans une vie. 

**Elon Musk lui-même** utilise le time blocking pour gérer ses journées. C'est une méthode qui lui permet de maximiser son efficacité et de rester concentré sur ses objectifs sans se laisser distraire. En bloquant des plages horaires dédiées à des tâches spécifiques.

Pour nous, cette méthode peut également transformer notre manière de travailler, en nous aidant à prioriser nos actions, à rester productifs, tout en évitant le pire énemie : **la dispersion**

- **Réveil à 5h** : Pour détruire tes objectifs en seulement 2h30 de boulot
- **Début du travail à 5h15** : Commencer à travailler juste après le réveil permet de rentrer dans le flow beaucoup plus facilement et de manière plus productive.
- **En jaune Sport tous les jours** : Crucial pour les bienfaits mentaux et physiques.
- **En rouge** : Travail sur la BSCP.
- **Sieste chaque midi** : Pour rester productif l'après-midi ainsi que la fin de journée.
- **Coucher à 21h** : Le sommeil est crucial pour l'apprentissage, la gestion du stress, et pour éviter le burnout.


<img src="/images/agenda.png" style="border:solid;border-color:#885FFF;">

Mes temps de repos sont donc :

- Le sport
- Le sommeil
- La douche
- Quand je mange
- Un peu de Free time

Et c'est tout ! Pas besoin de plus, car la cybersécurité, pour moi comme pour toi, est une passion !

### SAUF que 

Tu te dis **actuellement** : "Ce rythme n'est pas pour moi, je ne suis pas un lève-tôt...", "Je suis trop fatigué le matin...", "Je ne suis pas assez motivé...", "Je préfère travailler tard le soir...", "Je n'ai pas besoin de routines aussi strictes...", "Je suis trop occupé pour ça..."

**Toujours des excuses...** Mais rappeles-toi, ce n'est qu'en affrontant l'inconfort que l'on progresse. Tant que vous ne vous engagez pas sérieusement pendant au moins 2 semaines, vous ne saurez jamais de quoi vous êtes réellement capable. Donnez-vous une chance de surprendre la version de vous-même qui doute.

**Et oui, chaque matin à 5h, tu voudras rester au lit. Tu sentiras le poids de la fatigue, l'envie de tout laisser tomber. Mais c'est précisément ce moment qui définit tout : chaque fois que tu décides de te lever malgré les épreuves,  te prouves que tu es plus fort que tes excuses. C'est là que tu crées la différence, c'est là que tu forges ta réussite.**

**"Success isn’t always about greatness. It’s about consistency. Consistent hard work leads to success. Greatness will come."**\
— *Dwayne Johnson*


- - - 
- - - 
# Conclusion 


Passer la certification **BSCP** est loin d'être une promenade de santé. C'est un chemin semé d'obstacles, mais chaque étape, chaque échec, et chaque réussite te rapprochent de ton objectif. J'ai fait face à des moments de doute, des échecs, et parfois des moments de grande solitude, mais chaque échec m'a été utile pour m'améliorer, et chaque victoire a été le résultat de cette persévérance.

Si tu es prêt à te lancer dans cette aventure, rappelle-toi que **l'échec fait partie du process**, et que **le plan et la persévérance sont tes meilleurs alliés**. Créer une roadmap / plan d'action claire et prend des notes.

Ne te contente jamais du minimum. Vise haut, et sois toujours prêt à t'adapter et à apprendre. La **BSCP** est plus qu'une certification, c'est un **test de ta détermination**. Alors, peu importe combien de fois tu tomberas, souviens-toi toujours : "**You only fail when you stop trying**". 
Bonne chance dans cette aventure !

n'hésite pas à me contacter !

**Stay hard**

---
---

# Les Meilleures Ressources pour Préparer la BSCP

[📥 Mes ressources](https://github.com/Atom-U/My-BSCP-tools/)


## Mystery Labs : La Clé pour Réussir la BSCP

Explication juste ici 

👉 [Click ici -> Lien vers un peu plus haut dans la page](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#fin-août--préparation-juste-avant-la-bscp--la-clé-pour-réussir-la-bscp)

---

## Mon Setup pour Passer la BSCP


- Burp Pro
- Les extensions qui vont bien
- Sublime Text
- Mes roadmaps
- WSL
- Chrome
- ChatGPT
- Cyberchef

- - - 

## Les extension a utiliser 

1. **Java Deserialization Scanner** : Essentielle pour l'exam.
2. **HTTP Request Smuggler** : Essentiel pour l'exam, complète le scan de Burp pour le request smuggling.
3. **Logger++** : Capture les requêtes/réponses HTTP.
4. **Param Miner** : Essentiel pour l'exam, utile pour le web cache poisoning.
5. **JSON Web Tokens** : Manipule et teste les jetons JWT.
6. **JWT Editor** : Édite les jetons JWT pour tester.
7. **Collaborator Everywhere** : Essentiel pour l'exam, complète le scanner de Burp pour détecter les attaques par host header.
8. **Reflector** : Non essentiel, aide à détecter des XSS reflected.


- - - 
## L'utilisation de mon Template *Proceed by elimination*

![image du template en svg](/images/Proceed-by-elimination-BSCP.svg)

**📽️👉 [Explication vidéo de ma roadmap SSTI + Roadmap BSCP + Process By elimination](https://youtu.be/QaKsUK2EItI?si=f7oFuyegQbjDU7of)**  

[📥 Téléchargez le Template](https://github.com/Atom-U/My-BSCP-tools/)
- - -
## Mon Template Obsidian pour Passer la BSCP

[📥 Téléchargez le Template](https://github.com/Atom-U/My-BSCP-tools/)

![Image du premier aperçu du template](/images/template-bscp01.png)
![Image du premier aperçu du template](/images/template-bscp02.png)
- - -
### Les meilleurs ressources externe

#### Video : 
1. [Crypto Cat](https://www.youtube.com/watch?v=L-3jJTGLAhc)  Plein de petit tips
2. [Daniel Redferm](https://www.youtube.com/watch?v=Lbn8zQJByGY) Super tips + exemple de la pérséverance car il a fait plus de 10 attemps

#### Blog / Github

1. [Nishacid](https://nishacid.guru/articles/bscp/) Bonne info + WSAAR tools
2. [micahvandeusen](https://micahvandeusen.com/burp-suite-certified-practitioner-exam-review/) Liste des 23 vulnérabilitées

3. [BotesJuan](https://github.com/botesjuan/Burp-Suite-Certified-Practitioner-Exam-Study) Super ressource qui répèrtorie beaucoup de note, qui ma beaucoup aider
4. [Dingy Shark](https://github.com/DingyShark/BurpSuiteCertifiedPractitioner) Super ressource qui répèrtorie beaucoup de note 
5. [Edra xss]([https://github.com/Edr4/XSS-Bypass-Filters](https://github.com/Edr4/XSS-Bypass-Filters)) Best for the XSS
---

## Tips & Tricks


### Tips & Tricks : Si tu commences ton ascension vers la BSCP

1. Fais un plan d'action solide.
   C'est la première chose que tu dois faire Voir ici l'importance du plan d'action [plan d'action](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#-mon-parcours-et-ma-méthodologie----from-zero-to-certified-bscp)
2. Concentre-toi sur les 20% qui vont te donner 80% des résultats (loi de Pareto).
3. Prend des notes claire pour chaque lab que tu fais
4. Relecture de ces notes chaque semaine afin d'assimiler toutes ces informations 
5. Faire tout les jours du port swigger, ou une action qui te fait avancé vers ton objectif (la BSCP)
6. Ne jamais avoir plus de 3 jours sans faire du port swigger, le fait de ne pas pratiquer tout les jours risque de te retarder considérablement

- - -
### Tips & Tricks si tu vas bientôt passer la BSCP

1. As tu fait au moins 60% de port swigger ? 
2. Dévelope ta methodolgie en faisant plus de 20 mystery labs (sans reveler l'objectif)
3. Ne te contente pas des prérequis de PortSwigger pour la BSCP, fais bien plus.
4. Fais un plan d'action solide.
   C'est la première chose que tu dois faire [Voir ici l'importance du plan d'action](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#-limportance-dun-plan-daction-)
5. Lit bien [Les hint de port swigger](https://portswigger.net/web-security/certification/exam-hints-and-guidance) tu découvriras des choses

- - -
### Tips & Tricks : l'Examen de la BSCP

1. Utiliser Burp Scanner, cela vous permet de gagner beaucoup de temps
	- Savoir ce que Burp scanner peut trouver comme vuln 
2. L'examen est dur : trouver 6 vulnérabilités en 4h ne vous laisse que 40 minutes par vulnérabilité, y compris leur exploitation.
3. Si vous échouez, pas de problème, vous avez un plan d'action, vous savez exactement quoi faire. Apprenez de vos erreurs et recommencez jusqu'à l'obtenir.
4. Envoyez-moi un message, je vous partagerai d'autres ressources qui ne sont pas ici ;)
5. Il est nécessaire d'utiliser Windows, car la plateforme de surveillance de l'examen n'est pas compatible avec Linux :/
6. Si vous trouvez une SSRF elle sera sur le port `localhost:6566` et te permettra d'avoir un *File Reading* pour le stage 3 
7. La victime utilise Chromuim (toujours bon a savoir pour les XSS)
8. Ne tomber pas dans **The rabbit hole**, si vous ne trouvez pas prenez un petite pause, prenez du recul comme un oiseau qui s'élève
9. Si vous ne trouvez rien faites par elimination en utilisant [Proceed by elimination](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#lutilisation-de-mon-template-proceed-by-elimination)
10. Je donne quelques mini tips au debut de [cette article sur les differents Stage](/blogs/de-zéro-à-la-bscp-mon-parcours-et-mes-astuces/#-ce-que-vous-devez-savoir-sur-la-bscp--les-notions-clés)


- - -
### Tips & Tricks : Comment Faire le Meilleur Plan d'Action

Je rêve ou... tu vas faire un plan d'action ? Top ! 
Les plans d'action sont l'autoroute du succès.

1. Décomposez au mieux votre objectif.
2. Fixez des deadlines.
3. Planifiez les obstacles potentiels que vous pouvez rencontrer (exemple : échouer à la BSCP).
4. Identifie les ressources (temps, outils, compétences) que tu as à disposition. Cela t'aidera à adapter ton plan en fonction de la réalité
5. Mets en place des points de contrôle hebdomadaires ou mensuels pour suivre tes progrès par rapport au plan
6. Un bon plan d'action doit être adaptable
7. À chaque étape franchie, prends un moment pour reconnaître tes progrès
8. Envoie moi ton plan d'action ^-^ 

- - -
### Tips & Tricks : Comment Faire les Meilleures Roadmaps

1. Plus vous ferez de roadmaps, plus votre cerveau les comprendra.
2. Utilisez Excalidraw dans Obsidian afin de pouvoir relier vos notes (celles des labs) avec vos roadmaps.
3. Utilisez les raccourcis d'Excalidraw, vous gagnerez beaucoup de temps dans la création de roadmaps.
   - Exemple : A = permet de créer une flèche.
4. Faites en sorte que vos roadmaps soient agréables et les plus lisibles possible. Celles-ci vous permettront de les exploiter plus rapidement pendant l'examen (n'oubliez pas, vous n'avez que 4h ! Tic Tac Tic Tac).
5. Vous allez en faire beaucoup des roadmaps, alors créez-vous un template, comme ça, un simple copier-coller et c'est fait.
6. Revoyez chaque jour au moins une de vos roadmaps. Vous verrez, plus vous en ferez, plus votre état d'esprit va changer, et vous changerez plein de petits détails dans celles-ci.
7. **📽️👉 [Explication vidéo de ma roadmap SSTI + Roadmap BSCP](https://youtu.be/QaKsUK2EItI?si=f7oFuyegQbjDU7of)**  

- - - 

Good luck ! 

Send me a message ;) 🫴 [Mon discord](https://discord.com/users/user19216820011)


---

# Sources de l'Article

- [My BSCP tools](https://github.com/Atom-U/My-BSCP-tools/)
- [Roadmap SSTI (sans notes)](https://excalidraw.com/#json=JjypEaWNFXGPs2yhwV9kS,mkJgF-Y0D2cHa1cvrL_IPg)
- [Roadmap BSCP](https://excalidraw.com/#json=wsXZjNIUK2mYBcBMdv69i,O18VLULtD4J5fDzTXHtqvA)
- [roadmap XSS (sans notes)](https://excalidraw.com/#json=olc_SyA3xCmOvYnHZJAb6,h75MbZMjap12LElWdaWoNA)
- [Roadmap Mystery Labs](https://excalidraw.com/#json=vRppITajm2KbzouWWcWPE,uD8cxQeL0Ln8yJCqUhG23Q)
- [Template BSCP exam sur GitHub](https://github.com/Atom-U/My-BSCP-tools/)
- [Vidéo sur la roadmap SSTI + Roadmap BSCP + Process By elimination](https://youtu.be/QaKsUK2EItI?si=f7oFuyegQbjDU7of)
- [Crypto Cat - Vidéo YouTube](https://www.youtube.com/watch?v=L-3jJTGLAhc)
- [Daniel Redferm - Vidéo YouTube](https://www.youtube.com/watch?v=Lbn8zQJByGY)
- [Blog de Nishacid](https://nishacid.guru/articles/bscp/)
- [Blog de Micah Vandeusen](https://micahvandeusen.com/burp-suite-certified-practitioner-exam-review/)
- [BotesJuan - GitHub](https://github.com/botesjuan/Burp-Suite-Certified-Practitioner-Exam-Study)
- [Dingy Shark - GitHub](https://github.com/DingyShark/BurpSuiteCertifiedPractitioner)
- [Edra xss - GitHub](https://github.com/Edr4/XSS-Bypass-Filters)
- **📽️👉**[Optimize Your BSCP -> Part 1](https://www.youtube.com/watch?v=eNYIq1Rc_08)
- **📽️👉**[Optimize Your BSCP -> Part 2](https://youtu.be/62M5hRS673Y?feature=shared) 
---

