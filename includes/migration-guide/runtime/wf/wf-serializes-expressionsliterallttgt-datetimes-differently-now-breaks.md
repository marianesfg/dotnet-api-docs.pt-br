### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>O WF serializa Expressions.Literal&lt;T&gt; DateTimes diferentemente agora (quebras de analisadores XAML personalizados)

|   |   |
|---|---|
|Detalhes|Associado <xref:System.Windows.Markup.ValueSerializer> objeto converterá um <xref:System.DateTime?displayProperty=name> ou <xref:System.DateTimeOffset?displayProperty=name> objeto cujo segundo e <xref:System.DateTime.Millisecond?displayProperty=name> componentes são diferentes de zero e (para um <xref:System.DateTime?displayProperty=name> valor) cujo <xref:System.DateTime.Kind> propriedade não for especificada para o elemento de propriedade sintaxe, em vez de uma cadeia de caracteres. Essa alteração permite que os valores <xref:System.DateTime?displayProperty=name> e <xref:System.DateTimeOffset?displayProperty=name> completem um ciclo. Os analisadores XAML personalizados que assumem que a entrada XAML está na sintaxe de atributo não funcionará corretamente.|
|Sugestão|Essa alteração permite que os valores <xref:System.DateTime?displayProperty=name> e <xref:System.DateTimeOffset?displayProperty=name> completem um ciclo. Os analisadores XAML personalizados que assumem que a entrada XAML está na sintaxe de atributo não funcionará corretamente.|
|Escopo|Microsoft Edge|
|Versão|4.5|
|Tipo|Tempo de execução|

