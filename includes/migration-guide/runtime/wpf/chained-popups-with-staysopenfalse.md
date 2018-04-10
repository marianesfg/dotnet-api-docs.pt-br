### <a name="chained-popups-with-staysopenfalse"></a>Encadeados pop-ups com StaysOpen = False

|   |   |
|---|---|
|Detalhes|Um pop-up com StaysOpen = False deve para fechar quando você clica fora o pop-up. Quando dois ou mais tais pop-ups são encadeadas (ou seja, um contém outro), muitos problemas, incluindo:<ul><li>Abra dois níveis, clique fora P2, mas dentro P1.  Nada acontece.</li><li>Abra dois níveis, clique fora P1.  Feche ambos os pop-ups.</li><li>Abrir e fechar a dois níveis.  Em seguida, tente abrir novamente o P2.  Nada acontece.</li><li>Tente abrir três níveis.  Não é possível.  (Nada acontece ou fechar os primeiros dois níveis, dependendo de onde você clicar.) Nesses casos (e outras variantes) agora funcionar como esperado.</li></ul>|
|Escopo|Microsoft Edge|
|Versão|4.7.1|
|Tipo|Tempo de execução|
|APIs afetadas|<ul><li><xref:System.Windows.Controls.Primitives.Popup.StaysOpen?displayProperty=nameWithType></li></ul>|

