### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Moniker do Framework de destino ausente resulta em comportamento 4.0

|   |   |
|---|---|
|Detalhes|Aplicativos sem uma <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> aplicada no assembly nível executará automaticamente usando a semântica (quirks) do .NET Framework 4.0. Para garantir a alta qualidade, recomenda-se que todos os binários ser explicitamente atribuído com um <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> que indica a versão do .NET Framework que foram criados. Observe que usando um moniker do framework de destino em um arquivo de projeto fará com que o MSBuild aplicar automaticamente um <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Sugestão|Um <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> deve ser fornecido por meio de adicionar o atributo diretamente ao assembly ou especificando uma estrutura de destino no [arquivo de projeto ou por meio do Visual Studio GUI de propriedades de projeto](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Escopo|Principal|
|Versão|4.5|
|Tipo|Tempo de execução|

