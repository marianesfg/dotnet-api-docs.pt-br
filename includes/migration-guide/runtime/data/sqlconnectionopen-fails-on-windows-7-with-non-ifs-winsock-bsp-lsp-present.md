### <a name="sqlconnectionopen-fails-on-windows-7-with-non-ifs-winsock-bsp-or-lsp-present"></a>SqlConnection. Open falha no Windows 7 com IFS Winsock BSP ou LSP presente

|   |   |
|---|---|
|Detalhes|<xref:System.Data.SqlClient.SqlConnection.Open> e <xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)> falhar no .NET Framework 4.5 se executado em uma máquina Windows 7 com IFS Winsock BSP ou LSP está presente no computador. Para determinar se um não - IFS BSP ou LSP está instalado, use o <code>netsh WinSock Show Catalog</code> de comando e examine cada <code>Winsock Catalog Provider Entry</code> item que é retornado. Se o valor de Sinalizadores de Serviço tiver o bit <code>0x20000</code> definido, o provedor usará os identificadores do IFS e funcionará corretamente. Se o bit <code>0x20000</code> estiver limpo (não definido), trata-se de um BSP ou LSP não IFS.|
|Sugestão|Esse bug foi corrigido no .NET Framework 4.5.2, portanto, ele pode ser evitado com a atualização do .NET Framework. Como alternativa, ele pode ser evitado com a remoção de qualquer LSP Winsock não IFS instalado.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Data.SqlClient.SqlConnection.Open?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.OpenAsync(System.Threading.CancellationToken)?displayProperty=nameWithType></li></ul>|

