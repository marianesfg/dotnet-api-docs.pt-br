### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap com êxito converte ícones com quadros PNG em objetos de Bitmap

|   |   |
|---|---|
|Detalhes|Começando com os aplicativos que se destinam a .NET Framework 4.6 o <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> com êxito, o método converte ícones com quadros PNG em objetos de Bitmap. Em aplicativos de destino do .NET Framework 4.5.2 e versões anteriores, o <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> método lança um <xref:System.ArgumentOutOfRangeException> exceção se o objeto de ícone tiver quadros PNG. Essa alteração afeta os aplicativos que são recompilados para direcionar o .NET Framework 4.6 e que implementem um tratamento especial para o <xref:System.ArgumentOutOfRangeException> que é lançada quando um objeto de ícone tem quadros PNG. Ao executar no .NET Framework 4.6, a conversão é bem-sucedida, uma <xref:System.ArgumentOutOfRangeException> não é mais gerada e, portanto, o manipulador de exceção não é invocado.|
|Sugestão|Se esse comportamento é desejável, você poderá manter o comportamento anterior, adicionando o seguinte elemento para o <code>&lt;runtime&gt;</code> seção do arquivo App. config:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>Se o arquivo App. config já contiver o <code>AppContextSwitchOverrides</code> elemento, o novo valor deve ser mesclado com o atributo de valor como este:<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

