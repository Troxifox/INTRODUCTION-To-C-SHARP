# INTRODUCTION-To-C#
Introduction :
L'objectif de cet ensemble d'exercices est de vous initier aux bases du développement C# MVC en utilisant Visual Studio Code.

Prérequis :
Assurez-vous d'avoir Visual Studio Code installé sur votre machine. Vous aurez également besoin du SDK .NET Core installé.

Étape 1 : Créez un nouveau projet C# MVC
1. Ouvrez Visual Studio Code et créez un nouveau dossier pour votre projet.
2. Ouvrez un terminal dans Visual Studio Code (Ctrl+`) et accédez au dossier du projet.
3. Exécutez la commande suivante pour créer un nouveau projet C# MVC :

```
dotnet new mvc
```

4. Ouvrez le dossier du projet dans Visual Studio Code.

Étape 2 : Explorez la structure du projet
1. Jetez un coup d'œil à la structure du projet dans le volet Explorateur situé à gauche de Visual Studio Code.
2. Familiarisez-vous avec les dossiers importants tels que Controllers, Views et Models.

Étape 3 : Exécutez l'application
1. Ouvrez le terminal intégré dans Visual Studio Code (Ctrl+`).
2. Accédez au répertoire du projet et exécutez la commande suivante pour démarrer l'application :

```
dotnet run
```

3. Ouvrez un navigateur Web et visitez l'URL fournie dans le terminal pour voir l'application en cours d'exécution.

Étape 4 : Créez un nouveau contrôleur et une vue
1. Dans le volet Explorateur, accédez au dossier Controllers.
2. Cliquez avec le bouton droit sur le dossier et sélectionnez "Nouveau fichier". Nommez le fichier "HomeController.cs".
3. Ajoutez une méthode d'action simple à HomeController :

```csharp
using Microsoft.AspNetCore.Mvc;

namespace VotreProjet.Controllers
{
    public class HomeController : Controller
    {
        public IActionResult Index()
        {
            return View();
        }
    }
}
```

4. Dans le volet Explorateur, accédez au dossier Views.
5. Cliquez avec le bouton droit sur le dossier et sélectionnez "Nouveau dossier". Nommez le dossier "Home".
6. Cliquez avec le bouton droit sur le dossier Home et sélectionnez "Nouveau fichier". Nommez le fichier "Index.cshtml".
7. Ajoutez un contenu HTML de base dans le fichier Index.cshtml :

```html
<h1>Bienvenue dans l'application MVC !</h1>
```

8. Enregistrez les modifications.

Étape 5 : Mettez à jour la configuration des routes
1. Ouvrez le fichier `Startup.cs` à la racine de votre projet.
2. Recherchez la méthode `Configure` et mettez à jour la configuration des routes pour inclure la route par défaut :

```csharp
app.UseEndpoints(endpoints =>
{
    endpoints.MapControllerRoute(
        name: "default",
        pattern: "{controller=Home}/{action=Index}/{id?}");
});
```

3. Enregistrez les modifications.

Étape 6 : Testez le nouveau contrôleur et la vue
1. Arrêtez l'application en cours d'exécution si elle est toujours active (Ctrl+C dans le terminal).
2. Exécutez à nouveau l'application à l'aide de la commande `dotnet run`.
3. Ouvrez un navigateur Web et visitez l'URL fournie dans le terminal.
4. Vous devriez voir le message "Bienvenue dans l'application MVC !" sur la page d'accueil.

Exercices :
Maintenant que vous avez configuré une application MVC de base, passons aux exercices :

Exercice 1 :
Créez un nouveau contrôleur nommé "UserController" avec une méthode d'action qui affiche une liste d'utilisateurs.

Exercice 2 :
Ajoutez une nouvelle vue à UserController qui affiche les détails d'un utilisateur spécifique.

Exercice 3 :
Créez un formulaire dans la vue UserController pour permettre aux utilisateurs de créer de nouveaux enregistrements d'utilisateurs.

Exercice 4 :
Implémentez la logique nécessaire dans UserController pour gérer les soumissions de formulaire et enregistrer de nouveaux enregistrements d'utilisateurs.

Exercice 5 :
Créez une nouvelle classe de modèle nommée "User" avec des propriétés telles que Name, Email et Age. Utilisez ce modèle dans votre UserController.

Exercice 6 :
Ajoutez une validation au formulaire de création d'utilisateur dans UserController pour vous assurer que les champs requis sont remplis et affichez des messages d'erreur appropriés.

Exercice 7 :
Implémentez la possibilité de modifier et de mettre à jour les enregistrements d'utilisateurs dans UserController.
