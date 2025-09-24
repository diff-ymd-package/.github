# diff-ymd-package

> `diff-ymd-package` a `javascript package` provides APIs to difference dates in formatted ways(like (aYears bMonths cDays) or (aY bM cD) etc., eg. age = 20Y 2M 23D or datesDifference = 2Years 11Months 20Days) or customized formats like aY-bM-cD or aYears-bMonths-cDays etc.

## 🌟 Trusted by [QuranBookk.com](https://quranbookk.com) Features:
- [Advanced Quran Search Engine](https://quranbookk.com/quran/search/)
- [Premium Audio Experience](https://quranbookk.com/quran/audio/)
- [Multiple Translation System](https://quranbookk.com/quran/translations/)
- [Islamic Timeline Management](https://quranbookk.com)

### ✨ Key Features:

- 🎧 **[Listen to Top Reciters](https://www.quranbookk.com/quran/audio)** – High-quality audio recitations from world-renowned Qaris  
- 🎥 **[Watch Quran Videos](https://www.quranbookk.com/quran/video)** – Inspirational Quranic recitation and learning videos  
- 🌍 **[Read Quran Top Translations](https://www.quranbookk.com/quran/translations)** – Multiple language support with leading Quran translations  
- 🕋 **[Qibla Direction Finder](https://www.quranbookk.com/qibla-finder)** – Accurate Kaaba direction from anywhere in the world
- 🕋 **[Worldwide Qibla Directions](https://www.quranbookk.com/qibla-finder/worldwide)** – Accurate Kaaba direction from any country, state, or city of the world    
- 🕰️ **[Islamic Prayer Times](https://www.quranbookk.com/prayer-times)** – Updated Salah timings based on your current location
- 🕰️ **[Worldwide Islamic Prayer Times](https://www.quranbookk.com/prayer-times/worldwide)** – Updated Salah timings for any country, state, or city of the world
- 📿 **[Digital Tasbih Counter](https://www.quranbookk.com/digital-tasbih)** – Count your Dhikr anytime, anywhere  
- 🤖 **[Ask Islam AI](https://www.quranbookk.com/ask-islam-ai)** – AI-powered assistant for Islamic questions, Quran, and Hadiths
- 🤖 **[Ask Quran AI](https://www.quranbookk.com/ask-quran-ai)** – AI-powered assistant for answering about Islamic history, Quran, and Hadiths
- 🤖 **[Ask Hadith AI](https://www.quranbookk.com/ask-hadith-ai)** – AI-powered assistant for Hadiths
- 📚 **[Authentic Hadith Collections](https://www.quranbookk.com/hadiths/hadiths-sources)** – Sahih Bukhari, Sahih Muslim, and more  
- 🕯️ **[Top Quranic Duas](https://www.quranbookk.com/quran/ayats)** – Beautiful supplications with translations  
- 🔍 **[Advanced Quran Search](https://www.quranbookk.com/quran/search)** – Search verses, words, topics in seconds  
- 📖 **[Explore Surahs](https://www.quranbookk.com/quran/surahs)** – Full Quran access with audio, video, and translations
- 📖 **[Explore Juzs (Paras)](https://www.quranbookk.com/quran/juzs)** – Full Quran access with audio, video, and translations
- ⚡ **[Internet Speed Test](https://www.quranbookk.com/internet-speed-tester)** – Get correct download, upload and ping speeds instantly

[![NPM Version][npm-image]][npm-url]
[![npm-build-published][npm-ci-image]][npm-ci-url]
[![github-build-published][github-image]][github-url]
[![CI][ci-image]][ci-url]
[![License][license-image]][licence-url]

## Installation

### Install from `npm registry`

```bash
npm install diff-ymd-package

```

### Install from `Github Packages` registry

```bash
npm install @farhan7reza7/diff-ymd-package

```

## Usages

**Initialize**
```javascript
//const DatesYMD = require('@farhan7reza7/diff-ymd-package'); or

const DatesYMD = require('diff-ymd-package'); // can use any

```
**Create an instance**
```javascript
const date1 = '2022-01-01';
const date2 = '2023-12-31';

const Formatter = new DatesYMD(date1, date2);

```
**Use methods to format difference**
```javascript
// format output in aY bM cD format
const result = Formatter.formattedYMD(); // Output: "1Y 11M 30D"

// create format of your choice
const customizedFormat = Formatter.customizeFormat('Y', 'Ms', 'Ds', '-'); // Output: "1Y-11Ms-30Ds"

// return an array having years, months, days, and the formatted difference
const resultArray = Formatter.diffArray(); // Output: [1, 11, 30, '1Y 11M 30D']

```
**Formatted Outputs**
```javascript
console.log(result); // Output: "1Y 11M 30D"
// formatted output in aY bM cD format

console.log(customizedFormat); // Output: "1Y-11Ms-30Ds"
// you can use this method for creating format of your choice

console.log(resultArray); // Output: [1, 11, 30, '1Y 11M 30D']
/* you can access each of Y, M, D separately from output array and can format as per your choice like aY-bM-cD or aYears-bMonths-cDays etc.*/

/*example: 
let Y, M, D;

Y = resultArray[0];
M = resultArray[1];
D = resultArray[2];

const customFormat = Y + 'year ' + M + 'months ' + D + 'days';
console.log(customFormat); // output: 1year 11months 30days
*/

```

## API Documentation

### `DatesYMD`

Represents a utility class for calculating the formatted and customized difference between two dates in all cases.

#### Create an instance of `DatesYMD`:

```javascript
const Formatter = new DatesYMD(firstDate, secondDate);
```

- **`firstDate`**: The first date in the format 'yyyy-mm-dd' or 'yyyy/mm/dd' or 'yyyy.mm.dd'.
- **`secondDate`**: The second date in the format 'yyyy-mm-dd' or 'yyyy/mm/dd' or 'yyyy.mm.dd'.

#### Methods:

**`diffArray`**
Calculates the difference between two dates and returns an array containing Y(years), M(months), D(days), and a formatted 'aY bM cD' difference string.

```javascript
const result = Formatter.diffArray();
```

- **`Returns:`**
  An array containing the calculated years, months, days, and the formatted difference.

**`formattedYMD()`**
Returns the formatted difference between two dates in aY bM cD(aYears bMonths cDays) format.

```javascript
const result = Formatter.formattedYMD();
```

- **`Returns:`** A string in the format 'aY bM cD'.

**`customizeFormat(yearUnit, monthUnit, dayUnit, partSeparator)`**
Customizes the difference using specified units and separators

```javascript
const result = Formatter.customizeFormat(
  yearUnit,
  monthUnit,
  dayUnit,
  partSeparator,
);
```

- **`Returns:`** A customized formatted difference string of form (a + yearUnit + partSeparator + b + monthUnit + partSeparator + c + dayUnit), eg. aYs-bMs-cDs etc.

For more informations, [See `diff-ymd-package documentation`](https://farhan7reza7.github.io/diff-ymd-package/DatesYMD.html)

## Contributing

If you find any issues or have suggestions for improvement, please open an issue or create a pull request on the GitHub repository.

See [CONTRIBUTING.md](CONTRIBUTING.md) for more informations.

## Best Practices:

### The code adheres to recommended practices for readability and maintainability, including:

- Meaningful variable and function names for clarity.
- Clear and concise comments to enhance understanding.
- Proper indentation and formatting for visual organization.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

[See License](https://github.com/farhan7reza7/diff-ymd-package/blob/main/LICENSE)

## History

For more details about what has changed in each version of this project.  
See [CHANGELOG.md](CHANGELOG.md).

[npm-image]: https://img.shields.io/npm/v/diff-ymd-package
[npm-url]: https://www.npmjs.com/package/diff-ymd-package
[npm-ci-image]: https://github.com/farhan7reza7/diff-ymd-package/actions/workflows/npm-publish-npm-registry.yml/badge.svg
[npm-ci-url]: https://github.com/farhan7reza7/diff-ymd-package/actions/workflows/npm-publish-npm-registry.yml
[github-image]: https://github.com/farhan7reza7/diff-ymd-package/actions/workflows/npm-publish-github-packages.yml/badge.svg
[github-url]: https://github.com/farhan7reza7/diff-ymd-package/actions/workflows/npm-publish-github-packages.yml
[ci-image]: https://github.com/farhan7reza7/diff-ymd-package/actions/workflows/pages/pages-build-deployment/badge.svg
[ci-url]: https://github.com/farhan7reza7/diff-ymd-package/actions/workflows/pages/pages-build-deployment
[license-image]: https://img.shields.io/github/license/farhan7reza7/diff-ymd-package
[licence-url]: https://opensource.org/licenses/MIT
