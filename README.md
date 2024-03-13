# Per iniziare

Scarica un web server https che utilizzerai per servire i contenuti della cartella server/uploads. Nel mio caso ho utilizzato [`nginx`](https://docs.nginx.com/). 

In seguito avrai bisogno di scaricare le dipendenze del progetto : 

```bash
# client/
npm install

# server/
npm install
```

# Adattamento codice

Se utilizzi un editor di testo come ad esempio vscode, sfrutta la funzione che ti permette di trovare/modificare parti di testo

```bash
cerca la stringa  [tuo_indirizzo_ip] e sostituiscila con l'indirizzo ip della tua macchina

# Eempio

src={avatar_path.startsWith('https') ? avatar_path : `https://[tuo_indirizzo_ip]/${avatar_path}`}

# diventerà :

src={avatar_path.startsWith('https') ? avatar_path : `https://192.168.1.2/${avatar_path}`}
```

## Configurazione

To create a production version of your app:

```bash
in server/.env configura la variabile DATABASE_URI con l'indirizzo di collegamento per il tuo database in mongodb
```

# Avvia i server

```bash
# client/
  npm run dev -- --host

# server/
  npm start

# nginx/
  nginx.exe
```

Una volta fatto ciò per testare la web app vai su https://[tuo_indirizzo_ip]:5173/ 

Per una migliore esperienza consiglio di visualizzare la pagina in modalità telefono dal browser.
