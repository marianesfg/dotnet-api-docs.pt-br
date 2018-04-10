### <a name="assemblies-compiled-with-regexcompiletoassembly-breaks-between-40-and-45"></a>Assemblies compilados com CompileToAssembly quebras entre 4.0 e 4.5

|   |   |
|---|---|
|Detalhes|Se um conjunto de expressões regulares compiladas é criado com o .NET Framework 4.5, mas destinos do .NET Framework 4, a tentativa de usar uma das expressões regulares, em que o assembly em um sistema com o .NET Framework 4 instalado gera uma exceção.|
|Sugestão|Para solucionar esse problema, pode-se seguir uma das seguintes alternativas:<ul><li>Compile o assembly que contém as expressões regulares do .NET Framework 4.</li><li>Use uma expressão regular interpretada.</li></ul>|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName)?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[])?displayProperty=nameWithType></li><li><xref:System.Text.RegularExpressions.Regex.CompileToAssembly(System.Text.RegularExpressions.RegexCompilationInfo[],System.Reflection.AssemblyName,System.Reflection.Emit.CustomAttributeBuilder[],System.String)?displayProperty=nameWithType></li></ul>|

