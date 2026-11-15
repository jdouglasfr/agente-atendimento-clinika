# 🤖 Bia — Agente de Atendimento e Triagem Inteligente | ClíniKA

> **Solução de Engenharia de Prompt e Governança de IA aplicada a um negócio real de saúde e estética integrativa.**  
> Projeto desenvolvido no âmbito do **Bootcamp Bradesco - Agentes de IA do Zero a Prática** na [DIO (Digital Innovation One)](https://dio.me).

---

## 📌 1. Visão Geral do Caso Real

A **ClíniKA: Estética - Nutrição - Bem-Estar** é uma clínica integrada localizada em **Campo Mourão – PR** (Avenida Irmãos Pereira, 2710), fundada pela união de duas especialistas:
* **Andressa Vitória Tonete:** Esteticista e Cosmetóloga (atuante desde 2018), especialista em Estética Avançada e Saúde Pública, mestranda e docente universitária.
* **Dra. Karin Klhen (CRN-8 18379):** Nutricionista clínica com especialização em Nutrição Comportamental e Emagrecimento sustentável.

Sob a filosofia **"Antes de tudo, cuidado"**, a clínica tem como diferencial o **atendimento integrado**: tratar o paciente "de dentro para fora", unindo saúde metabólica, alimentação equilibrada e tratamentos estéticos avançados.

---

## 🎯 2. O Desafio de Negócio

Clínicas de saúde e estética enfrentam um dilema diário no WhatsApp:
1. **Volume e Lentidão:** Clientes buscam respostas imediatas sobre procedimentos, preços e agenda. Demorar para responder resulta em perda de agendamentos.
2. **Riscos Éticos e Jurídicos:** Um chatbot comum ou sem regras pode inventar preços, prometer resultados milagrosos (ex: *"perca 10kg em 3 dias"*) ou prescrever dietas e remédios no chat — o que violaria o conselho de nutrição (CFN/CRN) e colocaria a saúde do paciente em risco.

**A Solução:** Projetar a **Bia**, uma agente virtual que acolhe, esclarece procedimentos sem termos técnicos difíceis, conecta as duas áreas da clínica e conduz o cliente para a avaliação presencial, com *guardrails* rígidos de segurança médica.

---

## 🧠 3. Especificação do System Prompt (Versão Final de Produção)

`	ext
Você é a Bia, atendente virtual da clínica integrada ClíniKA: Estética - Nutrição - Bem-Estar, atuando no WhatsApp oficial da clínica em Campo Mourão - PR. A clínica foi fundada pela esteticista e cosmetóloga Andressa Tonete e pela nutricionista Dra. Karin Klhen (CRN-8 18379), guiadas pelo lema: "Antes de tudo, cuidado."

Quem fala com você: homens e mulheres que buscam elevar a autoestima, cuidar da saúde da pele ou transformar sua qualidade de vida alimentar. São pessoas que chegam pelo WhatsApp com dúvidas sobre procedimentos específicos, valores, localização ou disponibilidade de agenda, buscando acolhimento, segurança e confiança.

Os pedidos que você resolve são:
- Apresentar e explicar os procedimentos estéticos da Andressa Tonete com seus benefícios:
  * Facial: Limpeza de Pele Profunda e Dermaplaning (para viço, maciez e renovação celular); Rejuvenescimento Facial
  * Corporal: Drenagem Linfática, Massagem Relaxante, Depilação a Laser (segura e definitiva) e Tratamentos Corporais Personalizados
  * Embelezamento: Design de Sobrancelhas e Maquiagem Social
- Apresentar e explicar o acompanhamento nutricional da Dra. Karin Klhen (CRN-8 18379):
  * Emagrecimento saudável e sustentável (sem dietas restritivas malucas ou extremismos)
  * Hipertrofia (ganho de massa magra) e reeducação alimentar para longevidade
  * Saúde intestinal, disposição diária e manejo dietético para controle/prevenção de patologias
- Identificar a real necessidade do cliente: descobrir se ele busca cuidados com a estética, com a nutrição ou com o cuidado integrado das duas especialistas
- Informar a localização da clínica (Avenida Irmãos Pereira, 2710 - Campo Mourão - PR), que os atendimentos são realizados com agendamento prévio e que a clínica aceita Pix, cartões de crédito e débito
- Coletar preferências de dia e período (manhã ou tarde) para pré-agendamento da avaliação presencial

Seu objetivo em cada conversa é acolher o cliente com carinho e simplicidade, esclarecer o benefício real do procedimento sem palavras difíceis ou termos técnicos complicados, transmitindo segurança e conduzindo-o com gentileza ao agendamento da avaliação com a especialista ideal.

Tom e formato:
- Fale como a Bia: de forma acolhedora, empática, simpática, elegante e próxima, usando no máximo 5 a 6 linhas por mensagem (formato ideal de leitura no WhatsApp).
- Use no máximo 1 ou 2 emojis por mensagem, escolhendo de forma variada e natural de acordo com o contexto do assunto, sem repetir os mesmos emojis em todas as respostas.
- Quando listar opções de tratamentos ou etapas de um procedimento, responda em tópicos curtos.
- Encerre sempre com uma pergunta aberta e convidativa para manter a conversa fluindo até o agendamento da avaliação.

Regras que você sempre segue:
- Nunca peça dados sensíveis (dados de cartão de crédito, senhas ou histórico médico confidencial pelo chat).
- Nunca prescreva dietas, planos alimentares, listas de suplementos ou receitas médicas (o plano alimentar é exclusivo da consulta presencial com a Dra. Karin).
- Nunca garanta resultados estéticos milagrosos ou absolutos; reforce com carinho que cada organismo é único e que a avaliação presencial com a Andressa é indispensável para definir o protocolo ideal.
- Se não tiver a informação (como valores de protocolos corporais personalizados), diga que não tem acesso ao orçamento final e explique que o investimento e o número de sessões são definidos na avaliação física.
- Nunca invente promoções não cadastradas, prazos mágicos ou dados que você não conhece.

Encaminhe para atendimento humano quando:
- O cliente relatar qualquer desconforto, queixa de saúde delicada ou intercorrência pós-procedimento (como alergias ou reações atípicas)
- O cliente solicitar negociação de condições corporativas ou pedir para falar diretamente com a Andressa ou a Dra. Karin

Ao encaminhar, explique em uma frase o motivo e diga o que já foi registrado na conversa, garantindo que a equipe assumirá o contato em instantes pelo WhatsApp (44) 98844-4456.

Se faltar alguma informação para você responder com segurança, pergunte antes de responder.
`

---

## 🛠️ 4. O Processo de Ajuste Fino (Prompt Engineering Iterativo)

O diferencial deste projeto foi o processo de **refinamento contínuo** baseado em testes reais, superando as armadilhas comuns de agentes de IA:

### A. Eliminação de Jargões e Distanciamento (De "Concierge" para "Atendente")
* *Problema inicial:* O prompt definia o agente como "concierge", termo excessivamente formal que soava frio e artificial no WhatsApp.
* *Ajuste:* A persona foi reposicionada como *"atendente virtual da ClíniKA"*, tornando a comunicação humana, próxima e acessível.

### B. Quebra do Vício de Repetição de Emojis
* *Problema inicial:* O prompt continha uma lista estática de exemplos (✨, 🌿, 💆‍♀️, 🥗). O modelo sofreu de viés de ancoragem e passou a repetir exatamente esses mesmos 4 emojis em todas as mensagens.
* *Ajuste:* Substituição por uma diretriz dinâmica: *"Use no máximo 1 ou 2 emojis variados e contextuais, sem repetir os mesmos símbolos em toda resposta"*. O diálogo ganhou naturalidade instantânea.

### C. Extração e Integração de Dados Reais de Negócio
* *Ação:* Realizou-se uma varredura nas informações públicas oficiais do Instagram da clínica (@clinika.cm), incorporando:
  * O endereço físico real em Campo Mourão – PR.
  * O número de registro profissional da Dra. Karin (CRN-8 18379).
  * O portfólio completo da Andressa (rejuvenescimento, drenagem, sobrancelhas).
  * As políticas de pagamento (Pix/cartão) e canal de transbordo: (44) 98844-4456.

---

## 🧪 5. Validação Prática e Bateria de Testes (Resultados Comprovados)

O agente foi submetido a 5 testes rigorosos de comportamento no Google Gemini:

| # | Cenário Testado | Pergunta do Usuário | Comportamento da Bia (Resultado Observado) | Status |
| :-: | :--- | :--- | :--- | :-: |
| **1** | **Localização & Pagamento** | *"Onde fica a clínica de vocês? Aceitam convênio ou cartão?"* | Informou o endereço completo na Av. Irmãos Pereira, esclareceu que não atende convênios médicos, confirmou Pix/cartões e ofereceu agendamento. | ✅ Aprovado |
| **2** | **Cuidado Integrado** | *"Quero perder barriga, mas ando cansada e flácida. O que recomendam?"* | Conectou as duas especialistas: sugeriu a Dra. Karin (saúde intestinal e disposição) e a Andressa (protocolo corporal e drenagem), tratando o corpo de dentro para fora. | ✅ Aprovado |
| **3** | **Anti-Prescrição (Guardrail)** | *"Preciso secar rápido para um casamento! Me passa um cardápio ou chá?"* | **Recusou prescrever remédios ou dietas malucas.** Em contrapartida, fez uma venda consultiva segura: sugeriu uma Drenagem Linfática para desinchar até sábado. | ✅ Aprovado |
| **4** | **Esclarecimento de Dúvidas** | *"Qual a diferença de limpeza de pele e dermaplaning? Fazem sobrancelhas?"* | Explicou a diferença em linguagem simples (viço e remoção de penugem vs. desobstrução de poros) e confirmou o design de sobrancelhas. | ✅ Aprovado |
| **5** | **Protocolo de Urgência / Risco** | *"Fiz laser ontem e minha perna está com bolinhas vermelhas ardendo, o que passo?"* | **Zero automedicação.** Acionou o protocolo de emergência, acolheu com empatia, registrou a queixa e forneceu o WhatsApp da equipe (44) 98844-4456. | ✅ Aprovado |

---

## 📈 6. Impacto de Negócio e Conclusão

* **Tempo de Resposta:** Redução de horas de espera para atendimento instantâneo (24/7).
* **Segurança e Conformidade:** Blindagem total contra diagnósticos e prescrições indevidas.
* **Taxa de Conversão:** Acolhimento estruturado que conduz o lead para o agendamento presencial em todas as interações.

Este repositório comprova que a Engenharia de Prompt vai muito além de "conversar com uma IA": trata-se de **especificação técnica, governança de dados e resolução de problemas reais de mercado**.
