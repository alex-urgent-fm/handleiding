# Urgent.fm livestudio handleiding
### inhoud
1. Routing diagram
1. Afspraken
1. Livesessie workflow
1. Gebruik Midas M32 console
1. Gebruik Powerplay P16 (monitor mixertjes)
1. Materiaallijst 

## #1. routing diagram

![routing diagram](https://i.imgur.com/eD0j5Xl.png "Algemeen routing diagram")

## #2. afspraken

- Geen drank in de liveroom. uitzondering flesjes **met dop**
- geen drank in de mixroom nabij de mixing console.
- geen voedsel in de studio.
- Ruim alles op na de sessie: &nbsp;&nbsp;`geen onopgerolde kabels, los liggende micros/DI's, ...`
- vul de mic checklist in, hoeft niet lang te duren. te vinden in bovenste schuif. zie materiaallijst in #5.

## #3. Livesessie opstart checklist

1. voorzie studio van stroom:
    * zet de 4 stroomschakelaars aan: linksonder, linksboven, en rechtsonder 2 keer
&nbsp;&nbsp; `!! bij foute volgorde kan de elektrische zekering springen. !!`
    * zet de Mac aan: knopje aan achterzijde
    * zet de Midas aan: knopje aan de achterkant van de tafel, in de buurt van het stroomsnoer
    * zet de Yamaha versterker aan: links in de beenruimte onder de mengtafel. de Yamaha NS-10 zijn aangesloten.
    * zet de Trinnov DSP aan: de onderste unit in de linker rack.
    * zet de stageblock aan in de Liveroom
    * indien [mute] op de stageblock niet uitgaat is de synchronisatie met tafel niet in orde. *turn it off and on again* (de stageblock). sync success -> groen lampje op M32 scherm in rechterbovenhoek
    
1. start een nieuwe opnamesessie op de Mac
    - ![Dante controller en Pro Tools](https://i.imgur.com/bBmiiyB.png "Dante controller Pro Tools")
    - start 'Pro Tools'. de studio master clock is afgestemd op [RedNet5 PTHD], Pro Tools moet dus aanstaan om alles te doen samenwerken
    - start 'Dante Controller' en laad de correcte preset in: `Setup REDNET` `24ch Midas Recording preset`
    - maak een nieuw project in Pro Tools:
      * via Dashboard > CREATE
      * via 'File' > 'create new'
      * Name: gebruik altijd de naamgeving 'yyyy-MM-dd Programma - Artiest'
      * Create From Template: template group 'recording' > '24ch Standaardpatch'
      * I/O settings: '24io'
      * Location: 'Audio HD' > 'Urgent Sessies' 
      * ![create](https://i.imgur.com/0bTv1S7.png "create new project")
    - `zorg dat alle relevante tracks [armed] zijn (rode rec knob flikkert)`
1. breng de Midas in gereedheid:
    - laad de preset: 
      1. druk op de knop `View` onder show control en navigeer met de pijltjes onder het scherm naar het tabblad *scenes*
      1. laad de scene '24ch Standaardpatch'
1. aanzetten van de speakers
    Dangerous source: AN1
    1. SPKR 1 = KII three
    1. SPKR 2 = Yamaha ********* HOE AANZETTEN ?? ****************
1. beluistering van opname:
  - beluister op chan 25/26 `ALTIJD in solo`.
  - om de apart opgenomen tracks te beluisteren: 
    - druk op knop 'ROUTING' naast het scherm
    - op het 'home' tab, zet inputs 1-8 op 'card 1-8', 9-16 op 'card 9-16' enz
    - let op! bij het terugzetten blijft 'Inputs 25-32' op 'card 25-32'
        
### routing referentie voor livesessie

#### op Midas M32:

  - routing > home `=> selectie van inputs op tafel`
    - [ 1- 8] -> AES50 A1-8
    - [ 9-16] -> AES50 A9-16
    - [17-24] -> AES50 A17-24
    - [25-32] -> Card 25-32

dus:

      - 24 kanalen komen van de stageblock
      - 25/26 is playback van master opname op PC
      - 31/32 is afluistering van live radio.
  - routing > out 1-16 `=> uitsturen van masterbus naar radio en pro-tools`  
        - 13/14 is [direct out channel 31/32] -> `stuurt radio L/R naar Pro Tools`  
        - 15/16 is [master L/R Post master fader]. -> `stuurt masterbus naar Pro Tools`    
        - rest wordt niet gebruikt
  - routing > Ultranet P16 `=> uitsturen naar powerplay monitoring bakjes`  
        - in scene preset  &nbsp;&nbsp;`live-direct-moni` ?: [1-16] -> [direct channel out 1-16 (prefader)]  
        - in scene preset  &nbsp;&nbsp;`live-bus-moni` ?: [1-16] -> mixbus 1-16 (prefader)  
  - routing > card &nbsp;&nbsp;`=> uitsturen van dry kanalen naar Pro Tools`  
        - [ 1- 8] -> AES50 A1-8  
        - [ 9-16] -> AES50 A9-16  
        - [17-24] -> AES50 A17-24  
        - [25-32] -> Out 9-16 `dus hier worden de settings in [routing > out 1-16] op de card out overgenomen: radio en Midas master naar Pro Tools`
#### in Dante Controller

- transmitter [Midas M32] &nbsp;&nbsp;&nbsp;&nbsp; 1-32 &nbsp; -> &nbsp; Receiver [Rednet5 PTHD] 1-32
- transmitter [Rednet5 PTHD]                       1-26 &nbsp; -> &nbsp; Receiver [Midas M32] 1-26
- transmitter [Rednet3 AES] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1/2 &nbsp;-> &nbsp; Receiver [Midas M32] 31/32
- transmitter [Midas M32] &nbsp; &nbsp;&nbsp;31/32 &nbsp; -> &nbsp; Receiver [Rednet3 AES] 1/2

#### in Pro Tools:

- i/o per track: 1-24 is analog in en out 1-24, al staat er soms avalon of iets dergelijks bij
- track 25 is een stereo track voor de master bus: i/o 25/26
- track 26 is een stereo track voor de radio feed: i/o 31/32

## #4 Gebruik Midas M32 console
## #5 Gebruik Powerplay P16 (monitor mixertjes)

## #6 Materiaallijst

kast A

- schuif 1:
  - 6x Sure Sm58
  - 2x Sennheiser e606
  - 10x Radial DI (passief)
  - 3x popfilter
  - stereo bar
  - mic mount extension
  - materiaallijst
- schuif 2:
  - 6x Shure Sm57
  - 3x Shure Bèta 57
  - 1x Shure Bèta 52a
  - 1x AKG d112
  - 1x AKG D12
  - 1x pg52
- schuif 3:
  - 4x Sennheiser MD421
  - 2x Audio Technica AT2020
  - 2x Audio Technica AT4041
  - 2x Shure Sm81
- schuif 4: `alle koptelefoons MET 3.5mm adapter`
  - 5x Sennheiser HD280 koptelefoon
  - AKG d50