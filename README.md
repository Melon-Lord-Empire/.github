# Introduction

README écrit pour l'organisation MelonLord. Dans ce README, je vais détailler l'idée générale des repositories, les projets qui y seront créés, et y placer les liens utiles pour vous orienter vers ce qui peut vous intéresser.

Cette organisation a été créée pour regrouper l'intégralité de mes projets réalisés via mon serveur dédié.
Ce serveur est un serveur Proxmox loué chez OVH, possédant 32 Go de RAM, 8 To de stockage, et 12 cœurs exploitables.

---

## Proxmox

### Configuration initiale

#### Réseau
- LAN
- DNS
- VPN
- Redirection de port
- DMZ

#### Stockage
*(J'aimerais bien avoir quelque chose à y faire, mais je n'ai pas encore de NAS.)*

---

### Infrastructure

#### Portfolio
- VMs Portfolio
- AutoSendMail

#### Certificate Training
- RHCSA

#### Test VM
- Environnement de test OS à interface graphique

---

## Présentation générale

L'objectif est de disposer d'un environnement polyvalent répondant à trois besoins initiaux : tester de nouvelles solutions, auto-héberger mes interfaces, et m'entraîner aux certifications — en commençant par la RHCSA, avec l'ambition de poursuivre vers Docker, Kubernetes, et d'autres.

Le réseau local doit donc répondre à ces besoins. Pour cela, j'ai décidé d'utiliser SDN et un script pour la conception du réseau, ce qui permet d'alléger au maximum cette tâche et d'économiser un maximum de ressources.

Le DNS est géré par un conteneur LXC AdGuard, principalement utilisé pour la redirection DNS, mais auquel je trouverai certainement d'autres utilités.

Le VPN retenu est WireGuard : léger mais efficace, il répond très bien à la demande et fournit une IP privée à chaque utilisateur. J'aimerais exploiter cet élément davantage dans un projet futur.

Une DMZ a été testée ; je compte utiliser le nom de domaine qui y est déjà lié pour héberger mon portfolio et permettre un accès public. Il faudra cependant bien configurer le Nginx qui y est associé.

Le stockage est déjà vaste, ce qui me laisse de la marge au niveau des machines virtuelles. J'aimerais cependant disposer d'un NAS afin de pouvoir tester des pratiques présentes uniquement dans de grosses infrastructures : sauvegardes, rollbacks, et fonctionnalités associées à Proxmox. Le coût et l'entretien restent mes seuls freins.

---

## Infrastructure visée

L'infrastructure visée est polyvalente à tous les niveaux. Je souhaite disposer de plusieurs environnements distincts :

**Pool personnelle** — Hébergement de mon portfolio et du projet AutoSendMail, un projet d'automatisation d'envoi de mail.

**Pool certifications** — Dédié à l'entraînement pour les certifications. La RHCSA est un début, mais j'aimerais à terme être certifié sur Debian et Red Hat principalement. Ces certifications me seront utiles lorsque j'utiliserai les distributions qui en sont dérivées. Crux Linux pourrait être une bonne étape pour apprendre à maîtriser la philosophie d'Arch Linux.

**Pool Test VM** — Environnement permettant de tester différents bureaux Linux. Chacun a ses particularités et constitue une alternative sérieuse à Windows. J'aimerais passer mon ordinateur personnel en full Linux, mais je n'ai pas encore arrêté mon choix sur une distribution. Je vais donc créer plusieurs machines virtuelles à partir d'une sauvegarde de base incluant les applications et logiciels que j'utilise, afin de tester l'environnement aussi bien dans un contexte de travail que de divertissement.

---

## Compétences visées

Je n'ai que peu de compétences en développement pour l'instant, mais j'aimerais apprendre à coder et scripter, notamment en Bash, Python, Ansible, et en langages de bases de données. Je ne suis pas particulièrement attiré par la création d'interfaces graphiques, donc très peu orienté HTML, CSS ou Node.js — cependant, j'aimerais en maîtriser les bases pour créer certaines interfaces dans le cadre de mes automatisations.
