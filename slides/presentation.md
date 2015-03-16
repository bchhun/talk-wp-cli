# ./wp-cli 

## a.k.a. Automatiser nos projets Wordpress

---

# ./wp-cli o_O ?

## <span style="color:red">W</span>ord<span style="color:red">p</span>ress <span style="color:red">C</span>ommand <span style="color:red">L</span>ine <span style="color:red">I</span>nterface

## Presenter Notes

Un outil de gestion en ligne de commande de vos instances Wordpress

---

# ./wp-cli ?

## Pourquoi l'utiliser ?

## Presenter Notes

* Automatisation
* Réutilisation

---

# Installation

## Sous *nix,

	$ curl -O \
		https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
	$ chmod +x wp-cli.phar
	$ sudo mv wp-cli.phar /usr/local/bin/wp

## Sous windows ?

Utilisez une VM linux :)

---

# C'est bien beau tout ça, mais on veut du concret !

---

# Installer Wordpress et créer un site

	$ wp core download
	$ wp core config --dbname=test --dbuser=test \
		--dbpass=test
	$ wp core install --url=localhost:8000 \
		--title="un titre" \
		--admin_user=admin --admin_password=admin \
		--admin_email=votre@courriel.com
---

# Travailler sur un nouveau thème

	$ wp scaffold _s test --activate \
		--theme_name="test de wp cli" \
		--author="Bernard Chhun"

---

# Effectuer une mise à jour du core de Wordpress

	$ wp core update

---

# Installer/Désactiver des modules

	$ wp plugin list
	$ wp plugin deactivate hello
	$ wp plugin install wp-super-cache
	$ wp plugin activate wp-super-cache

---

# Créer des plugins

	$ wp scaffold plugin test \
		--plugin_name="test wp cli" \
		--activate

---

# Ajouter des usagers/groupes

	$ wp user create bob bob@example.com --role=author
	$ wp user add-role bob administrator

---

# Créer du contenus (page, billet, menus, etc...)

	$ wp post generate --count=10 --post_type=page
	$ wp post list --post_type=page
	$ wp menu list
	$ wp menu create "un menu" 
	$ wp menu item add-post un-menu 3

---

# Rechercher/remplacer des chaînes de caractères dans la base de données

	$ wp search-replace --url=example.com \
		example.local \
		example.com

---

# Liste complète des commandes disponibles

http://wp-cli.org/commands/

---

# Merci !

### Compte Twitter: @SFLinux, @bechhun

https://carrieres.savoirfairelinux.com/
