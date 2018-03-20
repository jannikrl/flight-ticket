## Kør Vue.js-projektet
1. Gå til mappen _flight-ticket_ i terminalen
2. Kør kommandoen _npm install_ efterfulgt af _npm run dev_
3. Åben http://localhost:8080/ browseren 

## Opbygning
- I _components_-mappen (src > components) ligger FlightTicket og dets underkomponenter. I _component_-mappen ligger også generelle komponenter som Button, Badge, og Rating.
- I _assets_-mappen (src > assets) findes de fælles CSS-filer som _normalize.scss, _varibales.scss og _base.scss
- Button- og Badge-komponenterne er bygget efter OOCSS-tankegangen opdelt i _structure_, _size_ og _color_.
- Rating-komponentet skifter smiley hvis værdien ændres (ret evt. værdien i FlightTicket.vue linje 75 til _2.2_)
- Flybilleten er responsive og vil tilpasse sig efter skærmens brede. Tilpasning af layout sker i FlightTicket-komponentet.

