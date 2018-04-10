### <a name="listsort-algorithm-changed"></a>Algoritmo de Sort alterado

|   |   |
|---|---|
|Detalhes|A partir do .NET Framework 4.5, <xref:System.Collections.Generic.List%601?displayProperty=name>do algoritmo de classificação foi alterada (para ser uma classificação introspectiva em vez de uma classificação rápida). <xref:System.Collections.Generic.List%601?displayProperty=name>da classificação nunca tiver sido estável, mas essa alteração pode causar a cenários diferentes classificar maneiras instável. Isso simplesmente significa que podem classificar itens equivalentes em ordens diferentes nas chamadas subsequentes da API.|
|Sugestão|Como o algoritmo de classificação antigo também foi instável (embora maneiras ligeiramente diferentes), não deve haver nenhum código que depende de itens equivalentes sempre classificação em uma ordem específica. Se houver instâncias de código, dependendo do que e sendo sorte com o comportamento antigo, esse código deve ser atualizado para usar um comparador que forma determinista classificará os itens na ordem desejada.|
|Escopo|Transparente|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Collections.Generic.List%601.Sort?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Comparison{%600})?displayProperty=nameWithType></li><li><xref:System.Collections.Generic.List%601.Sort(System.Int32,System.Int32,System.Collections.Generic.IComparer{%600})?displayProperty=nameWithType></li></ul>|

