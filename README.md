# mp-scraper
![npm](https://img.shields.io/npm/v/mp-scraper.svg)
[![Build Status](https://travis-ci.org/ISNIT0/mp-scraper.svg?branch=master)](https://travis-ci.org/ISNIT0/mp-scraper)
[![codecov](https://codecov.io/gh/ISNIT0/mp-scraper/branch/master/graph/badge.svg)](https://codecov.io/gh/ISNIT0/mp-scraper)
[![CodeFactor](https://www.codefactor.io/repository/github/isnit0/mp-scraper/badge)](https://www.codefactor.io/repository/github/isnit0/mp-scraper)
![NPM License](https://img.shields.io/npm/l/mp-scraper.svg)

## Example
```typescript
import { queryMw } from 'mp-scraper';

queryMw(
    {
        apiUrl: 'https://en.wikipedia.org/w/api.php',
    }, {
        coordinates: {
            coprop: {
                type: true,
                dim: false,
            },
        },
        categories: {
            cllimit: 40,
        },
        redirects: {
            rdlimit: 'max',
        },
    }, ['London', 'Paris'],
).then((out) => {
    console.log('Got Data:', out);
});
```

## Building
```bash
> ./build.sh
```

## Testing
```bash
> npm t
```

## License
[MIT](./LICENSE)