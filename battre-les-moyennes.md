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
