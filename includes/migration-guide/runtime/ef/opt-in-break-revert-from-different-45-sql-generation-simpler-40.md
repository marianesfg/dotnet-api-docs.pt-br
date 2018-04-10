### <a name="opt-in-break-to-revert-from-different-45-sql-generation-to-simpler-40-sql-generation"></a>Quebra de aceitação para reverter de geração de SQL 4.5 diferente para geração de SQL 4.0 mais simples

|   |   |
|---|---|
|Detalhes|Consultas que geram instruções de junção e contenham uma chamada para uma operação de limitação sem primeiro usar OrderBy agora produzir SQL mais simples. Depois de atualizar para o .NET Framework 4.5, essas consultas produzido SQL mais complicado do que as versões anteriores.|
|Sugestão|Esse recurso está desabilitado por padrão. Se o Entity Framework gera instruções de junção extras que provocam degradação do desempenho, você pode habilitar esse recurso, adicionando a seguinte entrada para o <code>&lt;appSettings&gt;</code> seção do arquivo de configuração (App. config) do aplicativo:<pre><code class="language-xml">&lt;add key=&quot;EntityFramework_SimplifyLimitOperations&quot; value=&quot;true&quot; /&gt;&#13;&#10;</code></pre>|
|Escopo|Transparente|
|Versão|4.5.2|
|Tipo|Tempo de execução|

