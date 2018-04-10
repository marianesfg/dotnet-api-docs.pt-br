### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>Tratamento de métodos ObjectContext.CreateDatabase e DbProviderServices.CreateDatabase diferentes de exceção

|   |   |
|---|---|
|Detalhes|A partir do .NET 4.5, se houver falha na criação do banco de dados, os métodos <code>CreateDatabase</code> tentarão remover o banco de dados vazio. Se essa operação for bem-sucedida, a <xref:System.Data.SqlClient.SqlException?displayProperty=name> original será propagada (em vez da <xref:System.InvalidOperationException?displayProperty=name> que sempre era gerada no .NET 4.0)|
|Sugestão|Quando obtendo um <xref:System.InvalidOperationException?displayProperty=name> durante a execução <xref:System.Data.Objects.ObjectContext.CreateDatabase> ou <xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>, SQLExceptions agora também deve ser capturado.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|

