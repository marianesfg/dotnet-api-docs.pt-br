### <a name="scrolling-a-wpf-treeview-or-grouped-listbox-in-a-virtualizingstackpanel-can-cause-a-hang"></a>Rolar um TreeView WPF ou ListBox agrupado em um VirtualizingStackPanel pode causar um travamento

|   |   |
|---|---|
|Detalhes|Em que a versão do .NET Framework 4.5, rolando um WPF <xref:System.Windows.Controls.TreeView?displayProperty=name> em uma pilha virtualizada painel pode causar a trava se houver margens no visor (entre os itens a <xref:System.Windows.Controls.TreeView?displayProperty=name>, por exemplo, ou em um elemento ItemsPresenter). Além disso, em alguns casos, itens de tamanhos diferentes no modo de exibição podem causar instabilidade, mesmo se não houver margens.|
|Sugestão|Esse bug pode ser evitado com a o upgrade para o .NET Framework 4.5.1. Como alternativa, as margens podem ser removidas de coleções de exibição (como <xref:System.Windows.Controls.TreeView?displayProperty=name>s) na pilha virtualizada painéis se todos os itens contidos são do mesmo tamanho.|
|Escopo|Principal|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel.SetIsVirtualizing(System.Windows.DependencyObject,System.Boolean)?displayProperty=nameWithType></li></ul>|

