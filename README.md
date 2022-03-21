# HCS-HomePage
Ajout d'une page d'accueil


Pour l'ajout d'une page d'accueil nous allons tout simplement crée une vue et modifier une vue

1. Ajouter les CSS/JS/... de votre template

2. Mettre en place un index.blade.php dans resources/views


3. Ajouter la vue ci-dessous dans routes/web.php
 Attention à bien l'ajouter en dessous de 
  
  ``  Auth::routes(['verify' => true]); ``
   
  `` Route::view('/', 'index'); /* Route pour l'accueil */ ``
  
   Maintenant nous allons modifier la route  du home
   
   Remplacer : 
    
    ``
      Route::get('/', [App\Http\Controllers\HomeController::class, 'render'])->name('home');
    ``
   Par
    ``
      Route::get('/home', [App\Http\Controllers\HomeController::class, 'render'])->name('home');
    ``
   Maintenant il ne vous reste plus qu'a modifier votre index.blade.php avec votre code HTML
   Attention votre bouton espace client ne doit pas être /login mais /home pour avoir une redirection permanante quand on est connecter
