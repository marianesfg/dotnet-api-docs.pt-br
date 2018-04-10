### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a>ClickOnce oferece suporte a SHA-256 em aplicativos voltados para o 4.0

|   |   |
|---|---|
|Detalhes|Anteriormente, um aplicativo ClickOnce com um certificado assinado com SHA-256 exigiria .NET 4.5 ou posterior esteja presente, mesmo que o aplicativo de destino 4.0. Agora, os aplicativos voltados para o 4.0 de ClickOnce podem executar em 4.0, mesmo se assinados com SHA-256.|
|Sugestão|Essa alteração remove essa dependência e permite que os certificados de SHA-256 ser usado para assinar aplicativos ClickOnce para .NET Framework 4 e versões anteriores.|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Redirecionando|

