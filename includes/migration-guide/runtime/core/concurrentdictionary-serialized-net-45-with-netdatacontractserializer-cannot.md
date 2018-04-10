### <a name="a-concurrentdictionary-serialized-in-net-45-with-netdatacontractserializer-cannot-be-deserialized-by-net-451-or-452"></a>Não é possível desserializar um ConcurrentDictionary serializado no .NET 4.5 com NetDataContractSerializer pelo .NET 4.5.1 ou 4.5.2

|   |   |
|---|---|
|Detalhes|Devido a alterações internas para o tipo <xref:System.Collections.Concurrent.ConcurrentDictionary%602> objetos que são serializados com o .NET Framework 4.5 usando o <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> não pode ser desserializado no .NET Framework 4.5.1 ou em 4.5.2.Note o .NET Framework ou movendo-se em outros (de direção Serializando com o .NET Framework 4.5 e a desserialização de com o .NET Framework 4.5) funciona. Da mesma forma, serialização de versão entre todos os 4. x funciona com o 4.6.Serializing do .NET Framework e desserializar com uma única versão do .NET Framework não é afetado.|
|Sugestão|Se for necessário serializar e desserializar uma <xref:System.Collections.Concurrent.ConcurrentDictionary%602?displayProperty=name> entre o .NET Framework 4.5 e o .NET Framework 4.5.1/4.5.2, um serializador alternativo, como o <xref:System.Runtime.Serialization.DataContractSerializer?displayProperty=name> ou <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serializador deve ser usado em vez do <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name>. Como alternativa, porque esse problema é resolvido no .NET Framework 4.6, ele pode ser resolvido com a atualização para essa versão do .NET Framework.|
|Escopo|Secundário|
|Versão|4.5.1|
|Tipo|Tempo de execução|

