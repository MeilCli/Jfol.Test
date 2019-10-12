# Test data of tokens
This test data format is [TOML](https://github.com/toml-lang/toml).

## Test Data
```toml
# Single or Multiple data
[[test]]
name = "" # test name
jfol = '''
'''
  [[test.tokens]]
  text = ""
  token = "" # Token Type
```

test.jfol's string must cut last `\r\n` or `\n`(depend on runtime) when your test, because inserting this line breaks means readable test data.  
And line break(`\r\n` or `\n`) is expected `\n` on expected result, so replace `\r\n` to `\n` when testing.

## Token Type
```ts
export type TokenType =
    | "Text"
    | "Dollar"
    | "DoubleDollar"
    | "LeftParenthesis" /* ( */
    | "RightParenthesis" /* ) */
    | "LeftSquareBracket" /* [ */
    | "RightSquareBracket" /* ] */
    | "Dot"
    | "Colon"
    | "SemiColon"
    | "Comma"
    | "Space"
    | "DoubleQuotation" /* " */
    | "Equal"
    | "Plus"
    | "Minus"
    | "Slash"
    | "Asterisk"
    | "Percent"
    | "Bang" /* ! */
    | "Ampersand" /* & */
    | "VerticalLine" /* | */
    | "LessThan" /* < */
    | "GreaterThan" /* > */;
```