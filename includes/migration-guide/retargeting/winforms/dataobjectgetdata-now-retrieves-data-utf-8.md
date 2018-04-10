### <a name="dataobjectgetdata-now-retrieves-data-as-utf-8"></a>DataObject.GetData agora recupera dados como UTF-8

|   |   |
|---|---|
|Detalhes|Para aplicativos que são direcionados ao .NET Framework 4 ou executados no .NET Framework 4.5.1 ou versões anteriores, <code>DataObject.GetData</code> recupera dados em formato HTML como uma cadeia de caracteres ASCII. Como resultado, os caracteres não ASCII (caracteres cujos códigos ASCII são maiores que 0x7F) são representados por dois caracteres aleatórios. Para aplicativos que visam o .NET Framework 4.5 ou posterior e execução no .NET Framework 4.5.2, <code>DataObject.GetData</code> recupera dados em formato HTML como UTF-8, que representa os caracteres maiores que 0x7F corretamente.|
|Sugestão|Se você implementou uma solução alternativa para o problema de codificação com cadeias de caracteres formatada em HTML (por exemplo, codificação explicitamente a cadeia de caracteres HTML recuperado da área de transferência, passando-o para <xref:System.Text.UTF8Encoding.GetString(System.Byte[],System.Int32,System.Int32)?displayProperty=name>) e está redirecionamento seu aplicativo da versão 4 para 4.5, que solução alternativa deve ser removida. Se o comportamento antigo for necessária por algum motivo, o aplicativo pode direcionar o .NET Framework 4.0 para obter esse comportamento.|
|Escopo|Microsoft Edge|
|Versão|4.5.2|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Windows.DataObject.GetData(System.String)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.Type)?displayProperty=nameWithType></li><li><xref:System.Windows.DataObject.GetData(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

