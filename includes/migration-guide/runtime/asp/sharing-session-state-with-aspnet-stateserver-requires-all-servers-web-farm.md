### <a name="sharing-session-state-with-aspnet-stateserver-requires-all-servers-in-the-web-farm-to-use-the-same-net-framework-version"></a>Compartilhamento de estado de sessão com Asp.Net StateServer requer que todos os servidores no farm da web para usar a mesma versão do .NET Framework

|   |   |
|---|---|
|Detalhes|Ao habilitar <xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=name> de estado de sessão, todos os servidores no farm da web fornecida devem usar a mesma versão do .NET Framework para o estado deve ser compartilhado corretamente.|
|Sugestão|Certifique-se de atualizar as versões do .NET Framework em servidores web que compartilham o estado ao mesmo tempo.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Web.SessionState.SessionStateMode.StateServer?displayProperty=nameWithType></li></ul>|

