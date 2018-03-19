---
title: Raktinis žodis final
category: Teorija
order: 2
---

Kintamasis (angl. variable) final - uždrausti keisti reikšmę. (t.y. Galima inicializuoti tik vieną kartą šio kintamojo reikšmę).

```java

public static final int KONSTANTA = 315;
private final String SAVININKAS= "Lietuvos bankas";
private final int ID; // Incijuoti ID galima tik per konstruktorių vieną kartą!

public Parduotuve(String pavadinimas, String adresas, int ID) {
   this.pavadinimas = pavadinimas;
   this.adresas = adresas;
   this.ID = ID;
}
```

Metodas (angl. method) final - uždrausti metodą paskelbtą **final** perrašyti (@Override) paveldėjusioje klasėje.

```java

// Pagrindinė tėvinė klasė su final metodu
class Bankas{
	public final void balansas(int id){
		//................
		// ieškome balanso pagal id
		System.out.println("Asmens balansas yra 200");
	}
}
// Tarkime turime kitą klasę Bankomatas
class Bankomatas extends Bankas{
	 @Override // metodo balansas negalime perrašyti tik paveldėti
	 public final void balansas(int id){
		System.out.println("Bandome perrašyti metodą pagal Bankomato klasę bet negalėsime.");
	}
	
}
```

Klasė (angl. class) final - uždrausti paveldėti klasę.
