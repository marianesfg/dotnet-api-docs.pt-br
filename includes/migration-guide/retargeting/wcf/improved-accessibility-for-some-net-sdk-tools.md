### <a name="improved-accessibility-for-some-net-sdk-tools"></a>Acessibilidade aprimorada para algumas ferramentas do SDK do .NET

|   |   |
|---|---|
|Detalhes|No .NET Framework SDK 4.7.1, as ferramentas svcconfigedit.exe e svctraceviewer.exe foram aprimoradas, corrigindo problemas de acessibilidade variadas. A maioria delas foram pequenos problemas, como um nome que não está sendo definido ou determinados padrões de automação de interface do usuário não está sendo implementados corretamente. Embora muitos usuários não conhecer esses valores incorretos, os clientes que usam tecnologias assistenciais, como leitores de tela encontrará essas ferramentas SDK mais acessíveis. Certamente essas correções alterar alguns comportamentos anteriores, como ordem de foco do teclado. Para obter todas as correções de acessibilidade nessas ferramentas, você pode o seguinte ao seu arquivo App. config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.UseLegacyAccessibilityFeatures=false&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7.1|
|Tipo|Redirecionando|

