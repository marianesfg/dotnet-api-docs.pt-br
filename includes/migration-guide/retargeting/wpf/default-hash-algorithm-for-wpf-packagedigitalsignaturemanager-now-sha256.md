### <a name="the-default-hash-algorithm-for-wpf-packagedigitalsignaturemanager-is-now-sha256"></a>O algoritmo de hash padrão para WPF PackageDigitalSignatureManager agora é SHA256

|   |   |
|---|---|
|Detalhes|O <code>System.IO.Packaging.PackageDigitalSignatureManager</code> fornece funcionalidade para assinaturas digitais em relação aos pacotes WPF.  No .NET Framework 4.7 e versões anteriores, o algoritmo padrão (<xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType>) usado para assinar as partes de um pacote foi SHA1.  Devido a questões de segurança recentes com SHA1, esse padrão foi alterado para SHA256 iniciando com o .NET Framework 4.7.1.  Esta alteração afeta todos os pacotes de assinatura, incluindo documentos XPS.|
|Sugestão|Um desenvolvedor que deseja utilizar esta alteração e como alvo uma versão do framework abaixo .NET 4.7.1 ou um desenvolvedor que exige a funcionalidade anterior ao direcionamento .NET 4.7.1 ou posteriores podem define o seguinte sinalizador de AppContext adequadamente.  Um valor true resultará em SHA1 que está sendo usado como o algoritmo padrão; False resulta em SHA256.<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.MS.Internal.UseSha1AsDefaultHashAlgorithmForDigitalSignatures=true&quot;/&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Microsoft Edge|
|Versão|4.7.1|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.IO.Packaging.PackageDigitalSignatureManager.DefaultHashAlgorithm?displayProperty=nameWithType></li></ul>|

