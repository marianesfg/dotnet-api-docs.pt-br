### <a name="serialport-background-thread-exceptions"></a>Exceções de thread de plano de fundo de SerialPort

|   |   |
|---|---|
|Detalhes|Threads criados com o plano de fundo <xref:System.IO.Ports.SerialPort> fluxos não encerrar o processo quando o sistema operacional exceções são lançadas. Em aplicativos voltados para o .NET Framework 4.7 e versões anteriores, um processo é encerrado quando uma exceção de sistema operacional é gerada em um thread em segundo plano criado com um <xref:System.IO.Ports.SerialPort> fluxo. Em aplicativos que o destino do .NET Framework 4.7.1 ou uma versão posterior, threads em segundo plano esperam eventos do sistema operacional relacionadas à porta serial ativa em podem falhar em alguns casos, como remoção repentina da porta serial.|
|Sugestão|Para aplicativos direcionam ao .NET Framework 4.7.1, você pode recusar o tratamento de exceção se não for desejável, adicionando o seguinte para o <code>&lt;runtime&gt;</code> seção do seu <code>app.config</code> arquivo:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Para aplicativos que se destinam a versões anteriores do .NET Framework mas executar no .NET Framework 4.7.1 ou posterior, você pode aceitar a exceção tratamento adicionando o seguinte para o <code>&lt;runtime&gt;</code> seção do seu <code>app.config</code> arquivo:<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.IO.Ports.DoNotCatchSerialStreamThreadExceptions=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Secundário|
|Versão|4.7.1|
|Tipo|Redirecionando|
|APIs afetadas|<ul><li><xref:System.IO.Ports.SerialPort?displayProperty=nameWithType></li></ul>|

