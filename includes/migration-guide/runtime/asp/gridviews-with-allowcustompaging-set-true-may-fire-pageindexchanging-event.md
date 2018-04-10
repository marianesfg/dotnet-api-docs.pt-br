### <a name="gridviews-with-allowcustompaging-set-to-true-may-fire-the-pageindexchanging-event-when-leaving-the-final-page-of-the-view"></a>GridViews com AllowCustomPaging definida como true pode acionar o evento de PageIndexChanging ao deixar a página final do modo de exibição

|   |   |
|---|---|
|Detalhes|Faz com que um bug no .NET Framework 4.5 <xref:System.Web.UI.WebControls.GridView.PageIndexChanging?displayProperty=name> a ser acionado, às vezes, não para <xref:System.Web.UI.WebControls.GridView?displayProperty=name>s habilitou <xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=name>.|
|Sugestão|Esse problema foi corrigido no .NET Framework 4.6 e pode ser resolvido com a atualização para essa versão do .NET Framework. Como uma solução alternativa, o aplicativo pode fazer um BindGrid explícita em qualquer <code>Page_Load</code> que alcance essas condições (o <xref:System.Web.UI.WebControls.GridView?displayProperty=name> está na última página e última<xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name> é diferente do <xref:System.Web.UI.WebControls.GridView.PageSize?displayProperty=name>). Como alternativa, o aplicativo pode ser modificado para permitir paginação (em vez de paginação personalizada), como esse cenário não demonstram o problema.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Web.UI.WebControls.GridView.AllowCustomPaging?displayProperty=nameWithType></li></ul>|

