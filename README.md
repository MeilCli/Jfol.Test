# Jfol.Test

[Jfol](https://github.com/MeilCli/Jfol) test data for any implementation

Note: Experimental implementation

## Test Data
This test data expect implementation of 4 layer:
- Lexer
- AST Parser
- Semantic Analyzer
- Compiler

### Lexer
Lexer is converting to Token from raw string.

So test data is raw string and expected tokens.

Test Data Location: [tokens](tokens)

### AST Parser and Semantic Analyzer
AST Parser and Semantic Analyzer are converting to Nodes from Tokens. Different between Nodes and Tokens are AST(abstract syntax tree) and Array of Tokens. Converting Nodes by ASP Parser, but Nodes are incomplete as AST. So convert nodes complete as AST by Semantic Analyzer.

So test data is raw string and expected complete Nodes as AST, because imcomplete Nodes as AST will be different on any implementation.

Test Data Location: [nodes](nodes)

### Compiler
Compiler's job is to give conclusive result using by JSON and AST Nodes.

So test data is JSON and Jfol string and expected result.

Test Data Location: [texts](texts)

## License

[MIT License](LICENSE).
