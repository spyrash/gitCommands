# Lista dei comandi git più utili

## clone with ssh: 
 - copia il link ssh presente sul repository,  git clone "link" e copia il repository
 -"ls -la" per vedere tutti i file anche quelli nascosti nella cartella
## git status:
 - mostra tutti i file che sono stati modificati,creati o modificati.
## git add:
  - aggiunge allo stash i file modificati presenti in git status cosi che le modifiche siano considerate.
  - git add (nome file) oppure "." per all file
## git commit:
  - "-m "titolo commit" -m "messaggio commit"
  - am "titolo commit" con am faccio add e commit in un singolo comando ma solo per file modificati non creati.
 ## sshkeys:
  -"ssh-keygen -t rsa -b 4096 -c "githubemailaddress#real"
  - -t rsa => tipo di criptazione
  - -b 4096 => quanto è forte
  - -C "" => l'email address.
##  step successivi:
    - ti dovrebbe dire dove sta andando a salvare la key, di solito /Users/utente/.ssh/id_rsa
    - si può rinominare l'ultimo file ad esempio al posto di id_rsa => testkey
    - ti chiederà anche una passphrase che si può lasciare vuota per quella chiave
    - ls | grep testkey => cerchera il file "testkey" nel pc
    - crerà testkkey.pub quella pubblica, quella senza .pub è quella privata da non condividere
    - copiare il contenuto di testkey.pub e incollarlo in ssh keys nel github personale.
 ## git push :
   - git push origin master ( oppure si setta un branch di default per fare solo git push) 
   - git push -u origin master per settarlo di default
   - se il branch è appena creato si può settare un upbreanch con "git push --set-upstream origin "nomebranch"" o al posto di "--set-upstream" usare il        solito comando -u
 ## git init :
   - inizializza un git repository nella posizione in cui ti trovi ( possibilmente una cartella appena creata)
   - questo git non potrà pushare poichè non collegato a un repository remote su github
   - "git remote add origin "link per repository" per collegare il git
   - "git remote -v" per vedere ogni repository collegato a questo repo
  ## git branch : 
    - per vedere in quale branch si è (quale branch si è fatto il checkout) e quanit ne esistono
  ## git checkout :
    - git checkout -b(per creare nuovi branch usare -b) "nomebranch"(ad esempio: SIFERMANT-9110)
    - git checkout (nome branch)
  ## git diff :
    - mostra le differenze con il codice, lo stesso che si vede nei merge e commit di github
    - git diff "branch con cui vedere differenze"
    - preferisco git status
  ## pull request:
    - in master fare git pull "nomebranch da mergare in master"
    - oppure nel branch che si vuole pushare in master, prima di fare il passo precedente fare git merge master
  ## undo commit :
    - git reset HEAD(head è l'ultimo commit)
    - git reset HEAD~1 (head ora punta 1 commit indietro rispetto all'ultimo per cui cosi facendo la testa punterà ancora all'ultimo commit e quelli           selezionati con il comando reset sono tutti eliminati
  ## git log :
    - si vedranno tutti i commit fatti con ordine cronologico fatto, potendo copiare il commit hash number e usare il comando reset usando quel codice        per andare a resettare tutti i commit al quel commit selezionato.
  ## git rebase -i HEAD~n
    - fa partire un rebase interattivo da n commit indietro, nell'editor da terminale si possono eseguire varie operazioni: squash, edit sono le più quotate
    - se volete editare e aggiungere modifiche all'ultimo commit pushato fare edit del commit, modificare i file, git add, git commit --amend, e git rebase --continue, seguito da git push -f (attenzione a quest'ultima parte)
  ## git rebase -i origin/branch
    - fai un rebase vero e proprio rispetto al branch "padre" cosi da far partire i tuoi commit dopo l'ultimo pull senza creare commit di merge conflict
    - una volta sistemati i conflitti vare git add dei vari file risolti, e git rebase --continue
