### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>Persistência do fluxo de trabalho SQL adiciona clusters e não permite valores nulos em algumas colunas de chave primária

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.7, as tabelas criadas para armazenamento de instância de fluxo de trabalho do SQL (SWIS) pelo script SqlWorkflowInstanceStoreSchema.sql usam chaves primárias em cluster. Por isso, as identidades não oferecem suporte a <code>null</code> valores. A operação de SWIS não é afetada por essa alteração. As atualizações foram feitas para dar suporte a replicação transacional do SQL Server.|
|Sugestão|O arquivo SQL SqlWorkflowInstanceStoreSchemaUpgrade.sql deve ser aplicado a instalações existentes para usar essa alteração. Novas instalações de banco de dados terá automaticamente a alteração.|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Tempo de execução|

