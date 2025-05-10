# Guide til lansering av egen npm-pakke 📦

1. [Opprett npm bruker](https://www.npmjs.com/signup)
2. Test brukeren din med `npm login`: [dokumentasjon](https://docs.npmjs.com/creating-a-new-npm-user-account#testing-your-new-account-with-npm-login)
3. I terminalen navigerer du til mappen du har lyst til å ha repoet. Nå skal du et viktig navn, nemlig navnet på hva pakken din skal hete på npmjs. Det er derfor litt viktig å ta en titt på disse små [retningslinjene](https://docs.npmjs.com/package-name-guidelines) før du skriver `mkdir ditt-unike-pakkenavn`.
4. Opprett en `package.json` med kommandoen `npm init` og fyll ut valgfritt.
5. I `package.json` kan du legge til `“main”: “./dist/index.ts”`. Dette forteller hvilken bygd TypeScript-fil som er startpunktet når noen importerer pakken din. Legg deretter til `"types": "./dist/index.d.ts"`. Dette gjør du får å fortelle hva som er typedefinisjonene. 
</br>📚: Les mer om `.d.ts`-filer her i [TypeScript sin egen dokumentasjon](https://www.typescriptlang.org/docs/handbook/2/type-declarations.html#:~:text=.-,d.,our%20own%20declaration%20files%20later.).
Dist-mappen inneholder kompilerte filer og genereres i byggeprosessen. 
7. I `package.json` kan du legge på nøkkelord som `author`, `license`, `keywords`, `bugs`, `homepage`, `repository`. Dette blir referanser som brukere kan se på npm-siden til pakken din. Prøv å fylle ut disse og sjekk ut senere 😁.
8. `npm install -D typescript` for å kunne skrive TypeScript. Dette gjør vi for å kunne konvertere `.ts`-filer til `.js`-filer. Det er for å kunne sjekke typer under utvikling og generering av `.d.ts` filer som vi så på i steg 5.
9. Opprett en `.gitignore` og legg til `node_modules` og `dist` ettersom disse ikke er vits å versjonskontrollere genererte filer.
10. For å kompilere koden til JavaScrip trenger vi en `tsconfig.json`-fil. Dette gjør vi med kommandoen `npx tsc --init`. Hvis du har TypeScript globalt på maskinen trenger du ikke ha med `npx`. `tsc` er et TypeScript cli som lar deg kompilere fra TypeScript til JavaScript.
</br>a. Legg til `"include": ["src"]` som forteller `tsc` hvilken kode du skal kompilere.
</br>b. `"exclude": ["node_modules", "dist"]` på utsiden av compilerOptions. Dette er paths som du ikke vil kompilere. Legg til `"outDir": "./dist"`, i compilerOptions. Det er her koden blir plassert.
11. `git init` på rot-nivå i pakken etterfulgt av `git remote add origin git://git-remote-url`.
12. `npm publish` og sjekk at du har publisert pakken din på npmjs.com!
13. Gjør en endring og gjør en npm publish igjen, se hva som skjer! Kan `npm version patch` hjelpe?
    
## 📚[Scopes](https://docs.npmjs.com/about-scopes)
* [unscoped public packages](https://docs.npmjs.com/creating-and-publishing-unscoped-public-packages)
* [scoped public packages](https://docs.npmjs.com/creating-and-publishing-scoped-public-packages)
* [private packages](https://docs.npmjs.com/creating-and-publishing-private-packages)


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

