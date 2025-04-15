
# Previsão de Placar Jogos Premier League

#Um projeto no Google Colab(ele começou no vs code depois migrei) onde eu faço o web scrapping dos dados, limpo e os manejo para criar um simples modelo de previsão de placares utilizando um dashboard dinâmico. Ele está dividido em três notebooks: App,Tabela,Dados dos Times. Faço um webscrapping do transfermarketing dos times da PL, depois faço das tabelas de classificação do campeonato inglês desde a temporada 2002 -2003.

# Com esses dados eu contruo um dashboard utilizando o streamlit e o ngrok eu crio um dashboard dinâmico onde é possível ver todos os dados que eu coletei, além disso utilizo de um ferramental estatístico simples para prever um possível confronto entre equipes.


## Instalação
# Premier League Dashboard - Instalação

Siga os passos abaixo para configurar e executar o projeto localmente.

## 📋 Pré-requisitos
- Python 3.8+
- Conta no [Ngrok](https://ngrok.com/) (para acesso público)
- Token de autenticação do Ngrok

## 🛠 Instalação

1. **Clonar o repositório**
```bash
git clone https://github.com/seu-usuario/premier-league-dashboard.git
cd premier-league-dashboard

pip install -r requirements.txt

Configurar Ngrok

Crie um arquivo config.toml na raiz do projeto:

toml
Copy
[server]
port = 8501
enableCORS = false

Obtenha seu token de autenticação no dashboard do Ngrok

Configure o token:

bash
Copy
ngrok config add-authtoken <SEU_TOKEN_AQUI>
🚀 Execução
bash
Copy
# Iniciar o Streamlit em background
streamlit run app.py --server.port 8501 --server.fileWatcherType none --browser.serverAddress 0.0.0.0 --server.enableCORS false --server.enableXsrfProtection false &>/dev/null&

# Obter URL público
from pyngrok import ngrok
public_url = ngrok.connect(addr='8501', proto='http')
print(f"URL de acesso: {public_url.public_url}"
    
## Referência

#Livros
-- [Python Data Science Handbook, 2nd Edition - Jake VanderPlas]

#Projeto Inspiração
# --[https://github.com/BrunoMeloSlv/appbrasileirao2025/blob/main/main.py]