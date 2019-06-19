---
ms.openlocfilehash: 733bfb4740f3f274ba9ebb396749d313907d5fa6
ms.sourcegitcommit: 1bb00d2f4343e73ae8d58668f02297a3cf10a4c1
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2019
ms.locfileid: "63870379"
---
A partir do .NET Framework 4.7, esse método autentica usando o <xref:System.Security.Authentication.SslProtocols.None>, o que permite que o sistema operacional escolha o melhor protocolo a ser usado e bloqueie protocolos que não são seguros. No .NET Framework 4.6 (e .NET Framework 4.5 com os patches de segurança mais recentes instalados), as versões de protocolos TLS/SSL permitidas são 1.2, 1.1 e 1.0 (a menos você desabilite a criptografia forte ao editar o Registro do Windows).
