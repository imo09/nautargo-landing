# nautargo.com - versione 13

## Cosa c'è nella cartella

| File | A cosa serve |
|---|---|
| index.html | La pagina |
| favicon.ico | Icona nella scheda del browser |
| apple-touch-icon.png | Icona quando la pagina si salva sulla schermata Home di iPhone |
| icon-192.png, icon-512.png | Icone per Android e per i motori di ricerca |
| manifest.webmanifest | Nome e colori della pagina quando si salva sul telefono |
| og-image.png | Anteprima quando il link viene condiviso (WhatsApp, LinkedIn, ...) |
| robots.txt, sitemap.xml | Indicazioni per Google |

Rispetto alla versione 12 cambia solo `index.html`. Puoi caricare tutto lo stesso: è indifferente.

## Come caricarla su GitHub

1. Apri il repository del sito su github.com.
2. Premi `Add file` > `Upload files`.
3. Trascina tutti i file della cartella (non la cartella stessa).
4. In basso scrivi un messaggio, per esempio `nautargo v13`, e premi `Commit changes`.
5. Aspetta un paio di minuti, poi apri nautargo.com e ricarica con Ctrl + F5 (su telefono: chiudi e riapri la scheda).

I file con lo stesso nome vengono sostituiti, gli altri restano. Se nel repository c'è un file `CNAME`, lascialo dov'è: è quello che collega il dominio.

## Gli indirizzi delle app

In `index.html`, in cima allo script, c'è il blocco `CONFIG`:

```
seroWebAppUrl: 'https://sero.nautargo.com',
sestanteWebAppUrl: 'https://sestante.nautargo.com',
folioWebAppUrl: 'https://folio.nautargo.com',
lareWebAppUrl: 'https://lare.nautargo.com',
tecaWebAppUrl: 'https://teca.nautargo.com',
seroPlayUrl: '', sestantePlayUrl: '', folioPlayUrl: '', larePlayUrl: '', tecaPlayUrl: '',
```

- La pagina controlla da sola se ogni indirizzo risponde: se un'app non è ancora online (per esempio teca, finché non crei il sottodominio), i suoi bottoni Prova e Web app restano spenti con la scritta "presto". Quando l'app va online si accendono da soli.
- Quando un'app arriva sul Play Store, incolla il link tra gli apici del suo `PlayUrl` e il bottone si accende.

## Il modulo Contatti (Web3Forms)

I messaggi arrivano alla casella con cui hai registrato la chiave su web3forms.com. La chiave è già nel blocco `CONFIG` (`web3formsKey`).

Prima prova, appena il sito è online:

1. Apri nautargo.com, premi `Scrivici` nella prima schermata (o `Contatti` in alto a destra).
2. Scrivi nome, la tua email e un messaggio di prova. Gli invii fatti meno di 4 secondi dopo l'apertura del modulo vengono fermati: compare un avviso rosso che chiede di riprovare.
3. Deve comparire "Messaggio inviato" in verde (se l'invio fallisce compare un avviso rosso e il testo resta nei campi) e, entro un minuto, l'email nella tua casella (controlla anche lo spam la prima volta). Rispondendo a quella email rispondi direttamente a chi ti ha scritto.

Nel pannello di Web3Forms ti consiglio due cose:

- Accetta il DPA (l'accordo sul trattamento dei dati) se te lo propone: è quello citato nell'informativa privacy.
- Se il tuo piano lo permette, accorcia il tempo di conservazione dei messaggi. L'informativa oggi dice "al massimo 3 anni": se lo riduci, dimmelo e aggiorno il testo.

## Dopo la pubblicazione

1. Prova la pagina da telefono e da computer, in tutte e tre le lingue.
2. Premi Prova su ogni app: deve aprirsi il telefono con l'app dentro. Su computer, con + e - sotto il telefono cambi la dimensione.
3. Anteprima dei link: se WhatsApp o LinkedIn mostrano ancora l'immagine vecchia, è la loro memoria. Si aggiorna da sola in qualche giorno; per LinkedIn si forza da linkedin.com/post-inspector.
