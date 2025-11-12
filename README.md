# DIO-CyberSec

Projetos de pesquisa em CyberSecurity (Ransomware & Keylogger)

Aviso ético e legal
Este repositório descreve, em termos gerais, dois projetos de pesquisa desenvolvidos para fins educacionais e de estudo (um demonstrador de ransomware e um demonstrador de keylogger). Nenhum código malicioso é publicado aqui. O objetivo do README é explicar o funcionamento em alto nível, os riscos associados e como prevenir/mitigar tais ameaças. Publicar, distribuir ou executar ferramentas maliciosas fora de ambientes controlados pode ser ilegal e anti-ético. Siga sempre políticas de divulgação responsável, leis locais e regras da sua instituição. 
Cyber Threat Alliance


Visão Geral

# Pesquisa: Demonstrações educativas em CyberSecurity — Ransomware & Keylogger

**Aviso:** Conteúdo educacional — nenhum código malicioso está publicado neste repositório. Uso indevido é proibido. Consulte as leis locais e procedimentos de divulgação responsável antes de qualquer teste.

## Objetivo
Este repositório documenta, em termos gerais, dois projetos desenvolvidos para estudo: um demonstrador de ransomware (apenas para laboratório) e um demonstrador de keylogger (apenas para laboratório). O intuito é descrever conceitos, riscos e medidas de mitigação — sem publicar código executável.

## Descrições (alto nível)
- **Ransomware (demonstrador):** Ransomware — descrição (alto nível)

Objetivo educacional: demonstrar o ciclo básico de cifragem de arquivos e a lógica de “nota de resgate” em um ambiente isolado (máquina virtual ou laboratório de testes).

Como funciona (resumo sem detalhes operacionais):

Gera-se uma chave simétrica (um segredo único) para cifrar e decifrar dados.

Lista-se arquivos alvo conforme critérios (por exemplo, extensões ou diretórios) e aplica-se uma operação de cifragem sobre o conteúdo desses arquivos.

Cria-se uma nota de resgate para informar a vítima sobre a cifragem.

Um componente separado (opcional) pode receber/usar a chave para recuperação, caso a chave seja preservada.

Ponto técnico relevante: no contexto de demonstração, bibliotecas modernas de criptografia (ex.: Fernet/AES) provêm confidencialidade, mas o uso responsável exige cuidado com geração, armazenamento e proteção da chave; o abuso desse fluxo é o que torna ransomware perigoso.
- **Keylogger (demonstrador):** Objetivo educacional: demonstrar como entradas de teclado podem ser capturadas e como logs podem ser exfiltrados para análise em um ambiente controlado.

Como funciona (resumo sem detalhes operacionais):

Um componente monitora eventos do sistema (teclas) e acumula um registro (log).

Periodicamente o registro é agregado e transmitido a um destino (ex.: envio por e-mail ou outra via) para análise posterior.

Em pesquisa, esse padrão permite estudar métodos de persistência, evasão, e técnicas de exfiltração.

Risco técnico: keyloggers podem capturar credenciais, números de cartão, mensagens privadas e outros dados confidenciais; por isso, são considerados ferramentas de alto risco

## Perigos associados
- Ransomware: perda de acesso/dados e impacto operacional.  
- Keylogger: vazamento de credenciais e dados sensíveis.  
(Ver referências técnicas e recomendações de mitigação neste README.)

## Mitigação e boas práticas (resumo)
- Backups regulares e testados (offline/immutáveis).  
- Manter sistemas atualizados; usar EDR/AV atualizados.  
- Princípio do menor privilégio e segmentação de rede.  
- Autenticação multifator e gerenciadores de senha.  
- Inspeção física para prevenir keyloggers de hardware.

## Ética e publicação
- Não publicar código que possa ser reutilizado maliciosamente.  
- Publicar apenas resultados sanitizados, análises e pseudocódigo.  
- Seguir canais de responsible disclosure se vulnerabilidades reais forem encontradas.

## Referências selecionadas
- Guias e recomendações de agências e fornecedores (CISA, Fortinet, UpGuard).  
- Artigos sobre detecção e prevenção de keyloggers.  
- Diretrizes de divulgação responsável.



