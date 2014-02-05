# Didaxo Custom

## Installazione

* Clonare la cartella del plugin nella cartella plugins e denominarla didaxo-custom

* Attivare il plugin

## Configurazione Wordpress

Il plugin come ora costruito funziona se sono presenti le seguenti condizioni

#### Custom Fields

Devono essere settati i seguenti custom fields ( qui indicati nel formato [post_type] id [type] )

* [Resource] video [string]
* [Resource] video_hd_url [string]
* [Resource] video_sd_url [string]
* [Resource] video_mobile_url [string]
* [Resource] video_hls_url [string]
* [Level] timer_start [string]
* [Level] timer_end [string]


Gli attributi riguardanti gli url singoli non sono utilizzati nella verisone Vimeo ma lo saranno per forza nella versione MediaElements. Il tempo di inizio e fine di ogni singolo sottolivello deve essere settato nella forma mm:ss


#### Gerarchia di livelli

L'organizzazione dei livelli deve essere del tipo

Livello 1 {
	Livello 1 - Part 1,
	Livello 2 - Part 2,
	...
}


Livello 2 {
	Livello 2 - Part 1,
	Livello 2 - Part 2,
	...
}

come definita dallo scambio di documenti con Carlo. Per iniziare un livello, andare direttamente alla pagina corrispondete al livello padre. Lì comparirà il player.

#### Impostazione TrainUp Test

Ricrodarsi di impostare la percentuale corretta per fare in modo che l'utente possa passare il test rispondendo correttamente ad una sola domanda. E' importante inoltre settare la proprietà resit del test a -1, cosicchè si possa far provare all'utnete più volte un test.

#### Librerie JS

L'attuale implementazione è con librerie Vimeo. 

* Impostare l'id di un video pubblico per il test provvisorio con Vimeo, fino alla risoluzione (se necessaria) di un bug che ne impedisce il playe via API una volta inserita la password
