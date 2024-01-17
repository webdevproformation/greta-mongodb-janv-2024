# POO en PHP 

## Programmation Orientée Objet 

organiser votre projet via des objets (concepts)

```
Etudiant 
    nom
    prenom
    date_naissance

    traitement liés à ces propriétés (fonctions)
```


```php
class Note{
    public float $valeur ;
    public string $date ;
    private string $matiere ;
    protected string $formule ; 
    public function __construct( float $v , string $dt  ) { 
            // fonction magique 
            // exécute automatiquement lorsque l'on fait un new 
        $this->valeur = $v ;
        $this->date = $dt ; 
    }

    public function affichage(): string{
        return "{$this->valeur} points / 20"; 
    }
}

$n = new Note(10.5 , "janvier 2024") ; 
// new === $n->__construct(10.5 , "janvier 2024")
echo  $n->affichage(); // 10.5 / 20
```


```html
<p class="hello">comment allez vous ?</p>
```

## PDO PHP Data Objet

- class native de PHP, livré dans le langage PHP 
- tu peux écrire => `new PDO($dsn, $login, $password)` n'importe où dans ton code
    - vous allez mettre 3 valeurs dans les () de new PDO
    - dsn => database serveur network (adresse internet pour base de données)
        - mysql://host:localhost;dbname=votre_base;charset=utf8
    - login =>  (ceux qui sont écrit dans le fichier Vagrantfile)
    - password =>  (ceux qui sont écrit dans le fichier Vagrantfile)
-  $connexion = new PDO($dsn, $login, $password); 
- $connexion est un objet communiquer avec la bdd 
- $stmt = $connexion->query("SELECT * FROM ...."); 
- // query => requete / demande
- $tableauAssociatif = $stmt->fetchAll() // parcourir / rechercher 


// Swift => le langage natif pour iOS iphone
// Java / Kotlin => langage natif pour Android  

// React Native => js => librairie React Native => Swift / Java 