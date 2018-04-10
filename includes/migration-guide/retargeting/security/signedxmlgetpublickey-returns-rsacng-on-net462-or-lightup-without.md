### <a name="signedxmlgetpublickey-returns-rsacng-on-net462-or-lightup-without-retargeting-change"></a>SignedXml.GetPublicKey retorna RSACng em net462 (ou lightup) sem alteração no redirecionamento

|   |   |
|---|---|
|Detalhes|Iniciando com o .NET Framework 4.6.2, o tipo concreto do objeto retornado pelo <xref:System.Security.Cryptography.Xml.SignedXml.GetPublicKey%2A?displayProperty=nameWithType> método alterado (sem uma sutileza) de uma implementação de CryptoServiceProvider para uma implementação Cng. Isso ocorre porque a implementação é alterado de uso <code>certificate.PublicKey.Key</code> para uso interno <code>certificate.GetAnyPublicKey</code> que encaminha à <xref:System.Security.Cryptography.X509Certificates.RSACertificateExtensions.GetRSAPublicKey%2A?displayProperty=nameWithType>.|
|Sugestão|Começando com aplicativos em execução no .NET Framework 4.7.1, você pode usar a implementação de CryptoServiceProvider usada por padrão no .NET Framework 4.6.1 e versões anteriores, adicionando a seguinte configuração de alternar para o [tempo de execução](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md)seção do arquivo de configuração de aplicativo:<pre><code class="language-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.Security.Cryptography.Xml.SignedXmlUseLegacyCertificatePrivateKey=true&quot; /&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.6.2|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Security.Cryptography.Xml.SignedXml.CheckSignatureReturningKey(System.Security.Cryptography.AsymmetricAlgorithm@)?displayProperty=nameWithType></li></ul>|

