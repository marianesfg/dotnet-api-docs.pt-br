### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>Acessando itens selecionados de um DataGrid WPF em um manipulador de eventos de UnloadingRow de DataGrid pode causar uma NullReferenceException

|   |   |
|---|---|
|Detalhes|Devido a um bug no .NET Framework 4.5, manipuladores de eventos para <xref:System.Windows.Controls.DataGrid> eventos que envolvem a remoção de uma linha podem causar uma <xref:System.NullReferenceException?displayProperty=name> seja lançada se acessarem o <xref:System.Windows.Controls.DataGrid>do <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> ou <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> propriedades.|
|Sugestão|Esse problema foi corrigido no .NET Framework 4.6 e pode ser resolvido com a atualização para essa versão do .NET Framework.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

