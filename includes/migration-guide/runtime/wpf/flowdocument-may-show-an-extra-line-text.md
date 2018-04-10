### <a name="flowdocument-may-show-an-extra-line-of-text"></a>FlowDocument pode mostrar uma linha extra de texto

|   |   |
|---|---|
|Detalhes|Em alguns casos, um <xref:System.Windows.Documents.FlowDocument> elemento exibirá uma linha extra de texto quando em execução no .NET Framework 4.5 em comparação com como ele exibidos quando executada no .NET Framework 4.0. Não há casos conhecidos da alteração, fazendo com que qualquer texto a ser exibido incorretamente ou illegibly, mas isso pode causar que anteriormente foi omitido do texto a ser exibido um <xref:System.Windows.Documents.FlowDocument>da exibição.|
|Sugestão|Em alguns casos, diminuindo a exibição propriedade do elemento PageHeight, um pode restaurar o número de linhas exibidas anterior.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Documents.FlowDocument.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Documents.FlowDocument.%23ctor(System.Windows.Documents.Block)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentReader.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.FlowDocumentPageViewer.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.DocumentPageView.%23ctor?displayProperty=nameWithType></li></ul>|

