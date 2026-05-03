# DON'T

Don't use single letters.

```js
let x = 1;

// vs

let someValue = 1;
```

Don't abbreviate names.

```js
function mRelScore(m1, m2) {}

// vs

function movieRelationScore(movie1, movie2) {}
```

Don't put types in the name (Hungarian notation)

```c
bool bIsValid;
int32_t iSpeed;
uint32_t uNumUsers;
char szUserName;
```

# DO

Use Endiannes / Smurfing / Molds

```bash
# big-endian = Most significant word FIRST
profitMonthlyMax

# little-endian = Most significant word LAST
maxMonthlyProfit
```

Add units to variables.

```js
function execute(delaySeconds) {}

// vs

function execute(delay) {}
```

# Refactor if you find yourself using `utils`.

```js
// utils.js
function assignDefaults() {}
function relationScore() {}
function moviesOnPage() {}
function topMoviesByRating() {}
function moviesByDirector() {}
function parseCookie() {}
function assignCookie() {}
```

```js
// movies.js
function assignDefaults() {}
function relationScore() {}

// pager.js
function moviesOnPage() {}

// movieCollection.js
function topMoviesByRating() {}
function moviesByDirector() {}

// cookie.js
function parseCookie() {}
function assignCookie() {}
```
