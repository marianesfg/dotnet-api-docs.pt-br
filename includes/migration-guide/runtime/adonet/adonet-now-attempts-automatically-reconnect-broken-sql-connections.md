### <a name="adonet-now-attempts-to-automatically-reconnect-broken-sql-connections"></a>ADO.NET agora tentará reconectar-se automaticamente quebradas conexões do SQL

|   |   |
|---|---|
|Detalhes|A partir do .NET Framework 4.5.1, .NET Framework tentará reconectar-se automaticamente quebradas conexões do SQL. Embora normalmente isso vai assegurar aplicativos mais confiáveis, há casos de borda que um aplicativo precisa saber que a conexão foi perdida, para que ele possa tomar alguma ação após a reconexão.|
|Sugestão|Se esse recurso é indesejável devido a questões de compatibilidade, ele pode ser desativado, definindo o <xref:System.Data.SqlClient.SqlConnectionStringBuilder.ConnectRetryCount?displayProperty=name> propriedade de uma cadeia de caracteres de conexão (ou <xref:System.Data.SqlClient.SqlConnectionStringBuilder?displayProperty=name>) como 0.|
|Escopo|Microsoft Edge|
|Versão|4.5.1|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Data.IDbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Configuration.ConnectionStringSettings.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnection.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.ConnectionString?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnectionStringBuilder.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbConnectionStringBuilder.%23ctor(System.Boolean)?displayProperty=nameWithType></li></ul>|

