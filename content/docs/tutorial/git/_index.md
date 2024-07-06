---
weight: 202
title: "Git"
---

# Guida Completa a Git

{{< buymecoffee>}}

## Introduzione

In questa guida, esploreremo un caso reale semplificato per analizzare ogni comando di Git e GitLab. Gli strumenti principali utilizzati saranno **Git** e **GitLab**.

## Creare un Nuovo Progetto su GitLab

1. Accedi a [GitLab](https://gitlab.com/dashboard/projects).
2. Crea un nuovo progetto chiamato `EsempioGit` con visibilità `public`.

---

## Clonare il Progetto su un Computer Locale

Dopo aver creato il progetto, scaricalo in locale posizionandoti nella cartella di riferimento ed eseguendo il comando:
```sh
git clone <url-del-progetto>
```

- **`git clone <url-del-progetto>`**: Questo comando crea una copia locale del repository remoto specificato dall'URL.

---

## Creare un File Vuoto

1. Una volta clonato il progetto, noterai che si è creata una cartella con lo stesso nome del progetto remoto.
2. Spostati all'interno della cartella e noterai che il terminale visualizza `(master)` accanto al prompt.

Per creare un file vuoto:
```sh
touch ReadMe.md
ls
```

- **`touch ReadMe.md`**: Questo comando crea un file vuoto chiamato `ReadMe.md`.
- **`ls`**: Questo comando elenca i file presenti nella directory corrente. Dovresti vedere il file `ReadMe.md` appena creato.

Il file `ReadMe.md` conterrà le istruzioni del progetto.

---

## Aggiungere il File al Progetto

1. Prepara le modifiche della cartella corrente:
    ```sh
    git status
    ```
    - **`git status`**: Questo comando mostra lo stato dei file nel repository. Indica quali file sono stati modificati, aggiunti o eliminati.

    ```sh
    git add .
    ```
    - **`git add .`**: Questo comando aggiunge tutte le modifiche (nuovi file, modifiche ai file esistenti e eliminazioni) all'area di staging, preparandole per il commit.

    ```sh
    git status
    ```
    - Verifica lo stato dei file per confermare che sono pronti per il commit. I file pronti saranno mostrati in verde.

    ```sh
    git reset .
    ```
    - **`git reset .`**: Questo comando rimuove tutte le modifiche dall'area di staging, permettendoti di apportare ulteriori modifiche prima di riprepararle.

    ```sh
    git status
    ```
    - Verifica lo stato dei file. Ora i file non saranno più nell'area di staging e verranno mostrati in rosso.

    ```sh
    git add .
    ```
    - Riprepara tutte le modifiche per il commit.

    ```sh
    git status
    ```
    - Verifica nuovamente lo stato dei file. I file pronti saranno mostrati in verde.

2. Crea una commit con una descrizione:
    ```sh
    git commit -m "Primo Commit"
    ```

    - **`git commit -m "Primo Commit"`**: Questo comando crea una snapshot delle modifiche preparate e le salva nel repository locale con il messaggio di commit "Primo Commit".

3. Invia tutto sul repository remoto:
    ```sh
    git push origin master
    ```

    - **`git push origin master`**: Questo comando invia le commit dal repository locale al repository remoto, aggiornando il branch `master`.

---

## Creare e Gestire Branch

1. Crea un nuovo branch per lavorare in autonomia:
    ```sh
    git branch
    ```
    - **`git branch`**: Questo comando elenca tutti i branch esistenti nel repository locale e indica il branch attualmente attivo.

    ```sh
    git branch -a
    ```
    - **`git branch -a`**: Questo comando elenca tutti i branch esistenti sia nel repository locale che remoto.

    ```sh
    git branch dev
    ```
    - **`git branch dev`**: Questo comando crea un nuovo branch chiamato `dev`.

    ```sh
    git branch -a
    ```
    - Verifica nuovamente tutti i branch per confermare la creazione del nuovo branch `dev`.

2. Spostati sul branch di riferimento:
    ```sh
    git checkout dev
    ```
    - **`git checkout dev`**: Questo comando cambia il branch attivo a `dev`.

    ```sh
    git checkout -b my_branch
    ```
    - **`git checkout -b my_branch`**: Questo comando crea e cambia il branch attivo a `my_branch`.

    ```sh
    git branch -d dev
    ```
    - **`git branch -d dev`**: Questo comando elimina il branch `dev`. Nota: non puoi eliminare il branch attualmente attivo.

Ora sei connesso al branch `(my_branch)`. Effettua delle modifiche al file:
```sh
nano ReadMe.md
```
- **`nano ReadMe.md`**: Questo comando apre il file `ReadMe.md` con l'editor di testo `nano`.

Scrivi:
```markdown
# ReadMe
In questo file si scrive qualcosa dal my_branch
```
Salva con `CTRL + O` e esci con `CTRL + X`.

3. Visualizza il contenuto del file:
    ```sh
    cat ReadMe.md
    ```

    - **`cat ReadMe.md`**: Questo comando visualizza il contenuto del file `ReadMe.md`.

4. Prepara il file, effettua la commit e invia le modifiche:
    ```sh
    git add .
    ```
    - Aggiungi tutte le modifiche all'area di staging.

    ```sh
    git commit -m "Cambiato il contenuto del file dal my_branch"
    ```

    - Crea una commit con il messaggio "Cambiato il contenuto del file dal my_branch".

    ```sh
    git push origin my_branch
    ```

    - Invia le modifiche al repository remoto nel branch `my_branch`.

Ricarica la pagina di GitLab per vedere i branch e le modifiche.

---

## Unire Branch

1. Unisci `my_branch` con `master`:
    ```sh
    git checkout master
    ```
    - Cambia il branch attivo a `master`.

    ```sh
    git pull origin master
    ```
    - **`git pull origin master`**: Questo comando aggiorna il branch locale `master` con le modifiche dal repository remoto.

    ```sh
    git merge my_branch
    ```
    - **`git merge my_branch`**: Questo comando unisce le modifiche del branch `my_branch` nel branch `master`.

    ```sh
    git push origin master
    ```
    - Invia le modifiche unite al repository remoto.

    ```sh
    git branch -d my_branch
    ```
    - Elimina il branch `my_branch`.

Ora il branch `master` include tutte le modifiche.

---

## Gestione dei Conflitti

1. Crea due branch distinti:
    ```sh
    git branch dev
    ```
    - Crea un branch chiamato `dev`.

    ```sh
    git branch my_branch
    ```
    - Crea un branch chiamato `my_branch`.

2. Modifica la stessa riga in entrambi i branch:
    ```sh
    git checkout dev
    ```
    - Cambia il branch attivo a `dev`.

    ```sh
    nano ReadMe.md
    ```
    - Apri il file `ReadMe.md` con `nano` e scrivi:
    ```markdown
    # ReadMe
    In questo file si scrive qualcosa dal Dev
    ```
    Salva e chiudi `nano`.

    ```sh
    git add .
    git commit -m "Modificato il file da Dev"
    git push origin dev
    ```

    - Prepara le modifiche, crea una commit e invia al repository remoto.

    ```sh
    git checkout my_branch
    ```
    - Cambia il branch attivo a `my_branch`.

    ```sh
    nano ReadMe.md
    ```
    - Apri il file `ReadMe.md` con `nano` e scrivi:
    ```markdown
    # ReadMe
    In questo file si RI - scrive qualcosa dal MyBranch
    ```
    Salva e chiudi `nano`.

    ```sh
    git add .
    git commit -m "Modificato il file da MyBranch"
    git push origin my_branch
    ```

    - Prepara le modifiche, crea una commit e invia al repository remoto.

3. Effettua la merge dei branch:
    ```sh
    git checkout master
    git pull origin master
    git merge dev
    git push origin master
    git branch -d dev
    ```

    - Cambia il branch attivo a `master`, aggiorna `master` con le modifiche dal repository remoto, unisci `dev` a `master`, invia le modifiche e elimina il branch `dev`.

    ```sh
    git checkout master
    git pull origin master
    git merge my_branch
    ```

    - Cambia il branch attivo a `master`, aggiorna `master` con le modifiche dal repository remoto e unisci `my_branch` a `master`.

Se ci

 sono conflitti, Git lo segnalerà. Apri il file con `nano` e risolvi il conflitto:
```markdown
# ReadMe
<<<<<<< HEAD
In questo file si scrive qualcosa dal Dev
=======
In questo file si Ri - scrive qualcosa dal MyBranch
>>>>>>> my_branch
```
Modifica il file come desiderato, salva e chiudi `nano`.

4. Prepara le modifiche, effettua la commit e pubblica:
    ```sh
    git add .
    git commit -m "Merge con Conflitto"
    git push origin master
    git branch -d my_branch
    ```

    - Prepara le modifiche, crea una commit con il messaggio "Merge con Conflitto", invia le modifiche al repository remoto e elimina il branch `my_branch`.

---

## Eliminare Branch Remoti

Quando hai finito di usare un branch, è buona norma eliminarlo per evitare confusione:
```sh
git branch -a
```
- Elenca tutti i branch esistenti sia nel repository locale che remoto.

```sh
git push origin --delete dev
```
- **`git push origin --delete dev`**: Questo comando elimina il branch `dev` dal repository remoto.

```sh
git push origin --delete my_branch
```
- Elimina il branch `my_branch` dal repository remoto.

In questo modo rimarrà solo il branch `master`.

---

{{< buymecoffee>}}
