### <a name="wpf-datatemplate-elements-are-now-visible-to-uia"></a>Elementos do WPF DataTemplate agora estão visíveis para UIA

|   |   |
|---|---|
|Detalhes|Anteriormente, <xref:System.Windows.DataTemplate?displayProperty=name> elementos foram invisíveis para automação de interface do usuário. A partir da versão 4.5, a Automação da Interface do Usuário detectar esses elementos. Isso é útil em muitos casos, mas pode dividir os testes que dependem de árvores UIA não contêm <xref:System.Windows.DataTemplate?displayProperty=name> elementos.|
|Sugestão|Testes de automação de interface do usuário para este aplicativo pode ser necessário atualizado para a conta para a árvore UIA agora incluindo anteriormente invisível <xref:System.Windows.DataTemplate?displayProperty=name> elementos. Por exemplo, os testes que esperam que alguns elementos fiquem próximos uns dos outros agora podem precisar esperar elementos UIA anteriormente invisíveis entre eles. Ou os testes que dependem de determinadas contagens ou de índices para elementos UIA talvez precisem ser atualizados com novos valores.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.DataTemplate.%23ctor?displayProperty=nameWithType></li><li><xref:System.Windows.DataTemplate.%23ctor(System.Object)?displayProperty=nameWithType></li></ul>|

