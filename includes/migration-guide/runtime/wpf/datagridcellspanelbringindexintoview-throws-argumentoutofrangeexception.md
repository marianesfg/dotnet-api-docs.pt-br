### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView lança ArgumentOutOfRangeException

|   |   |
|---|---|
|Detalhes|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> funcionará assincronamente quando virtualização de coluna, mas as larguras de coluna ainda não foi determinadas.  Se as colunas são removidas antes que o trabalho assíncrono ocorre, um <xref:System.ArgumentOutOfRangeException?displayProperty=name> pode ocorrer.|
|Sugestão|Qualquer um dos seguintes:<ol><li>Atualizar para o .NET 4.7.</li><li>Instale o patch mais recente de manutenção para .NET 4.6.2.</li><li>Evitar a remoção de colunas até que a resposta assíncrona para <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> foi concluída.</li></ol>|
|Escopo|Microsoft Edge|
|Versão|4.6.2|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

