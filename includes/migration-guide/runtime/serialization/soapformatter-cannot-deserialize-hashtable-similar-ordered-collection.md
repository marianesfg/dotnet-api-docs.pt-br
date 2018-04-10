### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter não é possível desserializar a tabela de hash e ordenados semelhante objetos de coleção

|   |   |
|---|---|
|Detalhes|O <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> faz garante que os objetos serializados em uma versão do .NET Framework desserializará com êxito em uma versão diferente. Especificamente, alguns ordenados coleções (como <xref:System.Collections.Hashtable?displayProperty=name>) adicionou membros entre 4.0 e 4.5, de forma que os objetos desses tipos não é possível desserializar com o .NET 4.0, se eles foram serializados com o .NET 4.5. Observe que se os dados serializados forem serializados e desserializados com a mesma versão do .NET Framework, nenhum problema ocorrerá.|
|Sugestão|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> serialização deve ser substituída pelo <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> serialização ou <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> para ser resiliente em alterações do .NET Framework.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

