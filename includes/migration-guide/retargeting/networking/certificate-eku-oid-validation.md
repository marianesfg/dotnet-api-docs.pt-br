### <a name="certificate-eku-oid-validation"></a>Validação de OID de EKU de certificado

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.6 e o <xref:System.Net.Security.SslStream> ou <xref:System.Net.ServicePointManager> classes executam validação de OID (identificador) do objeto de uso avançado de chave (EKU). Uma extensão de uso avançado de chave (EKU) é uma coleção de identificadores de objeto (OIDs) que indicam que os aplicativos que usam a chave. Validação de OID de EKU usa retornos de chamada do certificado remoto para garantir que o certificado remoto tem os OIDs corretos para a finalidade pretendida.|
|Sugestão|Se essa alteração é desejável, você pode desabilitar a validação de OID de EKU de certificado adicionando o seguinte alterna para o [ \<AppContextSwitchOverrides >](~/docs/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element.md) no [ ` ](~/docs/framework/configure-apps/file-schema/runtime/runtime-element.md) do seu arquivo de configuração do aplicativo:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Net.DontCheckCertificateEKUs=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre> <blockquote> [!IMPORTANT] Essa configuração é fornecida para fins de compatibilidade com versões anteriores. Caso contrário, seu uso não é recomendado.</blockquote> |
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Net.Security.SslStream?displayProperty=nameWithType></li><li><xref:System.Net.ServicePointManager?displayProperty=nameWithType></li><li><xref:System.Net.Http.HttpClient?displayProperty=nameWithType></li><li><xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType></li><li><xref:System.Net.HttpWebRequest?displayProperty=nameWithType></li><li><xref:System.Net.FtpWebRequest?displayProperty=nameWithType></li></ul>|

