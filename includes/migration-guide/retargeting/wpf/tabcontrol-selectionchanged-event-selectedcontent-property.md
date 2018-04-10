### <a name="tabcontrol-selectionchanged-event-and-selectedcontent-property"></a>Evento TabControl SelectionChanged e propriedade SelectedContent

|   |   |
|---|---|
|Detalhes|Iniciando com o .NET Framework 4.7.1, um <xref:System.Windows.Controls.TabControl> atualiza o valor de seu <xref:System.Windows.Controls.TabControl.SelectedContent> propriedade antes de acionar o <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> evento, quando sua seleção é alterada. No .NET Framework 4.7 e versões anteriores, a atualização SelectedContent ocorreu depois do evento.|
|Sugestão|Aplicativos direcionam ao .NET Framework 4.7.1 ou posterior podem recusar isso alterar e usar o comportamento herdado, adicionando o seguinte para o <code>&lt;runtime&gt;</code> seção do arquivo de configuração do aplicativo:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Aplicativos para o .NET Framework 4.7 ou mas anterior estão em execução no .NET Framework 4.7.1 ou posterior podem habilitar o novo comportamento adicionando a seguinte linha ao <code>&lt;runtime&gt;</code> seção do arquivo. Configuration do aplicativo:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.TabControl.SelectionPropertiesCanLagBehindSelectionChangedEvent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.7.1|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.TabControl.SelectedContent?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.Primitives.Selector.SelectionChanged?displayProperty=nameWithType></li></ul>|

