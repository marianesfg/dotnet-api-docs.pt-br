### <a name="incorrect-implementation-of-memberdescriptorequals"></a>Implementação incorreta de MemberDescriptor.Equals

|   |   |
|---|---|
|Detalhes|A implementação original do &quot;é igual a&quot; método foi comparando duas propriedades de cadeia de caracteres diferentes de objetos em comparação: nome da categoria à cadeia de caracteres de descrição. A correção é comparar &quot;categoria&quot; do primeiro objeto a ser &quot;categoria&quot; de um segundo e &quot;descrição&quot; para &quot;descrição&quot;. O valor de configuração MemberDescriptorEqualsReturnsFalseIfEquivalent pode ser definido como true para recusar o novo comportamento se direcionando 4.6.2 ou como false para habilitar essa correção quando a versão do framework de destino está abaixo 4.6.2.|
|Sugestão|Se seu aplicativo depende de MemberDescriptor.Equals, às vezes, retornando Falso quando descritores são equivalentes e estiver direcionamento 4.6.2 versão do .NET Framework, você tem várias opções:<ol><li>Fazer alterações de código para comparar &quot;categoria&quot; e &quot;descrição&quot; campos manualmente além de executar o método Equals.</li><li>Recusa essa alteração adicionando o seguinte valor para o arquivo App. config:</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Se seu aplicativo foi projetado 4.6.1 ou versão anterior do .NET Framework e você quiser que essa alteração habilitada, você pode definir a opção de compatibilidade como false, adicionando o seguinte valor para o arquivo App. config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.6.2|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

