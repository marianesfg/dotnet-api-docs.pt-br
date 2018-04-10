### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>SqlBulkCopy usa a codificação de coluna de destino para cadeias de caracteres

|   |   |
|---|---|
|Detalhes|Quando dados são inseridos em uma coluna, o <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> usa a codificação da coluna de destino em vez da codificação padrão para os tipos <code>VARCHAR</code> e <code>CHAR</code>. Essa alteração elimina a possibilidade de corrompimento de dados causada pelo uso da codificação padrão quando a coluna de destino não usa a codificação padrão. Em casos raros, um aplicativo pode gerar uma exceção SqlException se a alteração na codificação produz os dados que é muito grandes para caber na coluna de destino.|
|Sugestão|Esperar que <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> não corromperá os dados devido a diferenças de codificação. Se cadeias de caracteres perto do limite de tamanho da coluna de destino estão sendo copiadas, talvez seja necessário ou codificar previamente dados (deve ser copiado para verificar se os dados serão ajustadas na coluna de destino) ou catch <xref:System.Data.SqlClient.SqlException?displayProperty=name>s.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

