### <a name="wcf-addressheadercollection-now-throws-an-argumentexception-if-an-addressheader-element-is-null"></a>WCF AddressHeaderCollection agora gera ArgumentException se um elemento addressHeader é nulo

|   |   |
|---|---|
|Detalhes|Iniciando com o .NET Framework 4.7.1, o <xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})> construtor lança um <xref:System.ArgumentException> se um dos elementos é <code>null</code>. No .NET Framework 4.7 e versões anteriores, nenhuma exceção é lançada.|
|Sugestão|Se você encontrar problemas de compatibilidade com essa alteração no .NET Framework 4.7.1 ou uma versão posterior, você pode recusar-adicionando a seguinte linha ao <code>&lt;runtime&gt;</code> seção do arquivo App. config:<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.DisableAddressHeaderCollectionValidation=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.7.1|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.ServiceModel.Channels.AddressHeaderCollection.%23ctor(System.Collections.Generic.IEnumerable{System.ServiceModel.Channels.AddressHeader})?displayProperty=nameWithType></li></ul>|

