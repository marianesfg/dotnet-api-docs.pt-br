### <a name="xsd-schema-validation-now-correctly-detects-violations-of-unique-constraints-if-compound-keys-are-used-and-one-key-is-empty"></a>Validação de esquema XSD agora detecta corretamente a violações de restrições exclusivas se forem usadas chaves compostas e uma chave está vazia

|   |   |
|---|---|
|Detalhes|As versões do .NET Framework anteriores a 4.6 tinham um bug que fazia com que a validação de XSD não detectasse restrições exclusivas em chaves compostas se uma das chaves estivesse vazia. No .NET Framework 4.6, esse problema foi corrigido. Isso resultará na validação mais correta, mas também pode resultar na não validação de algum XML que anteriormente seria validado.|
|Sugestão|Se menos rígida validação do .NET Framework 4.0 é necessário, o aplicativo de validação pode direcionar versão 4.5 (ou anterior) do .NET Framework. No entanto, ao redirecionar para o .NET 4.6, a análise do código deverá ser feita para garantir que não se espere que chaves compostas duplicadas (conforme descrito na descrição desse problema) sejam validadas.|
|Escopo|Microsoft Edge|
|Versão|4.6|
|Tipo|Redirecionando|

