### <a name="systemthreadingtaskstask-no-longer-throw-objectdisposedexception-after-object-is-disposed"></a>Threading não lançar ObjectDisposedException depois que o objeto é descartado

|   |   |
|---|---|
|Detalhes|Exceto para <xref:System.Threading.Tasks.Task.System%23IAsyncResult%23AsyncWaitHandle>, <xref:System.Threading.Tasks.Task?displayProperty=name> métodos não geram um <xref:System.ObjectDisposedException?displayProperty=name> exceção depois que o objeto é descartado. Essa alteração oferece suporte ao uso de tarefas em cache. Por exemplo, um método pode retornar uma tarefa em cache para representar uma operação já concluída em vez de alocar uma nova tarefa. Isso era impossível nas versões anteriores do .NET Framework porque qualquer consumidor da tarefa poderia descartá-los, o que a tornava inutilizável.|
|Sugestão|Lembre-se de que os métodos de tarefa não podem gerar <xref:System.ObjectDisposedException?displayProperty=name> em casos em que o objeto é descartado. Se um aplicativo dependia essa exceção saber que uma tarefa foi descartada, ele deve ser atualizado para verificar o status da tarefa explicitamente usando <xref:System.Threading.Tasks.Task.Status>.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|

