# Urgent.fm Livestudio Handleiding
## #1. routing diagram

![routing diagram](https://imgur.com/a/nSOqn "Algemeen routing diagram")

## #2. afspraken

- Geen drank in de liveroom. uitzondering flesjes **met dop**
- geen drank in de mixroom nabij de mixing console.
- geen voedsel in de studio.
- geen bekers/glazen. no way.
- Ruim alles op na de sessie: &nbsp;&nbsp;`geen onopgerolde kabels, los liggende micros/DI's, ...`
- vul de mic checklist in, hoeft niet lang te duren. te vinden in bovenste schuif. zie materiaallijst in #4.

## #3. Livesessie workflow

1. voorzie studio van stroom: <br/>
    eerst links beneden -> 2x rechts -> linksboven
&nbsp;&nbsp; `!! bij foute volgorde kan de elektrische zekering springen. !!`

1. zet de Mac aan
    - knopje aan achterzijde.
1. zet de stageblock aan in de Liveroom

    - indien [mute] niet afgaat is de sync met tafel niet in orde. turn it off and on again (de stageblock). sync success-> groen lampje op M32 scherm in rechterbovenhoek
    - start Pro Tools op
    - de studio master clock is afgestemd op [RedNet5 PTHD], pro tools moet aan staan om alles te doen syncen.
    - start Dante Controller en bevestig dat alle labels groen worden eens pro-tools is opgestart.
1. laad de livesessie preset, sla op onder Audio HD > Urgent.fm livesessies  
&nbsp; `naamgeving: yyyy-mm-dd programma - artiest`

    - IN:
    - ch 1-24 mono: direct out van tafel (analog inputs 1-24)
    - ch 25 stereo: midas master mix (analog input 31/32)
    - ch 26 stereo: radio feed (analog input 27/28)
    - `zorg dat alle relevante tracks [armed] zijn`

1. evt. hernoemen van tracks als er tijd is
1. werking midas: neem de midas handleiding door! en/of zie hoofdstukje basiswerking M32
    - fx configuratie: bus 13-16
      1. stereo slapback delay. handig om gitaren, etc breed te trekken
      1. tap delay: tap op knopje dat flikkert
      1. room reverb: korte reverb
      1. rich plate reverb:
    - Masterbus mastering
        - select master > knop [effects] naast scherm.
        - mik op -9 tot -6 dB, de rest trekt de radiostudio wel gelijk.
1. monitoring:
    1. voor kleine sessies < 15 channels laad scene `live-direct-monitor`
        - de eerste 15 preamps worden gemirrord op de powerplay bakjes, kanaal 16 is talkback.
    1. grotere sessies > 15 kanalen laad scene `live-bus-monitor`
        - je moet de kanalen via de tafel naar één van de mixbussen routen. de mixbussen 1-12 komen terug op de powerplay. bus 16 is talkback. //TODO: zoek uit wat gebeurt met 13-16
1. beluistering van opname:
        - speel af op mac
        - beluister op chan 25/26 `in solo`. stuur deze nooit naar de masterbus (feedback loop)
        - om op de tafel af te mixen: routing > home de inputs te veranderen van AES50 A naar card. Als je in protools de preset hebt geladen staan de outputs al goed gerout.

### routing referentie voor livesessie

- op Midas:

  - routing > home: &nbsp;&nbsp;`=> selectie van inputs op tafel`

    - [ 1- 8] -> AES50 A1-8
    - [ 9-16] -> AES50 A9-16
    - [17-24] -> AES50 A17-24
    - [25-32] -> Card 25-32
        dus

      - 24    kanalen komen van de stageblock,
      - 25/26 is playback van master opname op pc
      - 30/31 is alfuistering van live radio.
    - routing > out 1-16 &nbsp;&nbsp;`=> uitsturen van masterbus naar radio en pro-tools`
        - 11/12 is [direct out channel 30/31]
        - 13/14 is [master L/R Pre master fader] -> naar pro tools opname
        - 15/16 is [master L/R Post master fader]. -> naar radio
        - rest wordt niet gebruikt
    - routing > ultranet &nbsp;&nbsp;`=> uitsturen naar powerplay monitoring bakjes`
        - in scene preset  &nbsp;&nbsp;`live-direct-moni`: [1-16] -> [direct channel out 1-16 (prefader)]
        - in scene preset  &nbsp;&nbsp;`live-bus-moni`: [1-16] -> mixbus 1-16 (prefader)
    - routing > card &nbsp;&nbsp;`=> uitsturen van dry kanalen naar pro-tools`
        - [ 1- 8] -> AES50 A1-8
        - [ 9-16] -> AES50 A9-16
        - [17-24] -> AES50 A17-24
        - [25-32] -> Out 9-16 `dus hier worden de settings in [routing > out 1-16] op de card out overgenomen`
- in Dante Controller
    - transmitter [Midas M32] &nbsp;&nbsp;&nbsp;&nbsp; 1-32 &nbsp; -> &nbsp; Receiver [Rednet5 PTHD] 1-32
    - transmitter [Rednet5 PTHD]                       1-26 &nbsp; -> &nbsp; Receiver [Midas M32] 1-26
    - transmitter [Rednet3 AES] &nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1/2 &nbsp;-> &nbsp; Receiver [Midas M32] 31/32
    - transmitter [Midas M32] &nbsp; &nbsp;&nbsp;31/32 &nbsp; -> &nbsp; Receiver [Rednet3 AES] 1/2
- in Pro Tools:
    - i/o per track: 1-24 is analog in en out 1-24, al staat er soms avalon of iets dergelijks bij
    - track 25 is een stereo track voor de master bus: i/o 25/26
    - track 26 is een stereo track voor de radio feed: i/o 31/32

## #4 Materiaallijst

kast A

- schuif 1:
  - 6x Sure Sm58
  - 2x Sennheiser e606
  - 10x Radial DI (passief)
  - 3x popfilter
  - materiaallijst
- schuif 2:
  - 6x Shure Sm57
  - 3x Shure Bèta 57
  - 1x Shure Bèta 52a
  - 1x AKG d112
  - 1x AKG D12
- schuif 3:
  - 4x Sennheiser MD421
  - 2x Audio Technica AT2020
  - 2x Audio Technica AT4041
  - 2x Shure Sm81
  - stereo bar
  - extra mic mount
- schuif 4: `alle koptelefoons MET 3.5mm adapter`
  - 5x Sennheiser HD280 koptelefoon
  - AKG d50

Kast B