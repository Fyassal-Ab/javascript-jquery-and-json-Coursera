# Utiliser PHP 8.2 avec Apache
FROM php:8.2-apache

# Installer les extensions PDO et MySQL
RUN docker-php-ext-install pdo pdo_mysql mysqli

# Copier tous les fichiers PHP dans le dossier web
COPY . /var/www/html/

# Définir index.php comme page d'accueil par défaut
RUN echo "DirectoryIndex index.php" >> /etc/apache2/apache2.conf

# Définir les permissions correctes
RUN chown -R www-data:www-data /var/www/html/ && chmod -R 755 /var/www/html/

# Exposer le port 80 (Apache)
EXPOSE 80
