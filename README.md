# Database-OLA2-fitnesscenter

##  ER-Modellering

### 🏋️ Nøglefunktioner i systemet

- Medlemskaber: Basis, Premium, Elite – med forskelle i adgang til faciliteter.
- Træningshold: Spinning, CrossFit, Yoga m.m. – hvor medlemmer kan tilmelde sig.
- Instruktører: Tilknyttet hold og kan administrere deltagerlister.
- Booking: Medlemmer kan booke pladser på hold eller personlig træning. Hold har typisk begrænset antal pladser.
- Betaling: Månedsvis abonnement eller klippekort.
- Medlemsrabatter: Kan gives i særlige tilfælde.

En ordre har enten null type på membership_type eller product_type da man kan kan købe enten et medlemskab eller et produkt som fx drikkedunk/protein bar.
Det er vigtigt at kunne se hvilken type medlemsskab et medlem har. Derfor har vi valgt at lave en membership type tabel.

Sessions = Hold. Et medlem kan booke sig ind på en session. En session har en type fx spinning som kan have et max antal på eksempelvis 16 da dette er max antal motionscykler i fitness centeret. Instruktøren kan oprette en session.

Vi gjorde os en del overvejelser omkring relationen imellem members og membership type. Vi kunne godt tænke os at få lidt feedback på denne del. Hvad ville du gøre Tine?
![image](https://github.com/user-attachments/assets/bd26d822-ada5-477b-82b0-8215a2af3fd6)

## Normalisering af ER-modellen

- 1NF: Sikr jer, at alle attributter er atomare og at der ikke er gentagne grupper.
- 2NF: Fjern partielle funktionelle afhængigheder (sørg for, at ikke-nøgle attributter afhænger af hele primærnøglen).
- 3NF: Fjern transitive afhængigheder (sørg for, at alle ikke-nøgle attributter kun afhænger af primærnøglen).

Alle attributer som kaldes ID er primary key.

Da vi allerede har lavet ER diagrammer på datamatiker undgik vi fælden med de 2 første NF'er. Derfor var det primært 3NF vi måtte gøre os nogle tanker for at ramme. Vi undlod at skrive FK's på det første billede da opgaven beskrev at vi skulle gøre dette i opgave 2. Men dette var i tankerne allerede fra start af.

For at ramme 3NF har vi valgt at session skal indholde så manger ID/FK'er som muligt.


![image](https://github.com/user-attachments/assets/97d0a5de-1bc2-4875-9b22-2d40815817f3)


## Mapping til Relationel Model
![image](https://github.com/user-attachments/assets/7c140c05-b06e-4dee-bc3d-8ee53920e5a2)


