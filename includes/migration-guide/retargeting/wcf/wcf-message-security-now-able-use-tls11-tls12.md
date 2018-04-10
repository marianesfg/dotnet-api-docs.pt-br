### <a name="wcf-message-security-now-is-able-to-use-tls11-and-tls12"></a>Segurança de mensagens do WCF agora é possível usar o TLS 1.1 e TLS 1.2

|   |   |
|---|---|
|Detalhes|A partir do .NET Framework 4.7, os clientes podem configurar TLS 1.1 ou TLS 1.2 em segurança de mensagens do WCF além do SSL 3.0 e TLS 1.0 por meio de configurações do aplicativo.|
|Sugestão|No .NET Framework 4.7, suporte para 1.1 e TLS 1.2 em segurança de mensagens do WCF é desativado por padrão. Você pode habilitá-lo adicionando a seguinte linha ao <code>&lt;runtime&gt;</code> seção do arquivo App. config ou Web. config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableUsingServicePointManagerSecurityProtocols=false;Switch.System.Net.DontEnableSchUseStrongCrypto=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Redirecionando|

