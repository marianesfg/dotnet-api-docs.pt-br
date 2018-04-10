### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException agora define as posições de linha corretamente

|   |   |
|---|---|
|Detalhes|Se o <xref:System.Xml.Linq.LoadOptions.SetLineInfo> valor é passado para o método de carga e ocorre um erro de validação, o <xref:System.Xml.Schema.XmlSchemaException.LineNumber> e <xref:System.Xml.Schema.XmlSchemaException.LinePosition> propriedades agora contêm informações de linha.|
|Sugestão|Código de tratamento de exceção que assume <xref:System.Xml.Schema.XmlSchemaException.LineNumber> e <xref:System.Xml.Schema.XmlSchemaException.LinePosition> não serão conjunto deve ser atualizado, pois essas propriedades serão agora definidas corretamente quando SetLineInfo é usada ao carregar o XML.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

