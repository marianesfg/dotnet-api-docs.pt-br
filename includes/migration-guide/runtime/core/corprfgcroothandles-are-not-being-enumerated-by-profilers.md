### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>COR_PRF_GC_ROOT_HANDLEs não estão sendo enumeradas por criadores de perfil

|   |   |
|---|---|
|Detalhes|No v4.5.1 .NET Framework, a API de criação de perfil <code>RootReferences2()</code> incorretamente está retornando nunca <code>COR_PRF_GC_ROOT_HANDLE</code> (eles são retornados como <code>COR_PRF_GC_ROOT_OTHER</code> em vez disso). Esse problema é corrigido a partir do .NET Framework 4.6.|
|Sugestão|Esse problema foi corrigido no .NET Framework 4.6 e pode ser resolvido com a atualização para essa versão do .NET Framework.|
|Escopo|Secundário|
|Versão|4.5.1|
|Tipo|Tempo de execução|

