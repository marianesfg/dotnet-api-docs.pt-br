---
ms.openlocfilehash: c28e3f97e02079905d591a7f27dc8d68d603c0bf
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2019
ms.locfileid: "63871557"
---
A barra invertida (\\) é um caractere reservado em um nome de mutex. Não use uma barra invertida (\\) em um nome de mutex, exceto conforme especificado na observação sobre como usar mutexes nas sessões do servidor de terminal. Caso contrário, uma <xref:System.IO.DirectoryNotFoundException> pode ser gerada, mesmo que o nome do mutex represente um arquivo existente.
