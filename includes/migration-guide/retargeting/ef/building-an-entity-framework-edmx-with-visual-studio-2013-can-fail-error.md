### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>Criar um edmx do Entity Framework com Visual Studio 2013 pode falhar com o erro MSB4062 se usando as tarefas EntityDeploySplit ou EntityClean

|   |   |
|---|---|
|Detalhes|Ferramentas de MSBuild 12.0 (incluídas no Visual Studio 2013) alterado locais de arquivos do MSBuild, fazendo com que os antigos arquivos de destino do Entity Framework seja inválido. O resultado é que as tarefas <code>EntityDeploySplit</code> e <code>EntityClean</code> falham porque não conseguem localizar <code>Microsoft.Data.Entity.Build.Tasks.dll</code>. Observe que essa quebra devido a uma alteração de conjunto de ferramentas (MSBuild/VS), não é devido a uma alteração do .NET Framework. Ela ocorrerá apenas no upgrade das ferramentas do desenvolvedor, não simplesmente no upgrade do .NET Framework.|
|Sugestão|Arquivos de destino do Entity Framework corrigidos para trabalhar com o início de layout do MSBuild nova no .NET Framework 4.6. O upgrade para essa versão do Framework corrigirá esse problema. Como alternativa, [esta](http://stackoverflow.com/a/24249247/131944) solução alternativa pode ser usada para aplicar patches diretamente aos arquivos de destino.|
|Escopo|Principal|
|Versão|4.5.1|
|Tipo|Redirecionando|

