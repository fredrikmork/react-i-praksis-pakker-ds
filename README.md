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

eller hvis du vil være sjefsjef 🕶️:

```
pnpm add react-i-praksis-pakker-ds
```

## Bruk 👨🏻‍💻

Pakken eksporterer en enkel funksjon som logger en hilsen til konsollen.

### ES Modules

```
import { hello } from 'react-i-praksis-pakker-ds';

hello('Verden'); // Logger: Hello, Verden!
```

### CommonJS

```
const { hello } = require('react-i-praksis-pakker-ds');

hello('Verden'); // Logger: Hello, Verden!
```

### Tilgjengelig funksjon

`hello(name: string): void`
Logger en hilsen til konsollen.

#### Parameter

`name`: Navnet som skal inkluderes i hilsningsbeskjeden

#### Retur-verdi

Denne funksjonen returnerer ingen verdi, men en melding i console.

## Lisens 🧑🏼‍⚖️

MIT © Fredrik Mørk

## Bidrag 👥

Issues og pull-requester er velkomne. Ikke nøl med å bidra til dette prosjektet.
