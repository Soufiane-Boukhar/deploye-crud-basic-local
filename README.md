# Deployment crud basic local




## Travail a faire

Déployez le CRUD de base sur le serveur local

### Critére de validation

- Realiser lab crud basic apres deployement
- Utiliser server apache pour le deployment
- Migration base donne automatique

### Commande

```bash
Use illuminate\Support\Facades\Artisan

# Ajouter ce commande au AppServicesProviders sur function registre()

Artisan::call('migrate');

```

### Solution

[crud-basic](http://192.168.1.245/)


### Reference

[Medium](https://adeyomoladev.medium.com/how-to-deploy-a-laravel-app-using-apache-and-mysql-4910a07f9a0c)
