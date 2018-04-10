### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath lança uma NullReferenceException

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6.2, o tempo de execução lança uma <code>T:System.NullReferenceException</code> ao recuperar um <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> valor que inclui caracteres nulos. No .NET Framework 4.6.1 e versões anteriores, o tempo de execução lança um <code>T:System.ArgumentNullException</code>.|
|Sugestão|Você pode fazer qualquer uma destas etapas para responder a essa alteração:<ul><li>Manipular o <code>T:System.NullReferenceException</code> se seu aplicativo estiver em execução no .NET Framework 4.6.2.</li><li>Atualizar para o .NET Framework 4.7, que restaura o comportamento anterior e gera um <code>T:System.ArgumentNullException</code>.</li></ul>|
|Escopo|Microsoft Edge|
|Versão|4.6.2|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

