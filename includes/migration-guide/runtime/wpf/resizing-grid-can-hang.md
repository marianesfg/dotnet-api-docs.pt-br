### <a name="resizing-a-grid-can-hang"></a>Redimensionar uma grade pode travar

|   |   |
|---|---|
|Detalhes|Um loop infinito pode ocorrer durante o layout de um <code>T:System.Windows.Controls.Grid</code> nas seguintes circunstâncias:<ul><li>Definições de linha contêm dois *-linhas, ambos os declarando um MinHeight e um MaxHeight.</li><li>Conteúdo do *-linhas não exceda o MaxHeight correspondente</li><li>Altura disponível da grade for excedida, o primeiro MinHeight (além de qualquer outro fixa ou automaticamente linhas)</li><li>O aplicativo tem como destino .net 4.7 ou aceita o algoritmo de 4.7 alocação, definindo <code>Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=false</code></li></ul>O loop também aconteceria com mais de duas linhas, ou no caso de análogo para colunas. O problema foi corrigido no .net 4.7.1.|
|Sugestão|Atualizar para o .net 4.7.1.  Como alternativa, se o algoritmo de 4.7 alocação não é necessário, você pode usar a seguinte configuração:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Controls.Grid.StarDefinitionsCanExceedAvailableSpace=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Tempo de execução|

