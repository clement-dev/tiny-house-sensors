# Mesures 🔬

## Schémas de la Tiny 

![Sketch 01](./src/resources/images/Sketch_01.png)
![Sketch 02](./src/resources/images/Sketch_02.png)

## Mesures automatisées

| information                                          | Plage        | période | Capteur          | N°   | μCtlr | topic & exemple                                        |
|------------------------------------------------------|--------------|---------|------------------|------|-------|--------------------------------------------------------|
| Salon Temp (°C) & Hygro (%)                          | 10 à 30 °C   | 10 min  | Si7021           | 1 9  | A     | ltl/tiny/capteur/salon {"temp":20.1, "hygro":35}       |
| Mezzanine temp. (°C)                                 | 10 à 30°C    | 10 min  | DS18B20          | 2    | A     | ltl/tiny/capteur/mezzanine {"temp":20.1}               |
| masse poele (°C)                                     | 20°C à 200°C | 10 min  | MAX31865 + PT100 | 3    | D     | ltl/tiny/capteur/poele {"temp":20.1}                   |
| Extérieur Temp (°C) & Hygro (%)                      | \-20 à 50°C  | 10 min  | Si7021           | 4 10 | C     | ltl/tiny/capteur/dehors {"temp":10.3, "hygro":95}      |
| Serre (°C)                                           | \-20 à 50°C  | 10 min  | DS18B20          | 5    | B     | ltl/tiny/capteur/serre {"temp":20.1}                   |
| sortie capteur air chaud (°C)                        | 10 à 80°C    | 10 min  | DS18B20          | 6    | (A?)  | ltl/tiny/capteur/airChaud {"temp":65.1}                |
| liquide caloporteur sortie de chauffe- eau sol. (°C) | 10 à 120°C   | 10 min  | DS18B20          | 7    | E     | ltl/tiny/capteur/solaireOut {"temp":65.1}              |
| ballon eau chaude (°C)                               | 20 à 100°C   | 10 min  | DS18B20          | 8    | E     | ltl/tiny/capteur/ECS {"temp":65.1}                     |
| Ensoleillement (si pas tp compliqué) (W/m2)          |              | 10 min  | ?                | 11   |       | ltl/tiny/capteur/soleil {"sol":578}                    |
| Production énergétique phovoltaique (W)              |              | 10 min  | PZEM-017         | 12   | F     | ltl/tiny/capteur/prodPV {"p":57, "u":12.2, "i":4.7}    |
| Consommation énergétique (W)                         |              | 10 min  | PZEM-017         | 13   | F     | ltl/tiny/capteur/consoElec {"p":57, "u":12.2, "i":4.7} |
| Marche/Arrêt Ventilation destratificateur (bit)      |              | \-      | ??               | 14   |       | ltl/tiny/capteur/ventilo {"on":true}                   |
| Marche/Arrêt Pompe chauffe eau (bit)                 |              | \-      | ??               | 15   | E     | ltl/tiny/capteur/pompeCE {"on":false}                  |

**N°** = Numéro sur le shéma  
**μCtlr** = microcontroleur = carte électronique interface entre le capteur et
le réseau **topic** Il seront de la forme :

ltl/tiny/capteur/xxxx pour tout ce qui vient des capteurs ltl/tiny/manu/xxxx
pour les informations manuelles

## Mesures manuelles

| Information                                                         | technologie    | Remarque                             | N° |
|---------------------------------------------------------------------|----------------|--------------------------------------|----|
| Lancement et fin du feu (secondes)                                  |                |                      | 16 |
| Masse de bois ajouté au poele (kg)                                  | Balance                        |                                                                                                                                            | 17 |
| Type de bois ajouté au poele                                        |                                |                                                                                                                                            | 18 |
| Humidité bois (%)                                                   |                                |                                                                                                                                            | 19 |
| Debit air en sortie de capteur à air chaud                          |                                | Comment quantifier cela ?                                                                                                                  | 20 |
| Consommation énergétique nominal des appareils élec                 |                                | ??                                                                                                                                         | 21 |
| Consommation eau douche (litres)                                    | compteur eau                   |                                                                                                                                            | 22 |
| Consommation gaz showerloop (masse consommée) (kg)                  | Balance                        |                                                                                                                                            | 23 |
| Temps passé sous la douche (secondes)                               | Chronomètre                    |                                                                                                                                            | 24 |
| Temps début et fin d'utilisation de marmite norvégienne (secondes)  | Chronomètre                    |                                                                                                                                            | 25 |
| Charge de la batterie (Volts                                        | Indicateur de charge           | Le point 13 nécessite la connaissance du voltage disponible sur le réseau. Il sera sans doute intéressant de transformer cette valeur en % | 26 |
| Surface de collecte d'eau de pluie (m2)                             |                                | Ca peut changer ?                                                                                                                          | 27 |
| Niveau d'eau disponible en tps réel (litres)                        | Jauge                          | Automatisable, par capteur ultrason ou pression d'air, ou pesage                                                                           | 28 |
| Volume d'eau de pluie récolté (litres)                              | Compteur d'eau ou pluviomètre  | Il faut de la pression pour le compteur d'eau                                                                                              | 29 |
| Qualité de l'eau en entrée de l'habitat                             | Analyse en labo                |                                                                                                                                            | 30 |
| Volume eau grise rejetée (litres)                                   | Seaux avant phyto ou compteurs |                                                                                                                                            | 31 |
| Qualité de l'eau en sortie de l'habitat                             | Analyse en labo                |                                                                                                                                            | 32 |
| Masse de déchet organique issu de gaspillage (fruit pourri,..) (kg) | balance                        |                                                                                                                                            | 33 |
| Masse de dechet organique issu toilette seche                       | Nb de seaux                    |                                                                                                                                            | 34 |
| Type de matière carbonée ajouté aux toilettes                       |                                |                                                                                                                                            | 35 |
| Type et nb de commission faites aux toilettes                       |                                |                                                                                                                                            | 36 |

## Matériel

| Points (N°) | Modèles             | Nombre | Montants |
|-------------|---------------------|--------|----------|
| 19 4 10     | Si7021              | 2      | 2        |
| 256 7 8     | DS18B20             | 5      | 1        |
| 12 13 26    | PZEM-017            | 2      | 14       |
| 3           | MAX31865            | 1      | 3        |
| 3           | PT100               | 1      | 5        |
| 3           | SEN0198             | 1      | 20       |
| AB C DE     | ESP8266             | 5      | 3        |
| F           | Arduino Mega + WiFi | 1      | 12       |
| server      | OrangePi Zero       | 1      | 16       |
| server      | Carte Orange Pi NAS | 1      | 12       |
| server      | Carte micro SD      | 1      | 4        |
| server      | Disque dur SSD      | 1      | 22       |
| alims       | step down 12V 5V    | 7      | 3        |

**Remarques :**

Concernant les mesures de température au niveau du ballon d'eau chaude, je pense qu'il serait intéressant de mettre plusieurs capteurs, au moins 3, à différentes
hauteurs du ballon. 
Cela permet d'avoir une meilleure idée de la quantité d'eau chaude présente.  La liste de matériel est une liste minimale qui pourra s'étoffer par la suite.
De plus, elle ne contient pas de nombreuses petites bricoles comme des cables et des résistances par exemple.
