# mongoShell Syntax
    
## utils
    
    cls 
    help
    help admin
    ls()
    pwd()
    
## databases 

Afficher les bases de données:

    show dbs 
    
Créer une base de donnée 'testdb'   

    use testdb
    
Afficher la base de donnée courante

    db 

Supprimer une base de donnée
    
    db.dropDatabase()


## collections / documents (table)

Créer une collection (table)

    db.users.insertOne({ name: "jean"})
    
Afficher les collections

    show collections 

Afficher le contenu d'une collection 
    
    db.users.find({})
