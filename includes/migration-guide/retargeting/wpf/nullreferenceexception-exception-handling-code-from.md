### <a name="nullreferenceexception-in-exception-handling-code-from-imagesourceconverterconvertfrom"></a>NullReferenceException no código de tratamento de exceções de ImageSourceConverter.ConvertFrom

|   |   |
|---|---|
|Detalhes|Um erro do código de tratamento de exceções de <xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)> fez com que um <xref:System.NullReferenceException?displayProperty=name> incorreto fosse gerado em vez da exceção pretendida (por exemplo, <xref:System.IO.DirectoryNotFoundException?displayProperty=name>, <xref:System.IO.FileNotFoundException?displayProperty=name>). Esta alteração corrige esse erro para que o método gere a exceção correta. Por padrão, todos os aplicativos destinados ao .NET Framework 4.6.2 e versões anteriores continuarão a gerar <xref:System.NullReferenceException?displayProperty=name> para compatibilidade. Os desenvolvedores destinados ao .NET Framework 4.7 e versões posteriores deverão ver as exceções corretas.//Substituir o espaço por um "x", se aplicável.|
|Sugestão|Os desenvolvedores que desejam reverter o recebimento de <xref:System.NullReferenceException?displayProperty=name> ao direcionar para o .NET Framework 4.7 podem adicionar/mesclar o seguinte ao arquivo App.config do aplicativo:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Media.ImageSourceConverter.OverrideExceptionWithNullReferenceException=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Windows.Media.ImageSourceConverter.ConvertFrom(System.ComponentModel.ITypeDescriptorContext,System.Globalization.CultureInfo,System.Object)?displayProperty=nameWithType></li></ul>|

