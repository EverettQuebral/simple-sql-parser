{<img src="https://travis-ci.org/EverettQuebral/simple-sql-parser.png" />}[https://travis-ci.org/EverettQuebral/simple-sql-parser]

sqlParser.js
============

Node.js Javascript library to parse CRUD (Create Retrieve Update Delete) SQL queries.

Note: this is a Fork of https://github.com/dsferruzza/sqlParser.js

## How to install

```
npm install simple-sql-parser
```

## How to use

Require the parser:

```js
var sqlParser = require('simple-sql-parser');
```

Parse a query:

```js
var statement = 'SELECT * FROM table WHERE field = value';
var result = sqlParser(statement);
console.log(result);
```

## Result
```js
{
	SELECT: [ '*' ],
	FROM: [ 'table' ],
	WHERE: { operator: '=', left: 'field', right: 'value' }
}
```

## Notes

sqlParser.js only supports these queries:
* SELECT
* INSERT
* UPDATE
* DELETE

sqlParser.js **is not a full SQL parser!**
It only support few SQL mechanisms and keywords.
Feel free to make a pull request/issue.

*sqlParser.js was made for @GestionAIR*

## License

The MIT License (MIT)
Copyright (c) 2013 David Sferruzza
 
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
 
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
 
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

