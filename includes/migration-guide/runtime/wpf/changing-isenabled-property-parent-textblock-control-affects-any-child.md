### <a name="changing-the-isenabled-property-of-the-parent-of-a-textblock-control-affects-any-child-controls"></a>Alterar a propriedade IsEnabled do pai de um controle TextBlock afeta os controles filho

|   |   |
|---|---|
|Detalhes|Iniciando com o .NET Framework 4.6.2, alterando o <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> propriedade do pai de um <xref:System.Windows.Controls.TextBlock?displayProperty=name> controle afeta os controles filho (como hiperlinks e botões) da <xref:System.Windows.Controls.TextBlock?displayProperty=name> controle. No .NET Framework 4.6.1 e versões anteriores, controles dentro uma <xref:System.Windows.Controls.TextBlock?displayProperty=name> nem sempre reflete o estado do <xref:System.Windows.UIElement.IsEnabled?displayProperty=name> propriedade o <xref:System.Windows.Controls.TextBlock?displayProperty=name> pai.|
|Sugestão|nenhuma. Essa alteração está em conformidade com o comportamento esperado para controles dentro de um controle <xref:System.Windows.Controls.TextBlock?displayProperty=name>.|
|Escopo|Secundário|
|Versão|4.6.2|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.UIElement.IsEnabled?displayProperty=nameWithType></li></ul>|

