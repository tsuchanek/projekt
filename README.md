# Alarm na kolo
![Alarm](https://im9.cz/iR/importprodukt-orig/008/0087ddcb215cc74a89fc4a97f06bac7a.jpg)


# Proč jsem si vybral tento projekt
Jelikož se hodně kradou kola a málokterá se najdou a vrátí se majiteli, tak jsem se rozhodl, že na ročníkový projekt udělám alarm pro kola. Jistěže to 100% nezábrání krádeži, ale nadruhou stranu to může některé zloděje odradit a o to jde ne? :)

#Jak bude alarm fungovat?
Když budu chtít alarm zapnout, tak zadám kód který si zvolím. No a když někdo bude chtít kolo ukrást, tak otřesový senzor pozná, že s kolem někdo hýbe a spustí se alarm (snad to případného zloděje odradí) do té doby, než ho vypnu kódem

#Co budu potřebovat za součástky
1) arduino nano - Pomocí Arduina můžete vyvíjet interaktivní předměty, získávat vstupy od různých spínačů, senzorů a ovládat například světla, motory,... 

![Arduino](https://www.arduino.cc/en/uploads/Main/ArduinoNanoFront_3_sm.jpg)

2) otřesové čidlo - Pomocí tohoto čidla arduino pozná, že se někdo pokouší ukrást kolo

![otřes](https://cdn-shop.adafruit.com/1200x900/1766-00.jpg)

3) nějaký bzučák - Pro zvuk alarmu a vystrašení zloděje

![bzučák](http://img.dxcdn.com/productimages/sku_138322_2.jpg)

4) tlačítka - pro odemknutí\zamknutí kola pomocí hesla

![klávenice](https://www.robotics.org.za/image/cache/data/Elec_Component/keypads/keypad04_000-500x500.jpg)

5) odpory - jsou potřeba proto, aby se nespálilo arduino
          - k tomuto projektu jsou potřeba 2,2k odpory
          
![odpory](http://litbimg5.rightinthebox.com/images/384x384/201310/pjkzaa1383016490412.jpg)

6) nepajivé pole - Slouží ke složení a vyzkoušení projektu bez pájení a poškození součástek v případě špatného zapojení.

![pole](http://www.pistek.eu/userfiles/image/breadboard.jpg)

#Schéma

![schema](https://cloud.githubusercontent.com/assets/14974344/19272023/43b74350-8fc7-11e6-8970-d8c2436af1d3.jpeg)

#Jak vyřešit aby arduino nevybilo baterku za den?
Arduino neustále provádí nějaké procesy a to vybíjí baterku. Timpádem bych musel často vyměňovat baterku za novou, proto jsem to musel vyřešit tím, že arduino zastaví všechny instrukce a pokračovat bude pouze, když bude potřeba(např.: když budu chtít zapnout alarm, nebo když čidlo zaznamená pohyb a bude potřeba spustit alarm).
Funguje to na principu, že když příjde proud na určitý pin, tak arduino začne provádět určité instrukce a po splnění se zase "vypne".
