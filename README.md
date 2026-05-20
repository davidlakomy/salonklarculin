# Beautify By Klára - Webové stránky

Webová prezentace pro kosmetický salon **Beautify By Klára** v Havířově.

Doména: beautifybyklara.cz
Adresa: Mickiewiczova 548/1a, 736 01 Havířov-Město
Telefon: +420 730 553 590

## Struktura souborů

```
.
├── index.html              hlavní stránka
├── README.md               tento návod
├── CNAME                   konfigurace pro GitHub Pages
├── favicon.ico             ikona webu
└── images/                 všechny obrázky
```

## Jak web zveřejnit (krok za krokem)

### Část 1: GitHub Pages

1. Jdi na github.com a přihlas se (nebo si vytvoř účet zdarma)
2. Vpravo nahoře klikni na "+" a vyber **New repository**
3. Pojmenuj repo třeba `beautifybyklara-web`
4. Nastav repo jako **Public** (musí být veřejné pro free GitHub Pages)
5. Klikni **Create repository**
6. Na další stránce klikni **uploading an existing file**
7. Přetáhni do okna **celý obsah složky** (index.html, README.md, CNAME, favicon.ico, složku images/)
8. Dole klikni **Commit changes**
9. Jdi do **Settings** (nahoře v repu)
10. V levém menu klikni **Pages**
11. V "Source" vyber **Deploy from a branch**, pak větev **main** a **/(root)**, ulož
12. Web bude do pár minut dostupný na adrese `https://TVOJEUSERNAME.github.io/beautifybyklara-web/`

### Část 2: Připojení domény z Wedos

1. Přihlas se do administrace Wedos: client.wedos.com
2. V levém menu vyber **Domény**, klikni na `beautifybyklara.cz`
3. Klikni na **DNS záznamy** (nebo "DNS servery > Editace DNS")
4. Smaž všechny existující A a CNAME záznamy pro doménu (kromě MX záznamů pokud používáš email)
5. Přidej 4 A záznamy (jeden po druhém):

   Typ: A, Název: @, Hodnota: 185.199.108.153, TTL: 1800
   Typ: A, Název: @, Hodnota: 185.199.109.153, TTL: 1800
   Typ: A, Název: @, Hodnota: 185.199.110.153, TTL: 1800
   Typ: A, Název: @, Hodnota: 185.199.111.153, TTL: 1800

6. Přidej CNAME záznam pro www:

   Typ: CNAME, Název: www, Hodnota: TVOJEUSERNAME.github.io.

   (za github.io musí být tečka na konci)

7. Ulož změny

### Část 3: Aktivace domény na GitHubu

1. Vrať se na GitHub do **Settings > Pages** ve svém repu
2. V poli **Custom domain** napiš `beautifybyklara.cz` a ulož
3. Počkej cca 5 až 60 minut (max 24h) na propagaci DNS
4. Jakmile GitHub zaškrtne zelenou fajfku u domény, zaškrtni **Enforce HTTPS**
5. Hotovo, web běží na https://beautifybyklara.cz

## Úprava obsahu webu

- Ceny ošetření: sekce treatment-card v index.html
- Ceník (obočí, řasy, depilace): sekce price-table v index.html
- Texty: všechny jsou přímo v index.html
- Obrázky: nahraď soubory ve složce images/, zachovej názvy

## Změny po publikování

Když chceš něco upravit:
1. Jdi na github.com do svého repa
2. Klikni na index.html
3. Klikni na tužku (vpravo nahoře nad obsahem)
4. Uprav text
5. Dole klikni Commit changes
6. Změny se projeví do pár minut na webu

## Technické info

- Čistý HTML5 + CSS3 + minimum JS, žádné dependencies
- Fonty: Pinyon Script, Montserrat (z Google Fonts)
- Plně responzivní (mobil, tablet, PC)
- SSL/HTTPS zdarma od GitHubu (Let's Encrypt)
