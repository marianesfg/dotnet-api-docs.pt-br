### <a name="wpf-textbox-defaults-to-undo-limit-of-100"></a>Padrões de caixa de texto do WPF para desfazer o limite de 100

|   |   |
|---|---|
|Detalhes|No .NET 4.5, o limite padrão da ação desfazer para uma caixa de texto do WPF é 100 (ao contrário de ser ilimitado como no .NET 4.0)|
|Sugestão|Se um limite de desfazer de 100 é muito baixo, o limite pode ser definido explicitamente com <xref:System.Windows.Controls.Primitives.TextBoxBase.UndoLimit>|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

