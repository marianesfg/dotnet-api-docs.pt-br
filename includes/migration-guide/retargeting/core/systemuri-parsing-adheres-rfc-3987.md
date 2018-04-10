### <a name="systemuri-parsing-adheres-to-rfc-3987"></a>Análise de System. URI segue RFC 3987

|   |   |
|---|---|
|Detalhes|A análise de URI foi alterada de várias maneiras no .NET 4.5. No entanto, observe que essas alterações afetam apenas o código que se destinam ao NET 4.5. Se um binário for destinado ao .NET 4.0, o comportamento antigo será observado. As alterações na análise de URI no .NET 4.5 incluem:<ul><li>Análise de URI executará a normalização e o caractere de verificação de acordo com as regras IRI mais recentes da RFC 3987.</li><li>Formulário de normalização Unicode C só será executado na parte do host do URI.</li><li>Inválida mailto: URIs agora fará com que uma exceção.</li><li>Pontos à direita do final de um segmento de caminho agora são preservados.</li><li><code>file://</code> URIs não escapar a <code>?</code> caracteres.</li><li>Caracteres de controle Unicode <code>U+0080</code> por meio de <code>U+009F</code> não têm suporte.</li><li>Caracteres de vírgula <code>,</code> ou <code>%2c</code> não são automaticamente sem escape.</li></ul>|
|Sugestão|Se a semântica de análise de URI antiga do .NET 4.0 for necessária (geralmente não é), ela poderá ser usada visando o .NET 4.0. Isso pode ser feito usando um <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> no assembly ou por meio do sistema de projeto do Visual Studio da interface do usuário na página de propriedades de projeto.|
|Escopo|Principal|
|Versão|4.5|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Uri.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.String,System.UriKind)?displayProperty=nameWithType></li><li><xref:System.Uri.%23ctor(System.Uri,System.String)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.String,System.UriKind,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.String,System.Uri@)?displayProperty=nameWithType></li><li><xref:System.Uri.TryCreate(System.Uri,System.Uri,System.Uri@)?displayProperty=nameWithType></li></ul>|

