### <a name="calling-itemsrefresh-on-a-wpf-listbox-listview-or-datagrid-with-items-selected-can-cause-duplicate-items-to-appear-in-the-element"></a>Chamar Items.Refresh em uma caixa de listagem do WPF, ListView ou DataGrid com itens selecionados pode fazer com que os itens duplicados sejam exibidos no elemento

|   |   |
|---|---|
|Detalhes|O .NET Framework 4.5, chamando ListBox.Items.Refresh a partir do código enquanto os itens selecionados em um <xref:System.Windows.Controls.ListBox?displayProperty=name> pode fazer com que os itens selecionados ser duplicado na lista. Ocorre um problema semelhante com <xref:System.Windows.Controls.ListView?displayProperty=name> e <xref:System.Windows.Controls.DataGrid?displayProperty=name>. Isso foi corrigido no .NET Framework 4.6.|
|Sugestão|Esse problema pode ser contornado desmarcando os itens antes de maneira programática <xref:System.Windows.Data.CollectionView.Refresh?displayProperty=name> é chamado e, em seguida, novamente selecionando-os depois da chamada ser concluída. Como alternativa, esse problema foi corrigido no .NET Framework 4.6 e pode ser resolvido com o upgrade para essa versão do .NET Framework.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Data.CollectionView.Refresh?displayProperty=nameWithType></li></ul>|

