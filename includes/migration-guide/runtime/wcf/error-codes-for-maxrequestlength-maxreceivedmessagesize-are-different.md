### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>Códigos de erro para maxRequestLength ou maxReceivedMessageSize são diferentes

|   |   |
|---|---|
|Detalhes|Mensagens no WCF web serviços hospedados em serviços de informações da Internet (IIS) ou o servidor de desenvolvimento ASP.NET que excedem maxRequestLength (no ASP.NET) ou maxReceivedMessageSize (no WCF) erro diferente de ter o código de status HTTP de codeThe mudou de 400 (solicitação incorreta ) para 413 (entidade de solicitação muito grande) e as mensagens que excederem maxRequestLength ou a configuração de maxReceivedMessageSize lançar um <xref:System.ServiceModel.ProtocolException?displayProperty=name> exceção. Isso inclui os casos em que o modo de transferência é transmitido.|
|Sugestão|Essa alteração facilita a depuração em casos em que o comprimento da mensagem excede os limites permitidos pelo ASP.NET ou WCF. Você deve modificar qualquer código que executa o processamento com base em um código de status HTTP 400.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|

