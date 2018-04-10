### <a name="wpf-pointer-based-touch-stack"></a>Pilha de toque baseada em ponteiro WPF

|   |   |
|---|---|
|Detalhes|Essa alteração adiciona a capacidade de habilitar um WM_POINTER opcional com base em pilha de toque/caneta do WPF.  Os desenvolvedores que não permitem explicitamente isso deverá ver nenhuma alteração no comportamento de toque/caneta do WPF. Atual problemas conhecidos com opcional WM_POINTER com base em pilha toque/caneta:<ul><li>Não há suporte para escrita à tinta em tempo real.</li><li>Ao escrever à tinta e StylusPlugins ainda funcionarão, eles serão processados no Thread da interface do usuário que pode resultar em baixo desempenho.</li><li>Alterações de comportamento devido a alterações na promoção de eventos de caneta/toque para eventos de mouse</li><li>Manipulação pode se comportar de maneira diferente</li><li>Arrastar/soltar não mostrará comentários apropriado para a entrada de toque</li><li>Isso não afeta a entrada de caneta</li><li>Arrastar/soltar não pode ser iniciado em eventos de toque/caneta</li><li>Isso pode travar o aplicativo até que a entrada do mouse seja detectada.</li><li>Em vez disso, os desenvolvedores devem iniciar a ação de arrastar e soltar usando eventos de mouse.</li></ul>|
|Sugestão|Os desenvolvedores que desejam habilitar esta pilha podem adicionar/mesclagem a seguir ao arquivo App. config de seu aplicativo:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Input.Stylus.EnablePointerSupport=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>Removendo isso ou definindo o valor como false desativa essa pilha opcional. Observe que esta pilha está disponível somente em criadores de atualização do Windows 10 e acima.|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Redirecionando|

