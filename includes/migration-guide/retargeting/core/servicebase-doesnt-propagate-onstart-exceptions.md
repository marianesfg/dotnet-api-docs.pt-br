### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase não propaga OnStart exceções

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.7 e versões anteriores, exceções geradas durante a inicialização do serviço não são propagadas para o chamador de <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>. Começando com aplicativos voltados para o .NET Framework 4.7.1, o tempo de execução propaga exceções <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType> para serviços que falham ao iniciar.|
|Sugestão|Na inicialização do serviço, se houver uma exceção, essa exceção será propagada. Isso deve ajudar a diagnosticar os casos em que os serviços não serão iniciados. Se esse comportamento é desejável, você pode optar por fora dele, adicionando o seguinte <AppContextSwitchOverrides> elemento para o <runtime> seção do arquivo de configuração de aplicativo:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>Se seu aplicativo tem como alvo uma versão anterior ao 4.7.1, mas você deseja ter esse comportamento, adicione o seguinte <AppContextSwitchOverrides> elemento para o <runtime> seção do arquivo de configuração de aplicativo:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.7.1|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

