### <a name="appdomainsetupdynamicbase-is-no-longer-randomized-by-userandomizedstringhashalgorithm"></a>AppDomainSetup.DynamicBase não é aleatória por UseRandomizedStringHashAlgorithm

|   |   |
|---|---|
|Detalhes|Antes do .NET Framework 4.6, o valor de <xref:System.AppDomainSetup.DynamicBase> seria aleatório entre domínios de aplicativos ou processos, se UseRandomizedStringHashAlgorithm foi habilitada no arquivo de configuração do aplicativo. A partir do .NET Framework 4.6 <xref:System.AppDomainSetup.DynamicBase> retornará um resultado estável entre instâncias diferentes da execução de um aplicativo e entre domínios de aplicativo diferente. Bases de dados dinâmicos ainda serão diferentes para diferentes aplicativos. Essa alteração só remove o elemento de nomenclatura aleatório para instâncias diferentes do mesmo aplicativo.|
|Sugestão|Lembre-se que habilitar <code>UseRandomizedStringHashAlgorithm</code> não resultará em <xref:System.AppDomainSetup.DynamicBase> sendo aleatória. Se for necessária uma base aleatória, devem ser produzido no código do aplicativo, em vez de por meio dessa API.|
|Escopo|Microsoft Edge|
|Versão|4.6|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.AppDomainSetup.DynamicBase?displayProperty=nameWithType></li></ul>|

