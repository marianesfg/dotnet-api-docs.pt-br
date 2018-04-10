### <a name="itemsclear-does-not-remove-duplicates-from-selecteditems"></a>Items.Clear não remove duplicatas de SelectedItems

|   |   |
|---|---|
|Detalhes|Suponha que um seletor (com seleção múltipla habilitada) tem linhas duplicadas seu <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> coleção - o mesmo item aparece mais de uma vez.  Falha na remoção desses itens da fonte de dados (por exemplo, chamando Items.Clear) para removê-los de <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name>; somente a primeira instância é removida. Além disso, use subsequente de <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> (por exemplo, SelectedItems.Clear()) pode encontrar problemas como <xref:System.ArgumentException?displayProperty=name>, pois <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> contém itens que não estão mais na fonte de dados.|
|Sugestão|Atualize se possível para .NET 4.6.2.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=nameWithType></li></ul>|

