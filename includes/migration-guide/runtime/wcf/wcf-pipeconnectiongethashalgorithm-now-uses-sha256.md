### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>WCF PipeConnection.GetHashAlgorithm agora usa SHA256

|   |   |
|---|---|
|Detalhes|Iniciando com o .NET Framework 4.7.1, o Windows Communication Foundation usa um hash SHA256 para gerar nomes aleatórios para pipes nomeados. No .NET Framework 4.7 e versões anteriores, era um hash SHA1.|
|Sugestão|Se você tiver problema de compatibilidade com essa alteração no .NET Framework 4.7.1 ou posterior, você pode recusar-adicionando a seguinte linha ao <code>&lt;runtime&gt;</code> seção do arquivo App. config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.7.1|
|Tipo|Tempo de execução|

