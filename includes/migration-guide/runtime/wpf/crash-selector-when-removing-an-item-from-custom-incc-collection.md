### <a name="crash-in-selector-when-removing-an-item-from-a-custom-incc-collection"></a>Ao remover um item de uma coleção de INCC personalizada de falhas no seletor

|   |   |
|---|---|
|Detalhes|Um <code>T:System.InvalidOperationException</code> pode ocorrer nas seguintes situações:<ul><li>A ItemsSource de um <code>T:System.Windows.Controls.Primitives.Selector</code> é uma coleção com uma implementação personalizada de <code>T:System.Collections.Specialized.INotifyCollectionChanged</code>.</li><li>O item selecionado será removido da coleção.</li><li>O <code>T:System.Collections.Specialized.NotifyCollectionChangedEventArgs</code> tem <code>P:System.Collections.Specialized.NotifyCollectionChangedEventArgs.OldStartingIndex</code> = -1 (indicando uma posição desconhecida).</li></ul>Pilha de chamadas da exceção começa em System.Windows.Threading.Dispatcher.VerifyAccess() em System.Windows.DependencyObject.GetValue (DependencyProperty dp) em System.Windows.Controls.Primitives.Selector.GetIsSelected (DependencyObject elemento) esta exceção pode ocorrer no .net 4.5, se o aplicativo tiver mais de um thread de Dispatcher. No .net 4.7 a exceção também pode ocorrer em aplicativos com um único thread Dispatcher. O problema foi corrigido no .net 4.7.1.|
|Sugestão|Atualizar para o .net 4.7.1.|
|Escopo|Secundário|
|Versão|4.7|
|Tipo|Tempo de execução|

