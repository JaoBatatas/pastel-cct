# 🥐 Pastelômetro MP

Uma aplicação web serverless e preditiva para modelar estatisticamente o horário de saída e o tempo de vida do pastel na cantina do Centro de Ciências Tecnológicas (CCT). Chega de dar viagem perdida e encontrar a estufa vazia!

## 📊 Como Funciona?

O projeto utiliza a **Distribuição Normal (Curva de Gauss)** para prever duas janelas críticas do dia:
1. **Horário de Saída (Ficar Pronto):** Modela a probabilidade do pastel já estar disponível com base no histórico de registros.
2. **Horário de Término (Acabar):** Modela o tempo de vida do pastel na estufa, ajudando a prever quando os salgados vão esgotar.

O sistema calcula automaticamente em tempo real no frontend:
* **Média (μ)**
* **Mediana**
* **Moda**
* **Desvio Padrão Populacional (σ)**

---

## 🏗️ Arquitetura do Projeto

O sistema foi desenhado para ser 100% gratuito, sem necessidade de servidores ativos (24/7) ou chaves expostas:

* **Frontend:** Página única estática (SPA) hospedada no **GitHub Pages** (`index.html`), utilizando **Chart.js**.
* **Backend:** Uma API Serverless construída com **Google Apps Script**.
* **Banco de Dados:** **Google Sheets**.

---

## ⚙️ Configuração Passo a Passo

### 1. Preparando o Banco de Dados (Google Sheets)
Crie uma planilha com uma aba chamada `Dados` e as colunas: Data, Hora, Minutos_do_Dia, Hora_Acabou.

### 2. Configurando o Backend (Google Apps Script)
1. Vá em **Extensões > Apps Script** na sua planilha.
2. Cole o código do backend, clique em **Implantar > Nova implantação**.
3. Configure como **App da Web** (acesso: 'Qualquer pessoa'). Copie o URL gerado.

### 3. Conectando o Frontend
1. No `index.html`, substitua `API_URL` pela sua URL do Apps Script.
2. Ative o **GitHub Pages** nas configurações do seu repositório.

---

Desenvolvido para otimizar o tempo de intervalo no MP! 🚀
