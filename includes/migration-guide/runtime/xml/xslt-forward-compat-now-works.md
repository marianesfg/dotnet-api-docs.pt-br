### <a name="xslt-forward-compat-now-works"></a>Compatibilidade de encaminhamento de XSLT agora funciona

|   |   |
|---|---|
|Detalhes|No .NET Framework 4, XSLT 1.0 compatibilidade tinha os seguintes problemas:<ul><li>O carregamento de uma folha de estilos falhava se sua versão era definida como 2.0 e o analisador encontrava uma compilação XSLT 1.0 não reconhecida.</li><li>A construção<code>xsl:sort</code> falhava ao classificar os dados se a versão de folha de estilo era definida como 1.1.</li></ul>No .NET Framework 4.5, esses problemas foram corrigidos e modo de compatibilidade do XSLT 1.0 funciona corretamente.|
|Sugestão|A maioria dos aplicativos deve ser afetada, mas os dados serão classificados diferentemente em alguns casos agora que XSL: Sort é respeitado. Se <code>xsl:sort</code> é usado em 1.1 folhas de estilo, confirme que aplicativos não foram dependendo da ordem sem classificação de dados. Se aplicativos dependem do comportamento de classificação de 4.0, remova <code>xsl:sort</code> da folha de estilos.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

