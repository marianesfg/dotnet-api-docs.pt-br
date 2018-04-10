### <a name="only-tls-10-11-and-12-protocols-supported-in-systemnetservicepointmanager-and-systemnetsecuritysslstream"></a>Somente os protocolos Tls 1.0, 1.1 e 1.2 com suporte no System.Net.ServicePointManager e System.Net.Security.SslStream

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.6, o <xref:System.Net.ServicePointManager> e <xref:System.Net.Security.SslStream> classes só podem usar um dos três seguintes protocolos: TLS 1.0 por, TLS 1.1 ou TLS 1.2. Não há suporte para o protocolo SSL 3.0 e a criptografia RC4.|
|Sugestão|A atenuação recomendada é atualizar o aplicativo do lado do servidor para TLS 1.0 por, TLS 1.1 ou TLS 1.2. Se não for viável ou se os aplicativos cliente estiverem desfeitos, a classe <xref:System.AppContext?displayProperty=name> poderá ser usada para recusar esse recurso de duas maneiras:<ol><li>Definindo programaticamente compat switches no <xref:System.AppContext?displayProperty=name>, conforme explicado [aqui](http://blogs.msdn.com/b/dotnet/archive/2015/04/29/net-announcements-at-build-2015.aspx#dotnet46)</li><li>Adicionando a seguinte linha ao <code>&lt;runtime&gt;</code> seção do arquivo App. config: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.System.Net.DontEnableSchUseStrongCrypto=true&quot;/&gt;</code>;</li></ol>|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Net.SecurityProtocolType.Ssl3?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.None?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl2?displayProperty=nameWithType></li><li><xref:System.Security.Authentication.SslProtocols.Ssl3?displayProperty=nameWithType></li></ul>|

