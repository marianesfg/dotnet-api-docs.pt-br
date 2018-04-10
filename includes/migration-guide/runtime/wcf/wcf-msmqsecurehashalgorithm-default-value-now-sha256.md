### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>Valor padrão de WCF MsmqSecureHashAlgorithm agora é SHA256

|   |   |
|---|---|
|Detalhes|Iniciando com o .NET Framework 4.7.1, a mensagem padrão do algoritmo no WCF para mensagens Msmq de assinatura é SHA256. No .NET Framework 4.7 e versões anteriores, a mensagem padrão do algoritmo de assinatura é SHA1.|
|Sugestão|Se você tiver problemas de compatibilidade com essa alteração no .NET Framework 4.7.1 ou posterior, você pode recusar a alteração, adicionando a seguinte linha ao <code>&lt;runtime&gt;</code>seção do arquivo App. config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.7.1|
|Tipo|Tempo de execução|

