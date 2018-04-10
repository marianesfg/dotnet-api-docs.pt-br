### <a name="contractinvariant-or-contractrequirestexception-do-not-consider-stringisnullorempty-to-be-pure"></a>Contract.Invariant ou Contract.Requires<TException> não considere IsNullOrEmpty ser puro

|   |   |
|---|---|
|Detalhes|Para aplicativos direcionam ao .NET Framework 4.6.1, se a constante de contrato para <xref:System.Diagnostics.Contracts.Contract.Invariant%2A?displayProperty=nameWithType> ou o contrato de pré-condição para <xref:System.Diagnostics.Contracts.Contract.Requires%2A?displayProperty=nameWithType)> chamadas de <xref:System.String.IsNullOrEmpty%2A?displayProperty=nameWithType> método, o regravador emite CC1036 de aviso do compilador: &quot;detectado chamada ao método ' System.String.IsNullOrWhteSpace(System.String)' sem [puro] no método.&quot; Este é um compilador de aviso em vez de um erro do compilador.|
|Sugestão|Esse comportamento foi abordado em [Problema nº 339 no GitHub](https://github.com/Microsoft/CodeContracts/issues/339). Para eliminar esse aviso, você pode baixar e compilar uma versão atualizada do código-fonte para a ferramenta de contratos de código do [GitHub](https://github.com/Microsoft/CodeContracts/blob/master/README.md). As informações para download são encontradas no fim da página.|
|Escopo|Secundário|
|Versão|4.6.1|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Diagnostics.Contracts.Contract.Invariant(System.Boolean)?displayProperty=nameWithType></li><li><xref:System.Diagnostics.Contracts.Contract.Requires(System.Boolean)?displayProperty=nameWithType></li></ul>|

