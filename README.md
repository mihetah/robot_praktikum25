## 🔰 Einführung in Java – Grundkonzepte für RoboCode

> Diese Einführung vermittelt dir die wichtigsten Grundlagen der Programmiersprache Java. Du brauchst sie, um später deinen eigenen Roboter programmieren zu können. Auch wenn du in RoboCode arbeitest, ist es wichtig, zu verstehen, wie Java ganz allgemein funktioniert.

----------

### 🔹 **1. Klassen und Objekte**

#### 🧠 Was ist eine Klasse?

Eine Klasse ist ein **Bauplan**. Sie beschreibt, welche Eigenschaften (Attribute) und Fähigkeiten (Methoden) ein Objekt hat.

```java
public class Auto {
    int geschwindigkeit;

    void fahren() {
        System.out.println("Das Auto fährt.");
    }
}

```

#### 🧠 Was ist ein Objekt?

Ein Objekt ist ein **konkretes Exemplar** einer Klasse.

```java
public class Start {
    public static void main(String[] args) {
        Auto meinAuto = new Auto();
        meinAuto.fahren(); // Ausgabe: Das Auto fährt.
    }
}

```

➡️ In RoboCode wird dein Roboter später ebenfalls als Objekt erzeugt – auf Basis deiner eigenen Klasse.

----------

### 🔹 **2. Vererbung und Oberklassen**

#### 🧠 Was ist Vererbung?

Vererbung bedeutet, dass eine Klasse von einer anderen Klasse **erbt**. Die erbende Klasse bekommt automatisch die Eigenschaften und Methoden der Oberklasse – und kann sie erweitern oder überschreiben.

```java
public class Fahrzeug {
    void hupen() {
        System.out.println("Huuup!");
    }
}

public class Auto extends Fahrzeug {
    void fahren() {
        System.out.println("Auto fährt.");
    }
}

```

```java
public class Start {
    public static void main(String[] args) {
        Auto a = new Auto();
        a.fahren(); // Auto fährt.
        a.hupen();  // Huuup!
    }
}

```

➡️ In RoboCode ist das genauso: Dein Roboter erbt Funktionen von einer RoboCode-Oberklasse wie `AdvancedRobot`.

----------

### 🔹 **3. Methoden & Überschreiben**

#### 🧠 Was ist eine Methode?

Eine Methode ist ein **benannter Codeblock**, der eine bestimmte Aufgabe erledigt.

```java
public class Auto {
    void fahren() {
        System.out.println("Auto fährt.");
    }
}

```

#### 🧠 Was bedeutet "überschreiben"?

Wenn du eine Methode aus der Oberklasse **neu definierst**, überschreibst du sie:

```java
public class Sportwagen extends Auto {
    @Override
    void fahren() {
        System.out.println("Sportwagen fährt sehr schnell!");
    }
}

```

➡️ In RoboCode überschreibst du z. B. `run()` oder `onScannedRobot()`, um deinem Roboter eigenes Verhalten zu geben.

----------

### 🔹 **4. Sichtbarkeit – public, private, protected**

Schlüsselwort

Bedeutung

`public`

Überall sichtbar (auch RoboCode braucht das!)

`private`

Nur in der eigenen Klasse sichtbar

`protected`

Sichtbar für die eigene und alle abgeleiteten Klassen

Beispiel:

```java
public class Auto {
    private int geschwindigkeit = 0;

    public void fahren() {
        System.out.println("Fährt mit " + geschwindigkeit + " km/h");
    }
}

```

➡️ In RoboCode verwendest du fast immer `public`, damit RoboCode deine Methoden erkennen und ausführen kann.

----------

### 🔹 **5. Bedingungen – Entscheidungen im Code**

```java
public class Ampel {
    public static void main(String[] args) {
        String farbe = "Rot";

        if (farbe.equals("Grün")) {
            System.out.println("Fahren!");
        } else {
            System.out.println("Anhalten!");
        }
    }
}

```

➡️ Später kann dein Roboter z. B. abhängig von der Energie oder Gegnerposition unterschiedlich reagieren.

----------

### 🔹 **6. Schleifen – Wiederholung von Code**

```java
public class Zaehler {
    public static void main(String[] args) {
        int i = 0;
        while (i < 5) {
            System.out.println("Zahl: " + i);
            i++;
        }
    }
}

```

➡️ In RoboCode nutzen Roboter oft eine `while(true)`-Schleife, um dauerhaft aktiv zu bleiben.

----------


### ✨ **Abschluss: Dein erstes Java-Programm – Hello World**

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
    }
}

```

🧩 **Was passiert hier?**

-   `public class HelloWorld` → Deine Klasse mit dem Namen `HelloWorld`
    
-   `public static void main(String[] args)` → Diese Zeile wird **immer zuerst ausgeführt** – sie ist der Startpunkt des Programms.  
    ✅ Kurzform: `psvm` steht für `public static void main` – eine häufig genutzte Abkürzung
    

----------

🧪 **Teste deinen Code direkt online:** 👉 [Zum Online-Java-Compiler (Programiz)](https://www.programiz.com/java-programming/online-compiler/)  
➤ Kopiere deinen Code dort hinein und klicke auf **"Run"**.

----------

✅ **Nächster Schritt:** Du wirst bald deinen ersten eigenen Roboter bauen – und viele dieser Begriffe wiedererkennen und anwenden.
