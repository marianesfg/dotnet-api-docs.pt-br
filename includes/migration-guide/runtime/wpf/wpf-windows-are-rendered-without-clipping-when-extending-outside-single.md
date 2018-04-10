### <a name="wpf-windows-are-rendered-without-clipping-when-extending-outside-a-single-monitor"></a>Windows WPF são renderizados sem recorte ao estender fora de um único monitor

|   |   |
|---|---|
|Detalhes|A execução do .NET Framework 4.6 no Windows 8 e posterior, toda a janela é processada sem recorte quando ele estende fora da exibição única em um cenário de vários monitor. Isso é diferente de versões anteriores do .NET Framework, que seriam clip windows WPF que estendida além de uma única exibição.|
|Sugestão|Esse comportamento (se ou não) pode ser definido explicitamente usando o <code>&lt;EnableMultiMonitorDisplayClipping&gt;</code> elemento <code>&lt;appSettings&gt;</code> no arquivo de configuração do aplicativo, ou definindo o <code>EnableMultiMonitorDisplayClipping</code> propriedade durante a inicialização do aplicativo.|
|Escopo|Secundário|
|Versão|4.6|
|Tipo|Tempo de execução|

