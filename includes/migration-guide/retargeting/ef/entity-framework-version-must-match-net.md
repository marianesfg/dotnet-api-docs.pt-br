### <a name="entity-framework-version-must-match-the-net-framework-version"></a>Versão do Entity Framework deve corresponder à versão do .NET Framework

|   |   |
|---|---|
|Detalhes|A versão do entity framework deve corresponder com a versão do .NET framework. Entity Framework 5 é recomendado para o .NET 4.5. Há alguns problemas conhecidos com o EF 4. x em um projeto do .NET 4.5 em torno de <xref:System.ComponentModel.DataAnnotations>. No .NET 4.5, eles foram movidos para um assembly diferente, portanto, há problemas de determinar quais anotações para usar.|
|Sugestão|Atualização para o Entity Framework 5 para o .NET Framework 4.5|
|Escopo|Principal|
|Versão|4.5|
|Tipo|Redirecionando|

