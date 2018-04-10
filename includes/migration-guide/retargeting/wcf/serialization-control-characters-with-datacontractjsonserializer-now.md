### <a name="serialization-of-control-characters-with-datacontractjsonserializer-is-now-compatible-with-ecmascript-v6-and-v8"></a>Serialização de caracteres de controle com DataContractJsonSerializer agora é compatível com ECMAScript V6 e V8

|   |   |
|---|---|
|Detalhes|O .NET framework 4.6.2 e versões anteriores, o <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer?displayProperty=name> não serializar alguns caracteres de controle especiais, como \b \f e \t, de forma que era compatível com os padrões ECMAScript V6 e V8. Começando com o .NET Framework 4.7, serialização desses caracteres de controle é compatível com ECMAScript V6 e V8.|
|Sugestão|Para aplicativos de destino do .NET Framework 4.7, esse recurso é habilitado por padrão. Se esse comportamento não for desejado, você poderá recusar esse recurso adicionando a seguinte linha na seção <code>&lt;runtime&gt;</code> do arquivo app.config ou web.config:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Runtime.Serialization.DoNotUseECMAScriptV6EscapeControlCharacter=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlDictionaryWriter,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Json.DataContractJsonSerializer.WriteObject(System.Xml.XmlWriter,System.Object)?displayProperty=nameWithType></li></ul>|

