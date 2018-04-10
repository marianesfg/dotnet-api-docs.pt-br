### <a name="wpf-layout-rounding-of-margins-has-changed"></a>Layout WPF arredondamento das margens foi alterado

|   |   |
|---|---|
|Detalhes|A maneira como as margens são arredondadas, bem como as bordas e a tela de fundo dentro delas, foi alterada. Como resultado dessa alteração:<ul><li>A largura ou altura dos elementos pode aumentar ou reduzir em um pixel no máximo.</li><li>O posicionamento de um objeto pode ser movido até um pixel, no máximo.</li><li>Os elementos centralizados podem estar vertical ou horizontalmente fora do centro em, no máximo, um pixel.</li></ul>Por padrão, esse novo layout é habilitado somente para aplicativos que se destinam ao .NET Framework 4.6.|
|Sugestão|Desde que essa modificação tende a eliminar o recorte da direita ou inferior de controles WPF em DPIs alta, os aplicativos que versões anteriores do .NET Framework de destino, mas que estão em execução no .NET Framework 4.6 podem aceitar esse novo comportamento adicionando a seguinte linha ao <code>&lt;runtime&gt;</code> seção do arquivo App. config: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=false&quot; /&gt;</code>aplicativos que o .NET Framework 4.6 de destino, mas deseja que os controles do WPF para renderizar usando o algoritmo de layout anterior podem fazer isso, adicione a seguinte linha ao <code>&lt;runtime&gt;</code> seção do arquivo App. config: <code>&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.DoNotApplyLayoutRoundingToMarginsAndBorderThickness=true&quot; /&gt;</code>.|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Redirecionando|

