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


Routeur 

j'allume le routeur 
enable
conf t
interface gigabitethernet 0/0
no shutdown
exit

 créer la passerelle du vlan 10 ( comptabilité)

 interface gigabitethernet 0/0.10
 encapsulation dot1Q 10
 ip address 192.168.10.1 255.255.255.0
 exit


 créer la passerelle du vlan 20 ( Direction)

 interface gigabitethernet 0/0.20
 encapsulation dot1Q 20
 ip address 192.168.20.1 255.255.255.0
 end
 write








 

