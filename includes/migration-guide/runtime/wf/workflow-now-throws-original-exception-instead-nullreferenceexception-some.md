### <a name="workflow-now-throws-original-exception-instead-of-nullreferenceexception-in-some-cases"></a>Fluxo de trabalho agora lança a exceção original em vez de NullReferenceException em alguns casos

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6.2 e versões anteriores, quando o método de execução de uma atividade de fluxo de trabalho gera uma exceção com um <code>null</code> valor para o <xref:System.Exception.Message> propriedade, o tempo de execução do fluxo de trabalho do System. Activities lança um <xref:System.NullReferenceException?displayProperty=name>, máscara de exceção original. Em 4.7 o Framework .NET, a exceção anteriormente mascarada é gerada.|
|Sugestão|Se seu código depende de tratamento de <xref:System.NullReferenceException?displayProperty=name>, alterá-la para capturar exceções que podem ser geradas de suas atividades personalizadas.|
|Escopo|Secundário|
|Versão|4.7|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Activities.CodeActivity.Execute(System.Activities.CodeActivityContext)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.AsyncCodeActivity%601.BeginExecute(System.Activities.AsyncCodeActivityContext,System.AsyncCallback,System.Object)?displayProperty=nameWithType></li><li><xref:System.Activities.WorkflowInvoker.Invoke?displayProperty=nameWithType></li></ul>|

