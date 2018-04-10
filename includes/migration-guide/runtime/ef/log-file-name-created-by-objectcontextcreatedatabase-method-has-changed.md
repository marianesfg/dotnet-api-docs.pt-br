### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>Nome do arquivo de log criado pelo método ObjectContext.CreateDatabase foi alterado de acordo com as especificações do SQL Server

|   |   |
|---|---|
|Detalhes|Quando o <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> método é chamado seja diretamente ou usando Code First com o provedor SqlClient e um valor de AttachDBFilename na cadeia de conexão, ele cria um arquivo de log denominado filename_log.ldf em vez de filename.ldf (onde filename é o nome do o arquivo especificado pelo valor de AttachDBFilename). Essa alteração melhora a depuração ao fornecer um arquivo de log chamado de acordo com especificações do SQL Server.|
|Sugestão|Se o nome do arquivo de log for importante para um aplicativo, o aplicativo deverá ser atualizado para esperar o formato de nome de arquivo _log.ldf padrão.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

