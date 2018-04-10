### <a name="webutilityhtmlencode-and-webutilityhtmldecode-round-trip-bmp-correctly"></a>WebUtility.HtmlEncode e BMP de ida e volta WebUtility.HtmlDecode corretamente

|   |   |
|---|---|
|Detalhes|Para aplicativos voltados para o .NET Framework 4.5, os caracteres que estão fora de viagem de plano multilíngue básico (BMP) corretamente quando eles são passados para o <xref:System.Net.WebUtility.HtmlDecode(System.String)> métodos.|
|Sugestão|Essa alteração deve não ter nenhum efeito em aplicativos atuais, mas para restaurar o comportamento original, defina o <code>targetFramework</code> atributo do <code>&lt;httpRuntime&gt;</code> elemento para uma cadeia de caracteres diferentes de &quot;4.5&quot;. Você também pode definir os atributos <code>unicodeEncodingConformance</code> e <code>unicodeDecodingConformance</code> do elemento de configuração <code>&lt;webUtility&gt;</code> para controlar esse comportamento independentemente da versão de destino do .NET Framework.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Net.WebUtility.HtmlEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlEncode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li></ul>|

