# Lexmodo Country -> Province builder
This README file explains how to build product variants automatically as select/radio depending on your design 

---
## Structure
```html
/* !!Replace the `UNIQUE IDENTIFIER` */
<select select="country" aim="{{UNIQUE IDENTIFIER}}"></select>
<select select="province" target="{{UNIQUE IDENTIFIER}}"></select>
```

---

## Inside JS
### Inside select-country-province.js change the path to countries.json in the fetchCountries function
```javascript
const fetchCountries = async () => {
  const response = await fetch('/assets/JSON/countries.json'); 
  const countriesObjectJSON = await response.json();
  countriesObject = countriesObjectJSON;
  initializeSelects();
};
```

### Import the 'fetchCountries' function from 'select-country-province.js' and use it to create select options reponsive to each other.
```javascript
import fetchCountries from "./select-country-province.js";
fetchCountries();
```
## Resulats 
![Screencast from 06-19-2023 04_48_22 PM](https://github.com/mostafaelhussainy/country-province-select/assets/105276328/71452e6e-6052-47fb-bb87-6c5f45374c60)
Note: The comments in the code provide guidance on where to place the previous button, index tabs, next button, and other relevant elements.
