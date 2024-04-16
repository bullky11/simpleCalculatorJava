 

Egyszerű Számológép Program Dokumentációja 

Bevezetés 

Az "Egyszerű Számológép" egy Java nyelven írt grafikus felhasználói felülettel rendelkező alkalmazás, amely lehetővé teszi egyszerű matematikai műveletek végrehajtását. A program a Swing keretrendszer segítségével készült, ami lehetővé teszi a felhasználóbarát és interaktív felület kialakítását. 

Funkciók 

Számok megjelenítése 

A program lehetővé teszi a felhasználó számok megjelenítését a számológép képernyőjén. A számokat gombok segítségével lehet beírni, és azok a képernyőn jelennek meg a felhasználó számára. 

Alapvető műveletek végrehajtása 

A program támogatja az alapvető matematikai műveletek végrehajtását, mint például összeadás, kivonás, szorzás és osztás. Ezeket a műveleteket a megfelelő gombokkal lehet aktiválni. 

Számítások végrehajtása 

Miután a felhasználó megadta az első és a második számot, valamint kiválasztotta a kívánt műveletet, a program végrehajtja a számításokat és megjeleníti az eredményt a képernyőn. 

Törlés funkció 

A program lehetővé teszi a felhasználó számára, hogy törölje a jelenlegi műveletet vagy a megjelenő eredményt, ha szükséges. 

Negatív számok kezelése 

A program lehetővé teszi a felhasználó számára, hogy negatív számokat állítson be és kezeljen a számítások során. 

Használati útmutató 

    Számok beírása: Használja a gombokat a számok beírásához a képernyőre. 

    Műveletek kiválasztása: Válassza ki az elvégzendő műveletet a megfelelő gomb segítségével (+, -, *, /). 

    Számítás elvégzése: Nyomja meg az "=" gombot a számítások végrehajtásához. 

    Eredmény megjelenítése: Az eredmény megjelenik a képernyőn. 

    Törlés: Ha szükséges, használja a "C" gombot az aktuális művelet vagy eredmény törléséhez. 

Telepítési útmutató 

    Töltsd le a Java Development Kit (JDK) legfrissebb verzióját és telepítsd a számítógépedre. 

    Töltsd le a forráskódot a GitHub repository-ból. 

    Nyisd meg a forráskódot egy Java fejlesztőkörnyezetben (pl. NetBeans, IntelliJ IDEA). 

    Fordítsd le és futtasd a programot a fejlesztőkörnyezetből. 

Rendszerkövetelmények 

    Java Development Kit (JDK) 8 vagy újabb verziója 

    Java Swing API-t támogató fejlesztőkörnyezet (pl. NetBeans, IntelliJ IDEA) 

Fejlesztői információk 

Az alkalmazást pozsm fejlesztette és az Apache 2.0 licenc alatt kiadta. A forráskód elérhető a GitHub repository-ban: . 

 

Hibabejelentés és támogatás 

 

Ha bármilyen hibát találsz az alkalmazásban, kérlek jelentsd azt a GitHub repository-ban, 

 

https://github.com/bullky11/simpleCalculatorJava.git  vagy lépj kapcsolatba a fejlesztővel az alábbi elérhetőségeken. 


                                                                  Hogyan készült 

Számok megjelenítése 

    0-9 számok gombjai: A számok megjelenítéséhez és hozzáadásához 10 különböző gombot készítettél el. Például: 

     

private void jBtn1ActionPerformed(java.awt.event.ActionEvent evt) {                                       
    String Enternumber = jtxtDisplay.getText() + jBtn1.getText(); 
    jtxtDisplay.setText(Enternumber); 
} 

    Ez a metódus hozzáadja a "1" számot a jelenlegi számológép képernyő tartalmához, amikor a "1" gombra kattint a felhasználó. 

Alapvető műveletek végrehajtása 

    Összeadás, kivonás, szorzás, osztás gombok: A műveletek végrehajtásához négy különböző gombot készítettél el, mindegyik a megfelelő műveletet hajtja végre. Például: 

java 

    private void jBtn11ActionPerformed(java.awt.event.ActionEvent evt) {                                        
        firstnum = Double.parseDouble(jtxtDisplay.getText()); 
        jtxtDisplay.setText(""); 
        operations = "+"; 
    } 
     

Ez a metódus beállítja az operations változót a "+" műveletre, és törli a jelenlegi képernyő tartalmát, hogy a felhasználó új számokat adhasson meg. 

Számítások végrehajtása 

    Egyenlőségjel (=) gomb: A számítások végrehajtásához és az eredmény megjelenítéséhez egy külön gombot készítettél el. Például: 

java 

private void jBtn18ActionPerformed(java.awt.event.ActionEvent evt) {                                        
    String answer; 
    secondnum = Double.parseDouble(jtxtDisplay.getText()); 
    switch (operations) { 
        case "+": 
            result = firstnum + secondnum; 
            break; 
        case "-": 
            result = firstnum - secondnum; 
            break; 
        case "*": 
            result = firstnum * secondnum; 
            break; 
        case "/": 
            result = firstnum / secondnum; 
            break; 
        default: 
            throw new IllegalArgumentException("Invalid operation: " + operations); 
    } 
    answer = String.valueOf(result); 
    jtxtDisplay.setText(answer); 
} 
 

Ez a metódus végrehajtja a kiválasztott matematikai műveletet (összeadás, kivonás, szorzás vagy osztás) az első és a második szám alapján, majd megjeleníti az eredményt a képernyőn. 
