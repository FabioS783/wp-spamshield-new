# WP-SpamShield 🛡️

**WP-SpamShield** è un plugin antispam estremamente potente, invisibile e facile da usare per WordPress. Elimina completamente lo spam nei commenti, nei pingback/trackback e nei moduli di contatto (come *Contact Form 7* o *Gravity Forms*) senza mai infastidire i tuoi visitatori con CAPTCHA illeggibili o domande di sicurezza.

---

## ✨ Perché sceglierlo?

A differenza di molti altri plugin antispam che si basano solo su database o che forzano gli utenti umani a superare test noiosi (es. reCAPTCHA), WP-SpamShield utilizza un doppio livello di difesa "invisibile":
1. **Livello Javascript/Cookie:** Blocca i bot automatizzati (che spesso non eseguono JS o non gestiscono i cookie) tramite token temporanei.
2. **Livello Algoritmico Avanzato:** Esegue un'analisi intelligente in background sui dati inviati e sull'IP del mittente, senza alcun impatto sull'esperienza utente.

---

## 🚀 Nuove Funzionalità e Migliorie (Versione 2.x)

Questo plugin è stato ampiamente riscritto e modernizzato per garantire le massime prestazioni sulle moderne architetture WordPress.

* **⚡ Zero Impatto sulle Performance (Ottimizzazione WooCommerce):** Abbiamo rimosso i colli di bottiglia causati dall'apertura indiscriminata delle sessioni PHP native. Ora il backend del tuo sito e le operazioni WooCommerce risultano fluidi e veloci, poiché le sessioni vengono evitate durante le richieste AJAX e le operazioni di amministrazione.
* **🌐 Integrazione API StopForumSpam (Opzionale):** Puoi ora attivare un ulteriore strato di protezione che interroga in tempo reale (tramite API sicure di WordPress) il rinomato database di *StopForumSpam*. I bot già noti vengono bloccati istantaneamente e il numero di spammers intercettati viene comodamente mostrato in un counter dedicato sulla Dashboard.
* **✅ Compatibilità Totale con REST API e Pixel Facebook:** È stato introdotto un "bypass" intelligente per le API di sistema di WordPress (`/wp-json/`). Questo previene fastidiosi falsi positivi bloccando il tracciamento in background di plugin popolari come **PixelYourSite**.
* **🚀 Supporto Cache Avanzato (LiteSpeed, WP Rocket):** Il rilevamento dei plugin di cache è stato aggiornato per includere le soluzioni più moderne sul mercato. Questo garantisce che i token antispam non vengano invalidati dalle cache di pagina (eliminando i falsi positivi sulle registrazioni WooCommerce).
* **🧹 Interfaccia Pulita e Tradotta:** Il pannello di amministrazione è stato completamente tradotto in italiano. Sono stati rimossi vecchi widget promozionali, form di contatto legacy integrati non più necessari (in favore del supporto a CF7) e schermate di documentazione obsolete. Ora hai solo le opzioni che ti servono davvero.

---

## 📦 Installazione

Essendo questa una versione customizzata e potenziata:
1. Scarica i file del plugin in formato `.zip`.
2. Dal pannello di amministrazione di WordPress, vai su **Plugin > Aggiungi nuovo > Carica plugin**.
3. Seleziona il file zip e clicca su "Installa ora".
4. Clicca su **Attiva**.

In alternativa, puoi scompattare la cartella e caricarla tramite FTP all'interno della directory `/wp-content/plugins/`.

---

## ⚙️ Configurazione

Una volta attivato, vai su **Impostazioni > WP-SpamShield** nel menu laterale di WordPress.

* **Protezione "Zero Configuration":** Il plugin inizierà a bloccare lo spam non appena attivato, senza bisogno di impostazioni complesse.
* **StopForumSpam:** Puoi attivare la spunta su "Abilita StopForumSpam API" per potenziare l'algoritmo usando il database cloud.
* **Moduli Vari:** Le chiamate REST in background (come il Pixel di Meta) sono già escluse automaticamente. Se dovessi notare che un tuo form molto particolare viene bloccato (errore JS/Cookies), puoi sempre usare l'opzione "Disabilita antispam per moduli vari".
* **Dashboard Widget:** Vai nella bacheca iniziale di WordPress per vedere in tempo reale i contatori degli spam bloccati.

---

*Mantenuto e aggiornato per le versioni moderne di PHP e WordPress da Scott Allen & DF Staff.*
