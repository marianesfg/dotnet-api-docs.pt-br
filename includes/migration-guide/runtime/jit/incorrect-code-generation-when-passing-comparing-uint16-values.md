### <a name="incorrect-code-generation-when-passing-and-comparing-uint16-values"></a>Geração de código incorreto quando passando e comparando valores UInt16

|   |   |
|---|---|
|Detalhes|Devido às alterações introduzidas no .NET Framework 4.7, em alguns casos o código gerado pelo compilador JIT em aplicativos em execução em que o .NET Framework 4.7 incorretamente compara dois <code>T:System.UInt16</code> valores. Para obter mais informações, consulte [problema #11508: silenciosa codegen incorreto quando passando e comparando args ushort](https://github.com/dotnet/coreclr/issues/11508) em GitHub.com.|
|Sugestão|Se você encontrar problemas na comparação de valores de 16 bits sem sinal no .NET Framework 4.7, atualize para o .NET Framework 4.7.1.|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Tempo de execução|

