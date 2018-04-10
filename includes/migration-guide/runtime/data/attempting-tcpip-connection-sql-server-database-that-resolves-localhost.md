### <a name="attempting-a-tcpip-connection-to-a-sql-server-database-that-resolves-to-localhost-fails"></a>Tentar uma conexão TCP/IP para um banco de dados do SQL Server que resolve para `localhost` falhar

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6 e 4.6.1, tentando uma conexão TCP/IP para um banco de dados do SQL Server que resolve para <code>localhost</code> falha com o erro &quot;Ocorreu um erro relacionado à rede ou específico da instância ao estabelecer uma conexão com o SQL Server. O servidor não foi encontrado ou não estava acessível. Verifique se o nome da instância está correto e se o SQL Server está configurado para permitir conexões remotas. (provedor: Interfaces de rede do SQL, erro: 26 - erro ao localizar servidor/instância especificada)&quot;|
|Sugestão|Esse problema foi resolvido e o comportamento anterior restaurado no .NET Framework 4.6.2. Para se conectar a do Microsoft Azure do SQL Server que resolve para <code>localhost</code>, atualize para o .NET Framework 4.6.2.|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Tempo de execução|

