### <a name="profiling-aspnet-mvc4-apps-can-lead-to-fatal-execution-engine-error"></a>Aplicativos ASP.Net MVC4 de criação de perfil pode levar ao erro Fatal do mecanismo de execução

|   |   |
|---|---|
|Detalhes|Criadores de perfil usando assemblies NGEN /Profile podem falhar com perfil aplicativos ASP.NET MVC4 na inicialização com um 'exceção de mecanismo de execução de Fatal'|
|Sugestão|Esse problema é corrigido no .NET Framework 4.5.2. Como alternativa, o criador de perfil pode evitar esse problema especificando <code>COR_PRF_DISABLE_ALL_NGEN_IMAGES</code> em sua máscara de evento.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|

