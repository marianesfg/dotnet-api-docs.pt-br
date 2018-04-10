### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>Foreach de variável de iterador agora tem escopo dentro da iteração, para a semântica de captura de fechamento é diferente (em C# 5)

|   |   |
|---|---|
|Detalhes|Começando com o c# 5 (Visual Studio 2012) <code>foreach</code> variáveis de iterador tem escopo dentro da iteração. Isso pode causar quebras se código anteriormente dependia as variáveis a não ser incluído no <code>foreach</code>do encerramento. O sintoma dessa alteração é que uma variável de iterador passada a um delegado é tratada como o valor que ele tem no momento em que o representante é criado, em vez do valor tem no momento que da invocação do delegado.|
|Sugestão|De maneira ideal, o código deve ser atualizado para esperar o novo comportamento do compilador. Se as semânticas antigas forem necessárias, a variável do iterador poderá ser substituída por uma variável separada que seja explicitamente colocada fora do escopo do loop.|
|Escopo|Principal|
|Versão|4.5|
|Tipo|Redirecionando|

