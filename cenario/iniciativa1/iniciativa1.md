Aqui está o descritivo completo e detalhado de toda a apresentação:

---

## **DESCRITIVO COMPLETO — Projeto "Internet no Avião – Reset de Senha"**

---

### **SLIDE 1 — CONCEITO GERAL**

**Título do Projeto:** Internet no Avião – Reset de Senha

**Data:** 22/07/2025

**Breve Descrição:**
Atualmente, os clientes TIM que utilizam o serviço de internet a bordo (Inflight) não conseguem resetar a senha diretamente pela página da companhia aérea. Quando tentam recuperar a senha, é exibida uma mensagem orientando-os a realizar o procedimento pelo aplicativo Meu TIM — o que gera uma quebra de jornada, já que o acesso ao app durante o voo é inviável ou extremamente limitado, causando diversas complicações para o usuário.

O objetivo deste Briefing é alterar a mensagem atual e direcionar o cliente diretamente para a página de reset de senha via Webview, sem a necessidade de acessar o App Meu TIM.

**Dados Gerais:**

| Campo | Valor |
|-------|-------|
| **Área Solicitante** | Consumer SMB Marketing Strategic Project |
| **Líder do Produto** | Felipe Povoa |
| **Categoria do Projeto** | Serviço |
| **Segmento** | Consumer / SMB |
| **Versão** | 1.0 |
| **Data** | 22/07/2025 |
| **Detalhamento** | (em branco — a ser preenchido) |
| **ID** | (em branco — a ser preenchido) |

---

### **SLIDE 2 — OVERVIEW DO PROJETO**

**Seção: Escopo**

**Resumo do Escopo do Projeto:**
Solicita-se que seja alterada a atual forma de reset de senha para o produto Inflight.

- **Cenário atual:** A parte de "Esqueci minha senha" na página da companhia aérea está apenas orientativa — ou seja, informa ao cliente que ele deve acessar o Meu TIM, mas não oferece nenhum botão ou link funcional para realizar a ação.
- **Cenário desejado:** Que seja inserido um botão funcional que leve o cliente diretamente para a página de reset de senha da TIM, aberta dentro de uma Webview integrada ao portal de bordo.

**Projetos de Referência:** (em branco — não informado)

**Metas de Contribuição:** (em branco — não informado)

**Seção: Premissas**

1. A página de reset de senha deve ser integrada ao sistema da Intelsat (provedor do serviço de conectividade a bordo), permitindo que o cliente trafegue e resete a senha diretamente pela Webview, sem ser redirecionado para fora do ambiente de bordo.
2. A URL de referência utilizada atualmente pelo App Beta para o reset de senha é:
   `https://auth3.tim.com.br/webapp-resetSenha/forgotPassword?layout=meutimapp&loginType=USER&channel=4&msisdn=DD%"MSISDN"`
   - Os parâmetros **DD** e **MSISDN** (destacados em amarelo no slide) representam respectivamente o código DDD e o número do celular do cliente.
   - Ressalva: a TI precisa avaliar e informar qual será o melhor caminho/URL definitiva para produção.

---

### **SLIDE 3 — DESCRIÇÃO DO PRODUTO**

**Seção: Elegibilidade, Abrangência & Benefícios**

| Campo | Detalhe |
|-------|---------|
| **Abrangência** | Nacional — o projeto se aplica a todo o território brasileiro |
| **Elegibilidade** | Este projeto não altera a base elegível — todos os clientes que já são elegíveis ao serviço Inflight continuam sendo, sem mudanças |
| **Benefícios** | (em branco — a ser preenchido) |
| **Vigência** | (em branco — a ser definido) |

**Seção: Integrações**
- A ser definido com TI — a integração técnica entre a Webview de reset e o sistema Intelsat ainda precisa ser mapeada e validada pela equipe de Tecnologia.

**Seção: Código Anatel**
- **SIM** ☐ / **NÃO** ☒ — O projeto não requer código Anatel.

**Seção: Informações sobre Fidelização**
- Não há — o projeto não envolve nenhum tipo de fidelização contratual.

**Seção: Canais (Contratação/Ativação/Consulta/Cancelamento/Desativação)**
- É apresentada uma tabela completa de canais TIM com checkboxes para marcar quais canais serão impactados nas operações de Contratação (C), Ativação (A), Consulta (S), Cancelamento (E) e Desativação (D). Os canais listados incluem:
  - URA *144, URA *222, URA Cadastro
  - App TIM Vendas, Captive Portal
  - Meu TIM Site, Meu TIM App
  - Portal Express, Siebel, Siebel Móvel
  - RTD, SMS, USSD, RTD NBA
  - USSD, Outros
- **Nenhum canal está marcado** — os campos estão todos em branco, aguardando definição.

---

### **SLIDE 4 — JORNADA DO CLIENTE (Detalhamento Completo)**

Este slide é o mais rico visualmente e apresenta a jornada completa do cliente em três cenários, com capturas de tela reais das interfaces.

**Texto introdutório (caixa superior):**
- "Hoje a jornada é apenas orientativa, e iremos adicionar o botão que irá direcionar para a Webview de reset de senha."
- "A página de reset de senha seja integrada ao sistema da Intelsat, e que seja possível trafegar e resetar a senha através da Webview."
- É reapresentada a URL de referência do App Beta, com os parâmetros DD e MSISDN destacados em amarelo.

---

#### **CENÁRIO ATUAL (lado esquerdo)**

São exibidas duas capturas de tela lado a lado:

1. **Tela de boas-vindas do Inflight (mais à esquerda):** Mostra a interface do portal de bordo da TIM com o branding "TIM NO AVIÃO" em fundo azul escuro com imagem de um passageiro usando o celular no avião. O texto diz: "Você conectado até nas alturas". Abaixo, há campos de login com "Número TIM" e "Senha do app Meu TIM", e logo abaixo a seção "Esqueceu sua senha?" — esta área está circulada em **vermelho** para destacar o problema. Os campos e a área de recuperação de senha são marcados como o ponto de dor do cliente.

2. **Tela de login ampliada (centro-esquerda):** Mostra em detalhe a mesma tela de login com:
   - Campo "Número TIM" com placeholder "Número TIM com DDD"
   - Campo "Senha" com placeholder "Senha do app Meu TIM" e ícone de visualizar senha
   - **Seção "Esqueceu sua senha?"** com o texto: *"Se ainda estiver em solo, desligue seu Wi-Fi, conecte-se a sua rede TIM 5G, e resgate sua senha pelo **App Meu Tim**."* — ou seja, apenas uma orientação textual, sem nenhum link clicável. O cliente é instruído a sair do ambiente de bordo e acessar o App Meu TIM, o que é impossível durante o voo.
   - Botão "Conectar" (cinza/inativo)
   - Link "Saiba mais"

---

#### **CENÁRIO SOLICITADO (centro)**

Exibe a tela de login idêntica à anterior, porém com a mudança proposta:

- Campo "Número TIM" com placeholder "Número TIM com DDD"
- Campo "Senha" com placeholder "Senha do app Meu TIM" e ícone de visualizar senha
- **Seção "Esqueceu sua senha?"** (destacada com **contorno vermelho** para indicar a alteração): O texto agora diz: *"Se ainda estiver em solo, desligue seu Wi-Fi, conecte-se a sua rede TIM 5G, e resgate sua senha **CLICANDO AQUI**."* — A diferença chave é que "CLICANDO AQUI" aparece como um **link sublinhado e clicável** (em azul), substituindo a referência ao "App Meu Tim". Este link direcionará o cliente para a Webview de reset de senha.
- Botão "Conectar"
- Link "Saiba mais"
- Uma **seta vermelha** parte desta tela e aponta para a próxima seção (Página de Reset), indicando o fluxo que o cliente seguirá ao clicar.

---

#### **PÁGINA DE RESET (lado direito)**

Exibe duas capturas de tela sequenciais do fluxo de recuperação de senha:

1. **Tela de recuperação (auth3.tim.com.br):** Mostra a Webview aberta no navegador do dispositivo com:
   - URL visível: `auth3.tim.com.br`
   - Botão azul **"RECUPERAR MINHA SENHA"**
   - Texto instrucional: *"Receba sua senha, digitando código de área (sem zero) + número do telefone. Sua senha será enviada por SMS para o seu TIM."*
   - Campo de input: "Insira seu DDD e número do telefone"
   - Checkbox **"Não sou um robô"** (reCAPTCHA)
   - Botão verde **"Enviar"**

2. **Tela de confirmação (mais à direita):** Mostra a tela de sucesso após o envio:
   - Notificação SMS do número **4141** aparece no topo da tela com a mensagem parcialmente visível: *"Olá! Sua senha é 5754 para acessar nos canais digitais da TIM. Caso queira alterar..."*
   - Ícone de **check verde** com o texto **"SENHA ENVIADA"**
   - Texto: *"Sua senha é simples e já pode ser usada..."*
   - Botão azul **"OK, JÁ TENHO O NÚMERO"**

---

#### **Fluxo resumido da jornada proposta:**

1. Cliente acessa o portal Inflight no avião → Tela de login aparece
2. Cliente clica em "Esqueceu sua senha?" → Clica no link "CLICANDO AQUI"
3. Webview abre a página `auth3.tim.com.br` → Cliente insere DDD + número
4. Cliente resolve o reCAPTCHA e clica "Enviar"
5. SMS com a nova senha é enviado para o celular do cliente
6. Tela de confirmação exibe "SENHA ENVIADA"
7. Cliente volta à tela de login e acessa o serviço com a nova senha

---

Esse é o descritivo completo e detalhado de cada slide e de cada elemento visual da apresentação. Posso reformatar isso como um documento formal, exportar em outro formato, ou detalhar algum ponto técnico específico.