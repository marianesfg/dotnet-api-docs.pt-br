### <a name="path-colon-checks-are-stricter"></a>Verificações de dois-pontos de caminho são mais rígidas

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6.2, várias alterações foram feitas para dar suporte a caminhos anteriormente sem suporte (tanto em tamanho e formato). Verifica a sintaxe de separador (vírgula) de unidade apropriada foram feitas mais correta, que tinha o efeito colateral de bloqueio alguns caminhos URI em Selecione algumas APIs de caminho em que eles são usados para ser tolerada.|
|Sugestão|Se passando um URI para APIs afetados, modifique a cadeia de caracteres para ser um caminho legal primeiro.<ul><li>Remover o esquema de URLs manualmente (por exemplo, remover <code>file://</code> de URLs)</li><li>Passar o URI para o <xref:System.Uri> de classe e usar <xref:System.Uri.LocalPath></li></ul>Como alternativa, você pode recusar a normalização de caminho novo definindo o <code>Switch.System.IO.UseLegacyPathHandling</code> switch AppContext como true.|
|Escopo|Microsoft Edge|
|Versão|4.6.2|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.IO.Path.GetDirectoryName(System.String)?displayProperty=nameWithType></li><li><xref:System.IO.Path.GetPathRoot(System.String)?displayProperty=nameWithType></li></ul>|

