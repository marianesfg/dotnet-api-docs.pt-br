### <a name="il-ret-not-allowed-in-a-try-region"></a>IL ret não permitido em uma região try

|   |   |
|---|---|
|Detalhes|Ao contrário do compilador just-in-time JIT64, RyuJIT (usado em .NET 4.6) não permite que um IL ret instrução em uma região de try. Não retornar de uma região try é permitido pela especificação ECMA-335 e nenhum compilador gerenciado conhecido gera tal IL. No entanto, o compilador JIT64 executará essa IL se ela for gerada usando emissão de reflexo.|
|Sugestão|Se um aplicativo está gerando IL que inclui um opcode ret em uma região try, o aplicativo pode destino .NET 4.5 para usar o antigo JIT e evitar essa interrupção. Como alternativa, o IL gerado pode ser atualizado para retornar após a região try.|
|Escopo|Microsoft Edge|
|Versão|4.6|
|Tipo|Redirecionando|

