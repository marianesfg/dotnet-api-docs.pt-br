### <a name="etw-event-names-cannot-differ-only-by-a-start-or-stop-suffix"></a>Nomes de eventos ETW não podem diferir somente por um sufixo "Start" ou "Stop"

|   |   |
|---|---|
|Detalhes|No .NET Framework 4.6 e 4.6.1, o tempo de execução lança uma <xref:System.ArgumentException> quando dois nomes de evento de rastreamento de eventos para Windows (ETW) diferem somente por um &quot;iniciar&quot; ou &quot;parar&quot; sufixo (como quando um evento é denominado <code>LogUser</code>e outro chamado <code>LogUserStart</code>). Nesse caso, o tempo de execução não pode construir a origem do evento, que não pode emitir nenhum log.|
|Sugestão|Para evitar a exceção, certifique-se de que nenhum nome de dois eventos diferem somente por um &quot;iniciar&quot; ou &quot;parar&quot; sufixo. Esse requisito foi retirado, iniciando com o .NET Framework 4.6.2; o tempo de execução pode resolver a ambiguidade de nomes de evento que diferem somente pelo &quot;iniciar&quot; e &quot;parar&quot; sufixo.|
|Escopo|Microsoft Edge|
|Versão|4.6|
|Tipo|Redirecionando|

