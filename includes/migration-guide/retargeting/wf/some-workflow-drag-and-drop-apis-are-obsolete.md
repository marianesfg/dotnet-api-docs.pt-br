### <a name="some-workflow-drag-and-drop-apis-are-obsolete"></a>Algumas APIs de arrastar e soltar do fluxo de trabalho são obsoletos

|   |   |
|---|---|
|Detalhes|Esta API de arrastar e soltar do fluxo de trabalho está obsoleta e causará avisos do compilador se o aplicativo for recriado contra 4.5.|
|Sugestão|Novo <xref:System.Activities.Presentation.DragDropHelper?displayProperty=name> APIs que oferecem suporte a operações com vários objetos deve ser usado em vez disso. Como alternativa, os avisos de compilação podem ser suprimidos ou evitados usando um compilador mais antigo. Ainda há suporte para as APIs.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Activities.Presentation.DragDropHelper.DoDragMove(System.Activities.Presentation.WorkflowViewElement,System.Windows.Point)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetCompositeView(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDraggedModelItem(System.Windows.DragEventArgs)?displayProperty=nameWithType></li><li><xref:System.Activities.Presentation.DragDropHelper.GetDroppedObject(System.Windows.DependencyObject,System.Windows.DragEventArgs,System.Activities.Presentation.EditingContext)?displayProperty=nameWithType></li></ul>|

