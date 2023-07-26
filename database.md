## Auto Usate

| Colonna           |    Tipo     |                  Attributo |
| ----------------- | :---------: | -------------------------: |
| id                |   BIGINT    | PRIMARY_KEY AUTO_INCREMENT |
| marca             | VARCHAR(30) |                   NOT NULL |
| prezzo_vendita    |  SMALLINT   |                   NOT NULL |
| danni             |   TINYINT   |                       NULL |
| motore            | VARCHAR(30) |                   NOT NULL |
| targa             | VARCHAR(7)  |           NOT NULL, UNIQUE |
| cilindrata        |  SMALLINT   |                       NULL |
| classe_emissioni  | VARCHAR(20) |                       NULL |
| cambio_automatico | TINYINT(1)  |       NOT NULL, DEFAULT(0) |
| trazione          | VARCHAR(3)  |                       NULL |
| immatricolazione  |    YEAR     |                   NOT NULL |

#### CONSIDERAZIONI

- Il prezzo è **SMALLINT** e non **MEDIUMINT** immaginando che le auto usate non siano di lusso
- La targa è **VARCHAR(7)** immaginando che abbiano tutte una marca italiana e **UNIQUE** perchè debbano essere tutte diverse tra loro
- Il cambio_automatico è **DEFAULT(0)** perchè volgio gestirlo come un booleano che sia falso di partenza
- la trazione è **VARCHAR(3)** perchè voglio gestire le trazioni con tre lettere **INT** = _trazione integrale_, **ANT** = _trazione anteriore_ e **POS** = _trazione posteriore_
