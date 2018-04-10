### <a name="systemuriiswellformeduristring-method-returns-false-for-relative-uris-with-a-colon-char-in-first-segment"></a>Método System.Uri.IsWellFormedUriString retorna false para URIs relativos com um caractere de dois-pontos no primeiro segmento

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.5, <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)> tratará os URIs relativos com um <code>:</code> em seu primeiro segmento como não formado corretamente. Essa é uma alteração de <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> comportamento no .NET Framework 4.0 que foi feita para manter a conformidade de RFC3986.|
|Sugestão|Essa alteração (como muitas outras alterações URI) afetará apenas aplicativos voltados para o .NET Framework 4.5 (ou posterior). Para continuar usando o comportamento antigo, direcione o aplicativo de acordo com o .NET Framework 4.0. Como alternativa, verificação do URI antes de chamar <xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=name> procurando <code>:</code> caracteres que você deseja remover para fins de validação, se o antigo comportamento é desejável.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Uri.IsWellFormedUriString(System.String,System.UriKind)?displayProperty=nameWithType></li></ul>|

