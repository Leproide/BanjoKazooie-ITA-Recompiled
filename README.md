# Banjo-Kazooie – Traduzione italiana per Banjo: Recompiled

Traduzione italiana dei dialoghi di **Banjo-Kazooie** per [Banjo: Recompiled](https://github.com/BanjoRecomp/BanjoRecomp), nel formato del mod **DialogLoader** di ProxyBK.

I testi provengono dalla traduzione amatoriale [Banjo-Kazooie Traduzione Italiana](https://sites.google.com/site/banjokazooieita/download?authuser=0) di **Snorlite**, realizzata nell'estate 2015 e revisionata nell'estate 2016. Quella patch funziona solo sulla ROM PAL: i dialoghi sono stati estratti e associati agli ID dei testi della versione **NTSC-U 1.0**, usata da Banjo: Recompiled.

*English summary below.*

<img width="1920" height="1032" alt="immagine" src="https://github.com/user-attachments/assets/b2e4e862-acf7-46c7-acdd-2b24cd0efd12" />

## Contenuto

- 706 dialoghi tradotti
- Funziona con il dump NTSC-U 1.0 **originale e non modificato** (il controllo della ROM del recomp passa)
- Due varianti:

| Cartella | Accenti | Font aggiuntivo |
|---|---|---|
| `dialog/apostrofi` | `E'`, `PIU'`, `PUO'` | non serve |
| `dialog/accenti` | `È`, `Ù`, `Ò` reali | [Font Plus Latin1](https://thunderstore.io/c/banjo-recompiled/p/Krisp0o/Font_Plus_Latin1/) |

## Requisiti

1. [Banjo: Recompiled](https://github.com/BanjoRecomp/BanjoRecomp), versione recente, con il proprio dump NTSC-U 1.0
2. [Asset Expansion Pak](https://thunderstore.io/c/banjo-recompiled/p/Dario/Asset_Expansion_Pak/)
3. [DialogLoader](https://thunderstore.io/c/banjo-recompiled/p/ProxyBK/DialogLoader/)
4. Solo per la variante `accenti`: [Font Plus Latin1](https://thunderstore.io/c/banjo-recompiled/p/Krisp0o/Font_Plus_Latin1/)

## Installazione

1. Scarica **Asset Expansion Pak** e **DialogLoader** da Thunderstore ("Manual Download").
2. Avvia Banjo: Recompiled, apri il menu **Mods**, installa i due mod e verifica che siano attivi.
3. Nel menu **Mods** premi **Open Mods Folder**.
4. Copia nella cartella mods il contenuto di **una sola** variante: tutto quello che c'è dentro `dialog/apostrofi/` oppure dentro `dialog/accenti/`.
   Se usi lo zip della [release](../../releases), estrailo direttamente nella cartella mods.
   **Non** usare l'installer del gioco per i testi: non sono un mod `.nrm`, ma file di testo letti da DialogLoader.
5. Il risultato deve essere:
   ```
   mods/DialogLoader/dialog/italiano/0A0B.dialog
   mods/DialogLoader/dialog/italiano/0A0C.dialog
   ...
   ```
6. Inizia una nuova partita: l'introduzione di Gruntilda deve essere in italiano.

### Risoluzione problemi

- **Testi ancora in inglese:** controlla il percorso del punto 5 e che DialogLoader e Asset Expansion Pak siano attivi.
- **"No mods found" all'installazione:** stai installando lo zip dei testi dal menu Mods; va estratto a mano (punto 4).
- **Lettere strane al posto degli accenti:** stai usando la variante `accenti` senza Font Plus Latin1. Installa il font o passa alla variante `apostrofi`.
- **Verifica degli ID:** attivando *Debug Mode* nelle opzioni di DialogLoader, il gioco mostra l'ID del testo corrente; corrisponde al nome del file `.dialog`.

## Limitazioni note

- **Quiz di Grunty's Furnace Fun** (200 domande): sono già tradotti e inclusi nella cartella `quiz/`, ma DialogLoader non carica ancora i quiz, quindi in gioco restano in inglese. Vedi la sezione *Quiz*.
- Testo `0x102C`: escluso, contiene byte di controllo (`0x0A`/`0x0D`) che il formato di DialogLoader non può rappresentare.
- Titoli di coda, `0x0E8F` ("GRNN...") e `0x0C00` ("OOOOOOOF..."): in inglese.
- Scritte grafiche (texture e modelli): non incluse.

## Quiz

La cartella `quiz/` contiene le 200 domande tradotte, pronte per quando DialogLoader supporterà i quiz:

- `quiz/quiz_it.yaml`: tutte le domande in formato leggibile, raggruppate per ID asset NTSC-U (hex). Le lettere accentate sono scritte con l'apostrofo (`E'`, `PIU'`, `PUO'`), come nella variante `apostrofi`; `\xFD` indica un codice di controllo del gioco.
- `quiz/bin/XXXX.bin`: ogni domanda come asset binario decompresso nel formato NTSC-U, utilizzabile direttamente con `bk_recomp_aep_register_replacement`.

Quando il loader supporterà i quiz basterà convertirli nel formato richiesto; per ora **non vanno copiati** nella cartella mods.

## English summary

Italian dialogue translation for Banjo: Recompiled, provided as `.dialog` files for ProxyBK's DialogLoader. It works with an unmodified NTSC-U 1.0 ROM.
Install Asset Expansion Pak and DialogLoader, then copy **one** variant (`dialog/apostrofi` for the stock font, or `dialog/accenti` with Font Plus Latin1) into the recomp's mods folder so that you get `mods/DialogLoader/dialog/italiano/*.dialog`.
Quiz questions stay in English until DialogLoader supports quiz assets.

## Crediti

- **Traduzione italiana:** Snorlite, [Banjo-Kazooie Traduzione Italiana](https://sites.google.com/site/banjokazooieita/download?authuser=0) (estate 2015, revisione estate 2016)
- Ringraziamenti del progetto originale:
  - Miguel Rivera (PacoChan), creatore di Banjo-Kazooie Editor
  - SOLLAZZATORE, conversione della ROM tradotta per Wii U
  - Utenti di Pokémon Central Forum, aiuto con terminologia e dialoghi
- **DialogLoader:** ProxyBK
- **Asset Expansion Pak:** Dario
- **Font Plus Latin1:** Krisp0o
- **Porting su NTSC-U e formato DialogLoader:** https://github.com/Leproide

Questo repository non contiene ROM né file del gioco. Serve un dump personale della propria cartuccia.

## License

Struttura del repository, documentazione e strumenti di conversione: **GPL-3.0** (vedi [LICENSE](LICENSE)).
I testi tradotti appartengono al loro autore (Snorlite); per usi diversi da questo pacchetto fare riferimento al progetto originale.
Banjo-Kazooie è un marchio dei rispettivi proprietari.

## Author

https://github.com/Leproide
