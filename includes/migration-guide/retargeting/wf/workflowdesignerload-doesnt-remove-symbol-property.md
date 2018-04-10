### <a name="workflowdesignerload-doesnt-remove-symbol-property"></a>WorkflowDesigner.Load não remove a propriedade de símbolo

|   |   |
|---|---|
|Detalhes|Durante o direcionamento do .NET Framework 4.5 no designer de fluxo de trabalho e carregar um fluxo de trabalho 3.5 re-hospedado com o <xref:System.Activities.Presentation.WorkflowDesigner.Load> método, uma <xref:System.Xaml.XamlDuplicateMemberException?displayProperty=name> é gerada ao salvar o fluxo de trabalho.|
|Sugestão|Esse bug manifestos somente durante o direcionamento do .NET Framework 4.5 no designer de fluxo de trabalho, portanto ele pode ser contornado definindo o <code>WorkflowDesigner.Context.Services.GetService&lt;DesignerConfigurationService&gt;().TargetFrameworkName</code> para Framework.Alternatively o .NET 4.0, o problema pode ser evitado usando o <xref:System.Activities.Presentation.WorkflowDesigner.Load(System.String)> método ao carregar o fluxo de trabalho em vez de <xref:System.Activities.Presentation.WorkflowDesigner.Load>.|
|Escopo|Principal|
|Versão|4.5|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Activities.Presentation.WorkflowDesigner.Load?displayProperty=nameWithType></li></ul>|

