### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Alteração no comportamento de Task.WaitAll métodos com argumentos de tempo limite

|   |   |
|---|---|
|Detalhes|Comportamento de Task.WaitAll foi feito mais consistente no .NET 4.5.In o .NET Framework 4, esses métodos se comportam de forma inconsistente. Quando o tempo limite expirou, se uma ou mais tarefas foram concluídas ou canceladas antes da chamada de método, o método lançou uma exceção <xref:System.AggregateException?displayProperty=name>. Quando o tempo limite expirava, se nenhuma tarefa tivesse sido concluída ou cancelada antes da chamada de método, mas uma ou mais tarefas tivessem entrado nesses estados após a chamada de método, o método retornava false.<br/><br/>No .NET Framework 4.5, essas sobrecargas de método agora retornam falsos se todas as tarefas ainda estão em execução quando o intervalo de tempo limite expirou, e elas geram um <xref:System.AggregateException?displayProperty=name> exceção somente se uma tarefa de entrada foi cancelada (independentemente se ela estava antes ou depois do método chamar) e não há outras tarefas ainda estão em execução.|
|Sugestão|Se um <xref:System.AggregateException?displayProperty=name> sendo detectada como um meio de detectar uma tarefa que foi cancelada antes da chamada WaitAll que está sendo invocada, que o código em vez disso, deve fazer a detecção mesmo por meio da propriedade IsCanceled (por exemplo:. Any(t =&gt; t.IsCanceled)) desde que o .NET 4.6 somente lançará nesse caso se todas as tarefas esperadas são concluídas antes do tempo limite.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

