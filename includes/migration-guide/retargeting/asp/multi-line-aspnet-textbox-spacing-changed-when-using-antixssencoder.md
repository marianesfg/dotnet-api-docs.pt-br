### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>Espaçamento de ASP.Net de caixa de texto de várias linha alteradas ao usar AntiXSSEncoder

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.0, linhas extras eram inseridas entre as linhas de uma caixa de texto de várias linhas no postback, se usando o <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>. No .NET Framework 4.5, essas quebras de linhas extras não são incluídas. mas somente se o aplicativo Web for direcionado ao .NET 4.5|
|Sugestão|Lembre-se de que os aplicativos Web 4.0 redirecionados ao .NET 4.5 podem ter caixas de texto de várias linhas aprimoradas para não inserirem mais quebras de linhas extras. Se isso não for desejável, o aplicativo pode ter o comportamento antigo quando em execução no .NET Framework 4.5 direcionando o .NET Framework 4.0.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Redirecionando|

