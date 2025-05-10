# react-i-praksis-pakker-ds
En enkel verktøypakke som tilbyr en hilsen i console.

## Installasjon ⚙️
```
npm install react-i-praksis-pakker-ds
```

eller

```
yarn add react-i-praksis-pakker-ds
```

eller hvis du vil være sjef:

```
pnpm add react-i-praksis-pakker-ds
```

## Bruk 👨🏻‍💻
Pakken eksporterer en enkel funksjon som logger en hilsen til konsollen.

### ES Moduler
```
import hello from 'react-i-praksis-pakker-ds';

hello('Verden'); // Logger: Hello, Verden!
```

### CommonJS
```
const hello = require('react-i-praksis-pakker-ds').default;

hello('Verden'); // Logger: Hello, Verden!
```
### API
`hello(name: string): void`
Logger en hilsen til konsollen.

#### Parameter
`name`: Navnet som skal inkluderes i hilsningsbeskjeden
#### Returnerer
Denne funksjonen returnerer ingen verdi, men en melding i console.

## TypeScript-støtte 
Denne pakken inkluderer TypeScript-deklarasjoner og er fullt typet.

## Lisens 🧑🏼‍⚖️
MIT © Fredrik Mørk

## Bidrag 👥
Issues og pull-requester er velkomne. Ikke nøl med å bidra til dette prosjektet.
