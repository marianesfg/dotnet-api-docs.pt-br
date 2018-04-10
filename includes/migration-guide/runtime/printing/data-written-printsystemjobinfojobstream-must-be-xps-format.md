### <a name="data-written-to-printsystemjobinfojobstream-must-be-in-xps-format"></a>Os dados gravados PrintSystemJobInfo.JobStream devem estar no formato XPS

|   |   |
|---|---|
|Detalhes|O <xref:System.Printing.PrintSystemJobInfo.JobStream> propriedade expõe o fluxo de trabalho de impressão. O usuário pode enviar dados brutos para os componentes de impressão do sistema operacional subjacente, escrevendo para esse fluxo. Começando com o .NET Framework 4.5 no Windows 8 e versões posteriores do sistema operacional Windows, os dados gravados nesse fluxo devem ser no formato XPS como um fluxo de pacote.|
|Sugestão|Para mostrar o conteúdo impresso, você tem duas opções:<ul><li>Use a classe <xref:System.Windows.Xps.XpsDocumentWriter> para produzir conteúdo de impressão. Essa é a alternativa recomendada.</li><li>Certifique-se de que os dados enviados para o fluxo retornado pelo <xref:System.Printing.PrintSystemJobInfo.JobStream> propriedade está no formato XPS como um fluxo de pacote.</li></ul>|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Printing.PrintSystemJobInfo.JobStream?displayProperty=nameWithType></li></ul>|

