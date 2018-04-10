### <a name="item-scrolling-a-flat-list-with-items-of-different-pixel-height"></a>Uma lista simples com itens da altura de pixel diferente de item de rolagem

|   |   |
|---|---|
|Detalhes|Quando um <xref:System.Windows.Controls.ItemsControl?displayProperty=name> exibe uma coleção usando a virtualização (<code>IsVirtualizing=true</code>) e o item rolagem (<code>ScrollUnit=Item</code>), e quando o controle rola para exibir um item cuja altura em pixels difere de seus vizinhos, o <xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=name> itera em todos os itens da coleção. A interface do usuário não está respondendo durante a iteração; Se a coleção for grande, isso pode ser considerado uma parada. A iteração ocorre em outras circunstâncias, mesmo em versões anteriores do .net. Por exemplo, ele ocorre durante a rolagem de pixel (<code>ScrollUnit=Pixel</code>) ao encontrar um item com a altura de pixel diferente e quando o item de rolagem dados hierárquicos (como um <xref:System.Windows.Controls.TreeView?displayProperty=name> ou um <xref:System.Windows.Controls.ItemsControl?displayProperty=name> com o agrupamento ativado) ao encontrar um item com um número diferente de itens de descendentes de seus vizinhos. No caso de altura de pixel de item de rolagem e diferentes, a iteração foi introduzida no .net 4.6.1 corrigir bugs no layout de dados hierárquicos.  Ela não é necessária se os dados forem simples (nenhuma hierarquia) e .net 4.6.2 não fazê-lo nesse caso.|
|Sugestão|Se a iteração ocorre no .net 4.6.1, mas não em versões anteriores - ou seja, se o <xref:System.Windows.Controls.ItemsControl?displayProperty=name> é uma lista simples de rolagem do item-com itens da altura de pixel diferente - há duas soluções:<ol><li>Instale o .net 4.6.2.</li><li>Instale o hotfix 1605 HR para .net 4.6.1.</li></ol>|
|Escopo|Secundário|
|Versão|4.6.1|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.VirtualizingStackPanel?displayProperty=nameWithType></li></ul>|

