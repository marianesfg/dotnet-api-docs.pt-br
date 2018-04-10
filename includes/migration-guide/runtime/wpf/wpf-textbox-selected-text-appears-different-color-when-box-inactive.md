### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>Texto da caixa de texto do WPF selecionado aparece uma cor diferente quando a caixa de texto está inativa

|   |   |
|---|---|
|Detalhes|No .NET 4.5, quando um controle de caixa de texto do WPF estiver inativo (não tem foco), o texto selecionado dentro da caixa aparecerá em uma cor diferente de quando o controle estiver ativo.|
|Sugestão|Comportamento anterior de (.NET 4.0) pode ser restaurado, definindo o <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> propriedade <code>false</code>.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

