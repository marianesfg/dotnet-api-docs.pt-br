### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable&lt;TResult&gt; sempre retorna armazenadas em cache instância

|   |   |
|---|---|
|Detalhes|A partir do .NET 4.5, <xref:System.Linq.Enumerable.Empty%60%601> sempre retorna uma instância interna em cache <xref:System.Collections.Generic.IEnumerable%601>. Anteriormente, <xref:System.Linq.Enumerable.Empty%60%601> seria cache vazio <xref:System.Collections.Generic.IEnumerable%601> no momento em que a API foi chamada, que significa que, em algumas condições em que <xref:System.Linq.Enumerable.Empty%60%601> foi chamado rapidamente e simultaneamente, diferentes instâncias do tipo podem ser retornadas para chamadas diferentes para o API.|
|Sugestão|Como o comportamento anterior não era determinístico, é improvável que o código dependesse dele. No entanto, na improbabilidade de que enumeráveis vazios estivessem sendo comparados e, às vezes, esperados que fosse diferentes, matrizes vazias explícitas deviam ser criadas (<code>new T[0]</code>) em vez de usar <xref:System.Linq.Enumerable.Empty%60%601>.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

