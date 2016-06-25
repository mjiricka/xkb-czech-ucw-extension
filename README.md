# My extension of UCW keyboard layout

Extension of [UCW](http://log.or.cz/?p=31) keyboard layout via xkb system.
It adds many particularly Czech characters that are not present on traditional layouts.

Rest of the page is in Czech.


---


## Co to je

Chtěl jsem mít na klávesnici různé české znaky jako krátkou (neboli půlčtverčíkovou)
pomlčku, různé druhy českých uvozovek a další. Rozhodl jsem se proto rozšířit UCW layout,
který používám na psaní diakritiky, o další znaky.

Zde jsou všechny přidané tisknutelné znaky (chybí nedělitelná mezera a krátká mezera),
jejich mapování je popsáno v komentářích souboru `cz.diff`:

    § ™ ® π € ∞ – — ≠ ± « » ‹ › „ “ , ‘ …


## Instalace


### Záloha souboru s českými layouty

Protože budeme rozšiřovat systémový soubor, je vhodné si ten původní zazálohovat,
např. takto:

    sudo cp /usr/share/X11/xkb/symbols/cz /usr/share/X11/xkb/symbols/cz_backup

### Rozšíření xkb layoutu

Buď lze zkopírovat celý soubor:

    sudo cp cz /usr/share/X11/xkb/symbols/cz

nebo aplikovat patch:

    sudo patch /usr/share/X11/xkb/symbols/cz < cz.diff


### Nastavení layoutu

Osobně používám US layout, ze kterého přepínám na UCW layout pomocí klávesy
caps lock, což lze nastavit následujícím příkazem:

    setxkbmap us,cz -variant ,ucw -option grp:caps_switch


## Zdroje

 - http://log.or.cz/?p=31
 - http://xakru.com/cshack/
 - http://xpisar.wz.cz/xkb-cz-typo/

