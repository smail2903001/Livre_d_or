## Livre d'or

-on aura une page avec un formulaire - Un champs pour le nom d'utilisateur - Un Champs message - Un bouton
(le formulaire devra etre valide et on n'acceptera pas les pseudo de moins de 3 caracteres ni les messages de moins de 10 caracteres)
-on creera un fichier "messages" qui contiendra un message par ligne
(on utilisera serialize et un tableau ['username'=>'...',message'=>'...', 'date'=> []] )
-pour "serialiser" les messages on utilisera les fonctions json_encode(tableau) et json_decode(tableau,true)
-La page devra afficher tous les messages sous le formulaire formate de la maniere suivante

<p> 
    <strong>Pesudo</strong> <em> le 03/12/20009 a 12h00 </em> <br> Le message
</p>
(les sauts de lignes devront etre conserves n12br)

## Restrinction

- Utiliser une classe pour representer un Message,
  -new Message(string $username, string $message, DateTime $date = null)
    -isValid(): bool
    -getErrors() :array
    -toHTML(): string 
    -toJSON(): string 
    -Message::fromJSON(string):Message
-Utiliser une classe pour representer le livre d'or 
    -new GuestBook($fichier)
  -addMessage(Message $message)
  -getMessage():array
