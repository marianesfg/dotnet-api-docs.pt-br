### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>Não é possível intermitentemente rolar até o último item no ItemsControls (como caixa de listagem e DataGrid) ao usar DataTemplates personalizado

|   |   |
|---|---|
|Detalhes|Em alguns casos, um bug no .NET Framework 4.5 está causando ItemsControls (como <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>, etc.) não rolar para o item inferior ao usar DataTemplates personalizado. Se houver uma tentativa de rolagem pela segunda vez (depois da rolagem de volta), ela funcionará.|
|Sugestão|Esse problema foi corrigido no .NET Framework 4.5.2 e pode ser solucionado com o upgrade para essa versão (ou uma versão posterior) do .NET Framework. Como alternativa, os usuários ainda podem arrastar as barras de rolagem para os itens finais nessas coleções, mas pode ser necessário tentar duas vezes para obter êxito.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|

