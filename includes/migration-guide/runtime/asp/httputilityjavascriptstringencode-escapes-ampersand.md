### <a name="httputilityjavascriptstringencode-escapes-ampersand"></a>HttpUtility.JavaScriptStringEncode escapes ampersand

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.5, <xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name> ignora o e comercial (&amp;) caracteres.|
|Sugestão|Se seu aplicativo depende do comportamento anterior desse método, você poderá adicionar uma definição aspnet:JavaScriptDoNotEncodeAmpersand ao [elemento appSettings do ASP.NET](https://msdn.microsoft.com/library/hh975440.aspx) no seu arquivo de configuração.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

