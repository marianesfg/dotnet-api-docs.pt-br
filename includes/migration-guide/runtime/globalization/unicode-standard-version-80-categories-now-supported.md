### <a name="unicode-standard-version-80-categories-now-supported"></a>Categorias do Unicode standard versão 8.0 agora tem suportadas

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6.2, dados Unicode no framework foi atualizados de Unicode standard versão 6.3 para a versão 8.0.  Ao solicitar a categoria de caracteres Unicode no .NET Framework 4.6.2, alguns resultados podem não corresponder os resultados nas versões anteriores do .NET Framework.  Isso altera principalmente afeta Cherokee sílabas e sinais de vogais Tai Lue Novo e marcas de tom.|
|Sugestão|Examine o código e remover/alterar lógica que dependa embutido categorias de caracteres Unicode.|
|Escopo|Secundário|
|Versão|4.6.2|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Char.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.Char)?displayProperty=nameWithType></li><li><xref:System.Globalization.CharUnicodeInfo.GetUnicodeCategory(System.String,System.Int32)?displayProperty=nameWithType></li></ul>|

