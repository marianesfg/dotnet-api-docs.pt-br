### <a name="winrt-stream-adapters-no-long-call-flushasync-automatically-on-close"></a>Adaptadores de fluxo do WinRT não chamar FlushAsync automaticamente ao fechar

|   |   |
|---|---|
|Detalhes|Em aplicativos da Windows Store, adaptadores de fluxo do Windows Runtime não chamar o método de FlushAsync do método Dispose.|
|Sugestão|Essa alteração deve ser transparente. Os desenvolvedores podem restaurar o comportamento anterior gravando um código como este:<pre><code class="language-csharp">using (var stream = GetWindowsRuntimeStream() as Stream)&#13;&#10;{&#13;&#10;// do something&#13;&#10;await stream.FlushAsync();&#13;&#10;}&#13;&#10;</code></pre>|
|Escopo|Transparente|
|Versão|4.5.1|
|Tipo|Tempo de execução|

