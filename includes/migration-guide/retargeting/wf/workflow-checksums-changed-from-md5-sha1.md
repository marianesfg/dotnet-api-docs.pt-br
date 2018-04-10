### <a name="workflow-checksums-changed-from-md5-to-sha1"></a>Somas de verificação do fluxo de trabalho alteradas de MD5 para SHA1

|   |   |
|---|---|
|Detalhes|Para dar suporte a depuração com o Visual Studio, o tempo de execução do fluxo de trabalho gera uma soma de verificação para uma instância de fluxo de trabalho usando um algoritmo de hash. No .NET Framework 4.6.2 e versões anteriores, o hash de soma de verificação do fluxo de trabalho usado o algoritmo MD5, o que causou problemas em sistemas de FIPS. Começando com o .NET Framework 4.7, o algoritmo é SHA1. Se seu código persistiu esses somas de verificação, eles serão incompatíveis.|
|Sugestão|Se seu código não é possível carregar instâncias de fluxo de trabalho devido a uma falha de soma de verificação, tente definir a <code>AppContext</code> alternar &quot;Switch.System.Activities.UseMD5ForWFDebugger&quot; como true. No código:<pre><code class="language-csharp">System.AppContext.SetSwitch(&quot;Switch.System.Activities.UseMD5ForWFDebugger&quot;, true);&#13;&#10;</code></pre>Ou na configuração:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Activities.UseMD5ForWFDebugger=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.7|
|Tipo|Redirecionando|

