# Battre les moyennes

L'original: <http://paulgraham.com/avg.html>

Avril 2001, révisé Avril 2003

(Cet article est dérivé d'un discours donné au 2001 Franz Developer
symposium.)

En été 1995, mon ami Robert Morris et moi avons lancé une startup qui
s'appelait Viaweb. Notre plan était de développer un logiciel permettant aux
utilisateurs de créer des magasins en ligne. Ce qui était nouveau pour ce
logiciel, à l'époque, c'est qu'il fonctionnait sur notre serveur en
utilisant des pages Web ordinaires comme interface.

Beaucoup de monde aurait pu avoir cette idée à ce moment-là, mais pour
autant que je sache, Viaweb était la première application Web-based. Cela
nous a semblé une idée si innovante que nous avons nommé notre société
d'après elle: Viaweb, parce que notre logiciel marchait via le Web, au lieu
de fonctionner sur votre ordinateur de bureau.

Une autre chose inhabituelle par rapport à ce logiciel était le fait qu'il a
été écrit en un langage de programmation qui s'appelle Lisp. En fait,
c'était une des premières grandes applications à être écrite en Lisp, qui
jusque-là avait été utilisé principalement par les universités et les
laboratoires de recherche.

## L'arme secrète

Eric Raymond a rédigé un essai intitulé “Comment devenir un Hacker” et dans
celui-ci, entre autres, il dit aux hackers potentiels quels langages ils
doivent apprendre. Il suggère de commencer par Python et Java, car ils sont
faciles à apprendre. Le hacker sérieux voudra aussi apprendre C, pour hacker
Unix, et Perl pour l'administration des systèmes et des scripts cgi. Enfin,
le hacker véritablement sérieux doit considérer d'apprendre Lisp:

> Lisp vaut la peine d'être appris pour l'expérience de l'illumination
> profonde qu'on aura quand on l'a finalement appris ; cette expérience fera
> de vous un meilleur programmeur pour le reste de vos jours, même si vous
> n'utiliserez jamais beaucoup Lisp.

C'est le même argument que vous avez tendance à entendre parler de
l'apprentissage du Latin. Ça ne vous donnera pas de travail, sauf peut-être
en tant que professeur de lettres classiques, mais il améliora votre esprit
et ferra de vous un meilleur écrivain en langues que vous voulez utiliser,
comme anglais.

Mais attendez un moment. Cette métaphore ne va pas si loin. La raison pour
laquelle le latin ne vous trouvera pas un emploi est que personne ne le
parle. Si vous écrivez en latin, personne ne peut vous comprendre. Mais Lisp
est un langage de programmation, et les ordinateurs parlent quel que soit le
langage vous leur dites de parler.

Donc si Lisp fait de vous un meilleur programmeur, comme il dit, pourquoi ne
voudriez-vous pas l'utiliser? Si un peintre se voyait offrir un pinceau qui
pourrait faire de lui un meilleur peintre, il me semble qu'il veuille
l'utiliser dans toutes leurs peintures, n'est-ce pas? Je n'essaie pas de me
moquer d'Eric Raymond. Dans l'ensemble, ses conseils sont bons. Ce qu'il dit
de Lisp est plutôt sagesse conventionnelle. Mais il y a une contradiction
dans la sagesse conventionnelle: Lisp ferra de vous un meilleur programmeur
et pourtant vous n'allez pas l'utiliser.

Pourquoi pas? Les langages de programmation ne sont que des outils, après
tout. Si Lisp produit vraiment de meilleurs programmes, vous devez
l'utiliser. Et sinon, qui en a besoin?

Ce n'est pas juste une question théorique. Le développement de logiciels est
une activité très compétitive, sujette aux monopoles naturels. Une
entreprise qui écrit des logiciels plus rapidement et mieux, toutes choses
égales par ailleurs, mettra ses concurrents en faillite. Et lorsque vous
démarrez une startup, vous le ressentez très fort. Les startups ont tendance
à être une proposition tout ou rien. Soit vous devenez riche, soit vous
n'obtenez rien. Dans un startup, si vous misez sur la mauvaise technologie,
vos concurrents vous écraseront.

Robert et moi connaissions bien Lisp, et nous ne pouvions voir aucune raison
de ne pas faire confiance à notre instinct et de n'aller pas avec Lisp. On
savait que tous les autres écrivaient leurs logiciels en C++ et Perl. Mais
on savait aussi que ça ne signifiait rien. Si vous choisissez la technologie
de cette façon, vous utiliseriez Windows. Quand on choisit la technologie,
il faut ignorer ce que les autres font et considérer seulement ce qui
fonctionnera le mieux.

C'est particulièrement vrai dans les startups. Dans une grande entreprise on
peut faire ce que les autres grandes entreprises font. Mais un startup ne
peut pas faire ce que les autres startups font. Je ne crois pas que beaucoup
de gens s'en rendent compte, même dans les startups.

Le grande entreprise moyenne grandit d'environ 10% par an. Donc si vous
dirigez une grande entreprise et faites tout comme une grande entreprise
moyenne le fait, vous pouvez vous attendre à faire aussi bien que le grande
entreprise moyenne—c'est-à-dire à grandir par d'environ 10% par an.

Bien sûr, la même chose arrivera si vous dirigez un startup. Si vous faites
tout comme un startup moyen, vous pouvez anticiper performance moyenne. Le
problème est, la performance moyenne signifie que vous serez mets en
faillite. Le taux de survie pour startups est beaucoup moins de cinquante
pourcent. Ça veut dire que si vous dirigez un startup, vous ferriez mieux de
faire quelque chose de bizarre. Sinon, vous avez des problèmes.

En 1995, nous savions quelque chose que je ne crois pas que nos concurrents
comprenaient, et peu comprennent même maintenant: quand vous écrivez
logiciel qui ne va fonctionner que sur vos propres serveurs, vous pouvez
utiliser un langage de programmation de votre choix. Quand vous écrivez
logiciel de bureau, il y a un fort biais pour l'écrire en le même langage
que le système d'exploitation. Il y a dix ans, écrire des applications
signifiait écrire des applications en C. Mais avec un logiciel basé sur le
Web, surtout si vous avez code source du langage et du système
d'exploitation, vous pouvez utiliser un langage de votre choix.

Cette nouvelle liberté est cependant une arme à double tranchant. Maintenant
que vous pouvez utiliser n'importe quel langage, vous devez déterminer
lequel utiliser. Les entreprises qui essayent de prétendre que rien n'a
changé risquent de trouver que leurs concurrents ne le pensent pas.

Si vous pouvez utiliser n'importe quel langage, quel langage vous utilisez?
Nous avions choisi Lisp. D'un côté, c'était évident que développement rapide
serait important sur ce marché. Nous tous partions de zéro, ainsi, une
entreprise qui pourrait obtenir de nouvelles fonctionnalités avant ses
concurrents aurait un gros avantage. On sait que Lisp était un langage
vraiment bien pour écrire logiciel vite, et les applications basés sur des
serveurs amplifient l'effet de développement rapide car vous pouvez publier
un logiciel la minute il est fait.

Si les autres entreprises n'utilisaient pas Lisp, tant mieux. Cela pourrait
nous donner un avantage technologique, et on avait besoin de toute aide
qu'on pouvait obtenir. Quand on a lancé Viaweb, on n'a aucune expérience en
affaires. On ne sait rien à propos de marketing, ou embouche, ou collecte de
fonds, ou obtention de clients. Aucun de nous n'avait même jamais eu ce que
vous appelleriez un travail vrai. La seule chose dans laquelle nous étions
bons était l'écriture de logiciels. On espérait que ça nous sauverait. Tout
avantage que nous pourrions obtenir dans le département de logiciel, nous
prendrions.

Donc, vous pourriez dire que Lisp était une expérience. Note hypothèse était
que si on écrivait notre logiciel en Lisp, on pourrait obtenir des
fonctionnalités plus rapidement que nos concurrents et faire des choses
qu'ils ne pouvaient pas faire.
