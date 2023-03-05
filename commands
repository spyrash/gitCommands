# Lista dei comandi git più utili

"clone with ssh": 
 -copia il link ssh presente sul repository,  git clone "link" e copia il repository
 -"ls -la" per vedere tutti i file anche quelli nascosti nella cartella
"git status":
 -mostra tutti i file che sono stati modificati,creati o modificati.
"git add":
  -aggiunge allo stash i file modificati presenti in git status cosi che le modifiche siano considerate.
  -git add (nome file) oppure "." per all file
 "git commit":
  - "-m "titolo commit" -m "messaggio commit"
  - am "titolo commit" con am faccio add e commit in un singolo comando ma solo per file modificati non creati.
 "ssh keys":
  -"ssh-keygen -t rsa -b 4096 -c "githubemailaddress#real"
  - -t rsa => tipo di criptazione
  - -b 4096 => quanto è forte
  - -C "" => l'email address.
  step successivi:
    - ti dovrebbe dire dove sta andando a salvare la key, di solito /Users/utente/.ssh/id_rsa
    - si può rinominare l'ultimo file ad esempio al posto di id_rsa => testkey
    - ti chiederà anche una passphrase che si può lasciare vuota per quella chiave
    - ls | grep testkey => cerchera il file "testkey" nel pc
    - crerà testkkey.pub quella pubblica, quella senza .pub è quella privata da non condividere
    - copiare il contenuto di testkey.pub e incollarlo in ssh keys nel github personale.
