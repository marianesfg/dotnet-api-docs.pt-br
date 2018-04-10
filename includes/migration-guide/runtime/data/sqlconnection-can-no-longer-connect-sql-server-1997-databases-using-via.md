### <a name="sqlconnection-can-no-longer-connect-to-sql-server-1997-or-databases-using-the-via-adapter"></a>SqlConnection não pode se conectar ao SQL Server 1997 ou bancos de dados usando o adaptador VIA

|   |   |
|---|---|
|Detalhes|Conexões com bancos de dados do SQL Server usando o [protocolo Virtual Interface Adapter (VIA)](https://technet.microsoft.com/library/ms191229%28v=sql.105%29.aspx) não são mais suportadas. O protocolo usado para se conectar a um banco de dados do SQL Server está visível na cadeia de conexão. Uma conexão VIA conterá:&lt;servername&gt;. Se este aplicativo está se conectando ao SQL por meio de um protocolo diferente de VIA (tcp: ou np: por exemplo), em seguida, nenhuma alteração significativa será encontrada. Além disso, não há suporte para conexões com o SQL Server 7 (1997).|
|Sugestão|O protocolo VIA foi preterido, um protocolo alternativo deve ser usado para se conectar a bancos de dados SQL. O protocolo mais comum usado é TCP/IP. As instruções para habilitar o protocolo TCP/IP podem ser encontradas [aqui](https://msdn.microsoft.com/library/bb909712.aspx). Se o banco de dados é acessado somente de dentro de uma intranet, o protocolo de pipes compartilhada pode fornecer um melhor desempenho se a rede estiver lenta.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String,System.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

