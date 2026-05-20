# 🚀 Century Financial - Trader Pro Dashboard

![Status do Projeto](https://img.shields.io/badge/Status-Operacional-success?style=for-the-badge)
![Tecnologias](https://img.shields.io/badge/Tech-HTML5%20%7C%20CSS3%20%7C%20JS-blue?style=for-the-badge)

O **Century Financial - Trader Pro Dashboard** é um terminal web avançado e de alta performance desenvolvido para mapeamento de mercado, automação de estratégias e execução simulada de ordens com foco no ativo **XAUUSD (Ouro Spot)**. 

O projeto foi estruturado para ser 100% autônomo (*client-side*), leve e responsivo, ideal tanto para uso em desktops quanto para compilação e instalação direta em dispositivos Android (APK).

---

## 💎 Funcionalidades Principais e Últimas Atualizações

* **📊 Gráfico Fixo Global:** O gráfico principal (`chartPrincipal`) foi integrado diretamente ao cabeçalho superior (`app-header`). Ele permanece visível de forma fixa no topo do aplicativo, permitindo o monitoramento do preço em tempo real independente da aba selecionada (*Home, Market, Trades* ou *Risco*).
* **🟢/🔴 Alerta HUD de Operação Dinâmica:** Sistema global de alertas instalado logo abaixo do gráfico. No milissegundo em que um rompimento é confirmado, a barra acende com um efeito neon suave: **Verde para COMPRA** ou **Vermelho para VENDA**, exibindo o preço de entrada e alvos instantaneamente.
* **🎯 Projeção de Linhas Estratégicas:** Linhas horizontais pontilhadas são desenhadas de forma dinâmica diretamente no gráfico superior para indicar visualmente onde estão o **Take Profit (Alvo)** e o **Stop Loss (Prevenção de Perdas)**.
* **🛠️ Painel de Engenharia Unificado:** O botão de ignição *"Inicializar Motor Operacional"* foi centralizado na aba **Risco**, posicionado estrategicamente junto com as configurações de horários (Início/Fim da Captura) e tempo gráfico de confirmação (M1, M5, M15).
* **🔒 Segurança e Persistência:** Sistema de autenticação simulada com suporte a registro local e login biométrico, salvando todas as preferências, histórico de trades e saldo da banca de forma segura no `LocalStorage` do dispositivo.

---

## 🛠️ Arquitetura Técnica & Dependências

O terminal foi construído utilizando tecnologias nativas para garantir a máxima velocidade de renderização:

* **Chart.js:** Renderização de gráficos de alta performance via Canvas HTML5.
* **NoSleep.js:** Biblioteca integrada para impedir que a tela do celular apague ou bloqueie enquanto o motor estiver realizando a varredura do canal.
* **WebSockets (Binance Stream):** Conexão contínua em tempo real para obter a cotação do Ouro Spot (`paxgusdt`).
* **Telegram Bot API:** Integração nativa via requisições assíncronas (`fetch`) para disparo de notificações instantâneas de ordens direto no smartphone do operador.

---

## 🚀 Como Executar o Projeto

Como o projeto é composto por um único arquivo estático, existem duas maneiras simples de utilizá-lo:

### 1. Execução Local
1. Faça o download ou clone este repositório.
2. Dê um duplo clique no arquivo `index.html`.
3. O painel abrirá instantaneamente em seu navegador.

### 2. Pelo GitHub Pages (Online 24/7)
Este repositório está configurado para rodar diretamente pelo GitHub Pages. Você pode acessar a versão estável e online através do link gerado nas configurações do seu repositório:
`https://<seu-usuario>.github.io/<nome-do-repositorio>/`

---

## 📱 Compilando para APK (Android)

Para transformar este painel em um aplicativo nativo para Android e acompanhar o robô direto do seu celular sem que a tela bloqueie:

1. Use ferramentas de empacotamento baseadas em WebView, como o **Website 2 APK Builder** ou framework **CapacitorJS**.
2. Forneça o link do seu GitHub Pages ou a pasta local contendo o arquivo `index.html`.
3. Defina o nome do aplicativo como `Century Pro Master` e adicione um ícone de sua preferência.
4. Gire o APK e instale diretamente no seu dispositivo Android.

---

## 📝 Configuração do Telegram

Para receber os alertas de início de operação no seu celular, lembre-se de ajustar as constantes no topo do arquivo JavaScript com as suas próprias credenciais:
```javascript
const TELEGRAM_TOKEN = "SEU_TOKEN_AQUI";
const CHAT_ID = "SEU_CHAT_ID_AQUI";
