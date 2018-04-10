### <a name="wpf-printing-stack-update"></a>Atualização de pilha de impressão do WPF

|   |   |
|---|---|
|Detalhes|Uso de APIs de impressão do WPF <xref:System.Printing.PrintQueue?displayProperty=name> agora chamar a API de pacote de documento da janela Imprimir em favor da API de impressão XPS agora substituído. A alteração foi feita com facilidade de manutenção em mente; os usuários, nem os desenvolvedores deverá ver as alterações no comportamento ou de uso da API. A nova pilha de impressão é habilitada por padrão durante a execução no Windows 10 criadores de atualização. A pilha de impressão antiga continuarão a funcionar como antes em versões mais antigas do Windows.|
|Sugestão|Para usar a pilha antiga na atualização do Windows 10 criadores, defina o <code>UseXpsOMPrinting</code> valor REG_DWORD de <code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code> chave do registro para <code>1</code>.|
|Escopo|Microsoft Edge|
|Versão|4.7|
|Tipo|Tempo de execução|

