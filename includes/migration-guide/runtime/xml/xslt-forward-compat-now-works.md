### <a name="xslt-forward-compat-now-works"></a>Compatibilidade com versões posteriores do XSLT agora funciona

|   |   |
|---|---|
|Detalhes|No .NET Framework 4, a compatibilidade com versões posteriores do XSLT 1.0 tinha os seguintes problemas:<ul><li>O carregamento de uma folha de estilos falhava se sua versão era definida como 2.0 e o analisador encontrava uma compilação XSLT 1.0 não reconhecida.</li><li>A construção<code>xsl:sort</code> falhava ao classificar os dados se a versão de folha de estilo era definida como 1.1.</li></ul>No .NET Framework 4.5, esses problemas foram corrigidos, e o modo de compatibilidade com versões posteriores do XSLT 1.0 funciona corretamente.|
|Sugestão|A maioria dos aplicativos não deve ser afetada, mas os dados serão classificados diferentemente em alguns casos agora que xsl:sort é respeitado. Se <code>xsl:sort</code> for usado em folhas de estilo 1.1, verifique se os aplicativos dependem da ordem sem classificação dos dados. Se os aplicativos dependerem do comportamento de classificação de 4.0, remova <code>xsl:sort</code> da folha de estilos.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform?displayProperty=nameWithType></li></ul>|

