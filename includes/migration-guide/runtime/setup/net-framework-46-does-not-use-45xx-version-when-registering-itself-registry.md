### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>O .NET Framework 4.6 não usa uma versão 4.5.x.x quando se registrou no registro

|   |   |
|---|---|
|Detalhes|Como se pode esperar, a chave de versão definida no registro (em <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) para o .NET Framework 4.6 começa com '4.6', não '4.5'. Aplicativos que dependem destas chaves do registro para saber quais versões do .NET Framework estão instaladas em um computador devem ser atualizados para entender que 4.6 é uma nova versão possíveis, e um que seja compatível com 4.5 anterior versões.|
|Sugestão|Atualização de investigação para um .NET Framework 4.5 por aplicativos instalados procurando 4.5 chaves do registro aceitar também 4.6.|
|Escopo|Microsoft Edge|
|Versão|4.6|
|Tipo|Tempo de execução|

