# TP-vlan---Router-on-a-stick

suite du TP vlan mode trunk

objectif:le But d'ajouter le routeur est de permettre à des réseaux différents de communiquer entre eux tout en restant séparés. ici Vlan 10 et Vlan 20 pourront communiquer même séparer.


le switch sépare , le routeur connecte.



j'ai configuré le commutateur afin que les trfics de vlan 10 et vlan 20 puisse être envoyer au routeur.

enable
configure terminal
interface fastethernet 0/24
switchport mode trunk
end
write

