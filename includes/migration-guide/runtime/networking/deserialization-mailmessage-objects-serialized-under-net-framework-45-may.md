### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>Desserialização de objetos MailMessage serializado sob o .NET Framework 4.5 pode falhar

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.5, <xref:System.Web.Mail.MailMessage> objetos podem incluir caracteres não-ASCII. No .NET Framework 4, somente caracteres ASCII têm suporte. <xref:System.Web.Mail.MailMessage> objetos que contêm caracteres não ASCII e que são serializados com o .NET Framework 4.5 ou posterior não podem ser desserializados em .NET Framework 4.|
|Sugestão|Verifique se o seu código fornece tratamento de exceções ao desserializar um <xref:System.Web.Mail.MailMessage> objeto.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

