# Overordnet datastruktur i prosjektet:
- EveFactory tar seg av all prosessering i bakgrunnen.
- EveFactoryViewer tar seg av frontend biten. 
- Splittes opp i flere Docker images så bare EFV publliseres mot internett.

## EveFactory
Tar seg av all prosessering og mater data til EveFactoryViewer on-demand. Alle connections mot database(r) skjer her.
Snakker med EFV via REST API.
Krever egen database image eller instans av Postgresql.

## EveFactoryViewer
Tar seg av kommunikasjon mot bruker. Prosesserer bare svar fra EF REST API.