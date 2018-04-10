### <a name="netdatacontractserializer-fails-to-deserialize-a-concurrentdictionary-serialized-with-a-different-net-version"></a>NetDataContractSerializer Falha ao desserializar um ConcurrentDictionary serializado com uma versão diferente do .NET

|   |   |
|---|---|
|Detalhes|Por design, o <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> pode ser usado somente se tanto a serialização e desserialização de extremidades compartilham os mesmos tipos CLR. Portanto, não há garantia de que um objeto serializado com uma versão do .NET Framework pode ser desserializado em uma versão diferente.<xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> é um tipo que é conhecido não para desserializar corretamente se serializado com o .NET Framework 4.5 ou anterior e desserializado com o .NET Framework 4.5.1 ou posterior.|
|Sugestão|Há um número de possíveis soluções alternativas para esse problema:<ul><li>Atualize o computador de serialização para usar o .NET Framework 4.5.1, também.</li><li>Use <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> em vez de <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> como isso não esperar os mesmos tipos CLR exatos em serialização e desserialização termina.</li><li>Use <xref:System.Collections.Generic.Dictionary%602?displayProperty=name> em vez de <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> desde que não apresentam esse determinado 4.5 -&gt;quebrar 4.5.1.</li></ul>|
|Escopo|Secundário|
|Versão|4.5.1|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Runtime.Serialization.NetDataContractSerializer.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li></ul>|

