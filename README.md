Guide til lansering av egen npm-pakke

1. [Opprett npm bruker](https://www.npmjs.com/signup)
2. Test brukeren din med `npm login`: [dokumentasjon](https://docs.npmjs.com/creating-a-new-npm-user-account#testing-your-new-account-with-npm-login)
3. Opprett en `package.json` med kommandoen `npm init` og fyll ut valgfritt.
4. I `package.json` kan du endre `“main”` til `“./dist/index.ts”` og legg til `"types"` med `"./dist/index.d.ts"` HVORFOR??
5. I `package.json` kan du legge på nøkkelord som `author`, `license`, `keywords`, `bugs`, `homepage`, `repository`. Dette blir referanser som brukere kan se på npm-siden til pakken din. Prøv å fylle ut disse.
6. `npm install -D typescript` for å kunne skrive TypeScript
7. Opprett en `.gitignore` og legg til `node_modules` og `dist`.

a. Legg til "include": ["src"],
    "exclude": ["node_modules"] på utsiden av compilerOptions
Legg til "outDir": "./dist", i compilerOptions

1. npm install -D tsup Vi trenger å bygge typescript-pakken vårt og må derfor bundle det først. 

    * Hva er bundling? Diskuterer med sidemannen

1. git init på rot-nivå i pakken
2. git remote add origin git://git-remote-url

Oppretter og publiserer

* unscoped public packages
* scoped public packages
* private packages


Hva scopes er: https://docs.npmjs.com/about-scopes
Noe å tenke på når man velger navn: https://docs.npmjs.com/package-name-guidelines
Ny versjon npm version patch

Utforsking av npm publish - hva har Helene gjort:

* Npm publish - fikk feilmelding om at repo var private
    * Gikk inn i package.json og endret “private” til false
* Npm publish - fikk feilmelding om ikke kjent bruker:
* Npm adduser - logget inn på npm
* Npm publish - publiserte første pakke :partying_face: 
    * Her bør vi passe på at hver gruppe gir pakkene sine forskjellige navn
* Gjør en endring - npm publish
    * Får feilmelding om at man ikke kan endre på en allerede publisert pakke
* Npm version patch - lager en patch versjon
* Inne på npm: Depreker pakken og slett pakken

