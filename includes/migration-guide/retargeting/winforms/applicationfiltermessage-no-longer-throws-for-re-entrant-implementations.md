### <a name="applicationfiltermessage-no-longer-throws-for-re-entrant-implementations-of-imessagefilterprefiltermessage"></a>Application.FilterMessage não gera mais para implementações de reinserção de IMessageFilter.PreFilterMessage

|   |   |
|---|---|
|Detalhes|Antes do .NET Framework 4.6.1, chamada <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> com um <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> que chamado <xref:System.Windows.Forms.Application.AddMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> ou <xref:System.Windows.Forms.Application.RemoveMessageFilter(System.Windows.Forms.IMessageFilter)?displayProperty=name> (ao chamar também <xref:System.Windows.Forms.Application.DoEvents>) pode causar um <xref:System.IndexOutOfRangeException?displayProperty=name>. Começando com os aplicativos voltados para o .NET Framework 4.6.1, essa exceção não é gerada e filtros reentrantes conforme descrito acima podem ser usados.|
|Sugestão|Lembre-se que <xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)> não lançará para o reentrantes <xref:System.Windows.Forms.IMessageFilter.PreFilterMessage(System.Windows.Forms.Message@)> comportamento descrito acima. Isso afeta somente os aplicativos voltados para o .NET Framework 4.6.1.Apps direcionamento do .NET Framework 4.6.1 pode recusar essa alteração (ou aplicativos podem aceitar o direcionamento estruturas mais antigas) usando o [DontSupportReentrantFilterMessage](~/docs/framework/migration-guide/mitigation-custom-imessagefilter-prefiltermessage-implementations.md#mitigation) opção de compatibilidade.|
|Escopo|Microsoft Edge|
|Versão|4.6.1|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Windows.Forms.Application.FilterMessage(System.Windows.Forms.Message@)?displayProperty=nameWithType></li></ul>|

