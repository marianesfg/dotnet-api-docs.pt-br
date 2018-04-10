### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>Chamar DataGrid.CommitEdit de um manipulador de CellEditEnding descarta o foco

|   |   |
|---|---|
|Detalhes|Chamando <xref:System.Windows.Controls.DataGrid.CommitEdit> de uma da <xref:System.Windows.Controls.DataGrid?displayProperty=name>do <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> manipuladores de eventos faz com que o <xref:System.Windows.Controls.DataGrid?displayProperty=name> a perder o foco.|
|Sugestão|Esse bug foi corrigido no .NET Framework 4.5.2, portanto, ele pode ser evitado com a atualização do .NET Framework. Como alternativa, ele pode ser evitado selecionando explicitamente novamente o <xref:System.Windows.Controls.DataGrid?displayProperty=name> depois de chamar <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

