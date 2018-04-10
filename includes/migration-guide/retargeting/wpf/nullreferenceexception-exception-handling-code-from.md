### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException no código do ImageSourceConverter.ConvertFrom manipulação de exceção

|   |   |
|---|---|
|Detalhes|Um erro no código de manipulação de exceções <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> causou incorreta <xref:System.NullReferenceException?displayProperty=name> seja lançada em vez da exceção pretendida (por exemplo, <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>), essa alteração corrige esse erro para que o método agora lança a exceção à direita. Por padrão todos os aplicativos de destino do .NET Framework 4.6.2 e abaixo continuará a gerar <xref:System.NullReferenceException?displayProperty=name> para compatibilidade, desenvolvedores voltados para o .NET Framework 4.7 e acima deverá ver o direito exceptions.// substituir o espaço com um 'x', se aplicável|
|Sugestão|Os desenvolvedores que desejam reverter à obtenção <xref:System.NullReferenceException?displayProperty=name> quando direcionar o .NET Framework 4.7 pode adicionar/mesclagem a seguir ao arquivo App. config de seu aplicativo:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

