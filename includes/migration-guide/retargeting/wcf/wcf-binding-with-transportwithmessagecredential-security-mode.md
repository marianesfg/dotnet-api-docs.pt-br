### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>Associação de WCF com o modo de segurança TransportWithMessageCredential

|   |   |
|---|---|
|Detalhes|A partir do .NET Framework 4.6.1, associação de WCF que usa o modo de segurança TransportWithMessageCredential pode ser configurada para receber mensagens com não assinado &quot;para&quot; cabeçalhos para chaves de segurança assimétrica. Por padrão, não assinado &quot;para&quot; cabeçalhos continuará a ser rejeitado em .NET 4.6.1. Eles só serão aceitos se um aplicativo aceita para esse novo modo de operação usando a opção de configuração Switch.System.ServiceModel.AllowUnsignedToHeader. Como esse é um recurso opcional, ele não deve afetar o comportamento de aplicativos existentes.|
|Sugestão|Como esse é um recurso de aceitação, ele não deve afetar o comportamento dos aplicativos existentes. Para controlar se o novo comportamento é usado ou não, use a seguinte configuração:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Transparente|
|Versão|4.6.1|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

