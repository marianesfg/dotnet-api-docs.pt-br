### <a name="targetframeworkname-for-default-app-domain-no-longer-defaults-to-null-if-not-set"></a>TargetFrameworkName para o domínio de aplicativo padrão não padrões para null se não definida

|   |   |
|---|---|
|Detalhes|O <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> era anteriormente nulo no domínio de aplicativo padrão, a menos que explicitamente definida. 4.6, a partir de <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> propriedade para o domínio de aplicativo padrão tem um valor padrão derivado de TargetFrameworkAttribute (se houver). Domínios de aplicativo padrão não continuará herdam suas <xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=name> do domínio de aplicativo padrão (que não o padrão será nulo na 4.6), a menos que ele seja substituído explicitamente.|
|Sugestão|O código deve ser atualizado para não depender do <xref:System.AppDomainSetup.TargetFrameworkName> que padroniza para nulo. Se for necessário que essa propriedade continue sendo avaliada como nula, ela poderá ser explicitamente definida para esse valor.|
|Escopo|Microsoft Edge|
|Versão|4.6|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.AppDomainSetup.TargetFrameworkName?displayProperty=nameWithType></li></ul>|

