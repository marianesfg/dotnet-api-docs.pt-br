### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute exporta como ObsoleteAttribute e DeprecatedAttribute em cenários de WinMD

|   |   |
|---|---|
|Detalhes|Quando você cria uma biblioteca de metadados do Windows (arquivo. winmd), o <xref:System.ObsoleteAttribute?displayProperty=name> atributo é exportado como ambos <xref:System.ObsoleteAttribute?displayProperty=name> e [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Sugestão|Recompilação de código-fonte existente que usa o <xref:System.ObsoleteAttribute?displayProperty=name> atributo pode gerar avisos durante o consumo de que o código do C + + CX ou JavaScript.We não é recomendável aplicar ambas <xref:System.ObsoleteAttribute?displayProperty=name> e [ Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) código em assemblies gerenciados; isso pode resultar em avisos de compilação.|
|Escopo|Microsoft Edge|
|Versão|4.5.1|
|Tipo|Redirecionando|

