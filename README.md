# 🤖 Chatbot EcoMart - IA Generativa com Python e Gemini

Chatbot inteligente desenvolvido com Flask e Google Gemini AI para atendimento ao cliente de e-commerce, criado durante o curso **"Python e Gemini: crie um chatbot com IA Generativa"** da Alura.

## 📋 Sobre o Projeto

Este projeto implementa um chatbot de atendimento ao cliente para a loja fictícia "EcoMart", utilizando o modelo de linguagem Gemini 1.5 Flash do Google. O chatbot é capaz de responder perguntas relacionadas ao e-commerce de forma contextualizada e inteligente.

### ✨ Funcionalidades

- 💬 Interface de chat interativa e responsiva
- 🤖 Integração com Google Gemini AI (modelo gemini-1.5-flash)
- 🔄 Respostas em tempo real
- 🎯 Contexto específico para atendimento de e-commerce
- ⚡ Sistema de retry automático em caso de falhas
- 🎨 Interface moderna e intuitiva

## 🛠️ Tecnologias Utilizadas

- **Python 3.x** - Linguagem de programação
- **Flask 2.3.2** - Framework web
- **Google Generative AI 0.8.2** - API do Gemini
- **python-dotenv 1.0.1** - Gerenciamento de variáveis de ambiente
- **HTML5/CSS3** - Interface do usuário
- **JavaScript** - Interatividade do frontend
- **jQuery** - Requisições AJAX

## 📦 Instalação

### Pré-requisitos

- Python 3.7 ou superior
- Conta no Google AI Studio para obter a API Key do Gemini

### Passo a Passo

1. **Clone o repositório**
```bash
git clone https://github.com/adriannylelis/alura-chatbotpy.git
cd alura-chatbotpy
```

2. **Crie um ambiente virtual (recomendado)**
```bash
python -m venv venv
source venv/bin/activate  # No Windows: venv\Scripts\activate
```

3. **Instale as dependências**
```bash
pip install -r requirements.txt
```

4. **Configure as variáveis de ambiente**

Crie um arquivo `.env` na raiz do projeto:
```env
GEMINI_API_KEY=sua_chave_api_aqui
```

Para obter sua API Key:
- Acesse [Google AI Studio](https://makersuite.google.com/app/apikey)
- Crie uma nova chave de API
- Copie e cole no arquivo `.env`

5. **Execute a aplicação**
```bash
python app.py
```

6. **Acesse no navegador**
```
http://127.0.0.1:5000
```

## 🎯 Como Usar

1. Abra a aplicação no navegador
2. Digite sua pergunta ou dúvida no campo de mensagem
3. Pressione Enter ou clique no botão de enviar
4. O chatbot irá processar e responder sua pergunta
5. Continue a conversa naturalmente

### Exemplos de Perguntas

- "Quais são os produtos disponíveis?"
- "Como faço para rastrear meu pedido?"
- "Qual é a política de devolução?"
- "Vocês têm produtos sustentáveis?"

## 📁 Estrutura do Projeto

```
alura-chatbotpy/
├── app.py                  # Aplicação Flask principal
├── requirements.txt        # Dependências do projeto
├── .env                    # Variáveis de ambiente (não versionado)
├── README.md              # Documentação
├── static/                # Arquivos estáticos
│   ├── css/
│   │   ├── _reset.css    # Reset CSS
│   │   └── index.css     # Estilos da aplicação
│   ├── img/              # Imagens
│   └── js/
│       └── index.js      # Lógica do frontend
└── templates/
    └── index.html        # Template HTML principal
```

## ⚙️ Configurações

### Parâmetros do Modelo Gemini

No arquivo `app.py`, você pode ajustar os seguintes parâmetros:

```python
configuracao_modelo = {
    "temperature": 0.1,        # Criatividade (0.0 a 1.0)
    "max_output_tokens": 8192  # Tamanho máximo da resposta
}
```

- **temperature**: Controla a aleatoriedade das respostas (0.1 = mais focado e determinístico)
- **max_output_tokens**: Limite de tokens na resposta

### Prompt do Sistema

O comportamento do chatbot é definido pelo prompt do sistema em `app.py`:

```python
prompt_do_sistema = f"""
Você é um chatbot de atendimento a clientes de um e-commerce. 
Você não deve responder perguntas que não sejam dados do ecommerce informado!
"""
```

## 🔒 Segurança

- ⚠️ **Nunca compartilhe sua API Key**
- ✅ Use sempre o arquivo `.env` para variáveis sensíveis
- ✅ Adicione `.env` ao `.gitignore`
- ✅ Em produção, desative o modo debug do Flask

## 🚀 Melhorias Futuras

- [ ] Adicionar histórico de conversas
- [ ] Implementar autenticação de usuários
- [ ] Criar base de conhecimento específica da loja
- [ ] Adicionar suporte a imagens
- [ ] Implementar análise de sentimento
- [ ] Deploy em produção (Heroku, Railway, etc.)

## 📚 Aprendizados

Este projeto foi desenvolvido durante o curso da Alura e aborda:

- Integração com APIs de IA Generativa
- Desenvolvimento web com Flask
- Manipulação de requisições assíncronas
- Boas práticas de segurança com variáveis de ambiente
- Tratamento de erros e retry de requisições

## 🎓 Curso

Este projeto foi desenvolvido durante o curso:
**[Python e Gemini: crie um chatbot com IA Generativa](https://cursos.alura.com.br/course/python-gemini-crie-chatbot-ia-generativa)** - Alura

## 📄 Licença

Este projeto é de código aberto e está disponível para fins educacionais.
