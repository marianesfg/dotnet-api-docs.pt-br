### <a name="apps-published-with-clickonce-that-use-a-sha-256-code-signing-certificate-may-fail-on-windows-2003"></a>Aplicativos publicados com o ClickOnce que usam um certificado de assinatura de código do SHA-256 podem falhar no Windows 2003

|   |   |
|---|---|
|Detalhes|O executável é assinado com SHA256. Antes, ele era assinado com SHA1, independentemente se o certificado de assinatura de código era SHA-1 ou SHA-256. Isso se aplica a:<ul><li>Todos os aplicativos compilados com o Visual Studio 2012 ou posterior.</li><li>Os aplicativos compilados com o Visual Studio 2010 ou anteriores em sistemas com o .NET Framework 4.5.</li></ul>Além disso, se o .NET Framework 4.5 ou posterior estiver presente, o manifesto do ClickOnce também será assinado com certificados SHA-256 para SHA-256, independentemente da versão do .NET Framework na qual ele foi compilado.|
|Sugestão|A alteração na assinatura do ClickOnce executável afeta somente os sistemas Windows Server 2003; elas exigem que o KB 938397 sejam instalados. A alteração na assinatura do manifesto com SHA-256, mesmo quando um aplicativo tem como alvo o .NET Framework 4.0 ou versões anteriores apresenta uma dependência de tempo de execução no .NET Framework 4.5 ou posterior.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Redirecionando|

