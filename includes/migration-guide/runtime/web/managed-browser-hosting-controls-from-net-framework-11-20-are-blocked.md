### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>Controles de hospedagem de navegador gerenciado do .NET Framework 1.1 e 2.0 estão bloqueados

|   |   |
|---|---|
|Detalhes|Hospedar esses controles é bloqueado no Internet Explorer.|
|Sugestão|O Internet Explorer falhará ao iniciar um aplicativo que usa o navegador gerenciado que hospeda controles. O comportamento anterior pode ser restaurado, definindo o valor de EnableIEHosting da subchave do registro <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> para <code>1</code> para x86 sistemas e processos de 32 bits em x64 sistemas e definindo o <code>EnableIEHosting</code> o valor da subchave do registro <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code>para <code>1</code> para processos de 64 bits em x64 de sistemas.|
|Escopo|Secundário|
|Versão|4.5|
|Tipo|Tempo de execução|

