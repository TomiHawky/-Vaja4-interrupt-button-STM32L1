# -Vaja4-interrupt-button-STM32L1
  V Pinout % Configuraton pogledu glede na vašo razvojno ploščico ugotovite, ali lahko uporabite modro tipko za digitalni vhod kot interrupt (GPIO_EXT…). Če da, kateri pin je to? ____PA0____. Če ni, uporabite drugi ustrezni pin ___X___, ki ga boste prožili s pomočjo Pull-UP vezja.
 Zapišite naslov izhodnih pinov za zeleno in modro LED: _______PB7 zelena, PB6 modra_____.
 Znotraj te funkcije zapišite ukaz za vklop/izklop zelene LED (pomagajte si z metodo toggle, glej vaja0a). _______HAL_GPIO_TogglePin(GPIO,GPIO_PIN_6);________.
 Znotraj iste funkcije dodajte še zakasnitev, ki je potrebna, ko uporabimo mehanska tipkala/stikala:
for(uint32_t i=0; i<10000; i++);
Koliko znaša (v mili sekundah) zapisana zakasnitev, ki jo proizvede zanka for? __10000__.
V user code begin 3 - zanka while(1) - zapišite ukaz za utripanje modre LED (metoda toggle, glej vaja0a):
____HAL_GPIO_TogglePin(GPIOB,GPIO_PIN_6);_____.
 V to zanko dodajte ukaz za zakasnitev z funkcijo Delay iz knjižnice HAL, in sicer pol sekunde (glej vaja0a): ____HAL_Delay(500);____.
 Opazujte delovanje (utripanje modre LED). Kaj se zgodi, ko pritisnemo na modro tipko na STM32L1?
_________Nič modra LED utripa naprej_________.
 Ali pritisk na modro tipko vpliva na utripanje modre LED in zakaj?
 __________Ne ker je koda napisana tako da modra tipka nima vpliva na modro LED______.
