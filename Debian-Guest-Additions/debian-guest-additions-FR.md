# Installer les Guest Additions VirtualBox pour une Machine Virtuelle Debian

### Mise à jour du système

On met à jour le système :

```shell
apt update
apt dist-upgrade
```



On redémarre pour travailler sur le nouveau noyau installé (si nouveau noyau installé) :

```
reboot
```

---

### Installations des paquets nécessaires

```shell
apt install make gcc dkms linux-source linux-headers-$(uname -r)
```

---

### Installation des Guest Additions

On insère les Guest Additions depuis **Périphériques ==> Insérer l'image CD des Additions Invité**.



On monte le CD, on l'on se place dans son dossier puis on lance le script :

```shell
sudo mount /dev/cdrom /mnt
cd /mnt
./VBoxLinuxAddition.run
```



On finit par redémarrer la machine virtuelle.

```shell
reboot
```



On peut désormais activer **la taille d'écran automatique**, **le presse papier partagé** et **le glisser déposer**.

