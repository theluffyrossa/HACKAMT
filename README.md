# HACKAMT-PANTANAL
FormScan Health - Aplicativo de OCR para Formulários de Saúde
Mostrar Imagem
📋 Visão Geral
FormScan Health é um aplicativo móvel desenvolvido com React Native que utiliza inteligência artificial e OCR (Reconhecimento Óptico de Caracteres) para digitalizar formulários físicos da área de saúde. Integrando a API OpenAI Vision, o aplicativo transforma documentos em papel em dados digitais estruturados, otimizando fluxos de trabalho em ambientes de saúde.
✨ Funcionalidades

Digitalização Inteligente: Utilize a câmera do dispositivo para capturar imagens de formulários médicos
Reconhecimento via IA: Processamento avançado de texto utilizando a API OpenAI Vision
Extração de Dados Estruturados: Conversão automática de formulários em dados utilizáveis
Modo Offline: Trabalhe sem conexão e sincronize posteriormente
Verificação Manual: Interface para revisão e edição dos dados extraídos
Segurança de Dados: Criptografia e conformidade com regulamentações de saúde (HIPAA, LGPD)
Histórico de Processamento: Acesso a documentos previamente digitalizados

🚀 Instalação
Pré-requisitos

Node.js (v16.0.0 ou superior)
npm ou yarn
Expo CLI
Uma conta na OpenAI para acesso à API Vision

Instalação

Clone o repositório:
bashgit clone https://github.com/seu-usuario/formscan-health.git
cd formscan-health

Instale as dependências:
bashnpm install
# ou
yarn install

Crie um arquivo .env na raiz do projeto:
OPENAI_API_KEY=sua_chave_api_aqui
API_URL=https://seu-backend.com/api

Inicie o aplicativo:
bashnpx expo start


🔧 Configuração
Configuração da API
A aplicação requer um backend para processar dados e gerenciar a comunicação com a API OpenAI Vision. Configure o backend seguindo as instruções no repositório formscan-health-api.
Configuração do ambiente de desenvolvimento
Certifique-se de habilitar a nova arquitetura do React Native no seu app.json:
json{
  "expo": {
    "plugins": [
      [
        "expo-build-properties",
        {
          "android": {
            "newArchEnabled": true
          },
          "ios": {
            "newArchEnabled": true
          }
        }
      ]
    ]
  }
}
📱 Uso

Login: Acesse o aplicativo com suas credenciais
Digitalização: Toque no botão de câmera para capturar um novo formulário
Revisão: Verifique se a imagem capturada está clara e legível
Processamento: Aguarde enquanto a IA extrai os dados do formulário
Validação: Revise os dados extraídos e faça correções se necessário
Salvamento: Confirme e salve os dados processados
Sincronização: Os dados são enviados para o servidor ou armazenados localmente para sincronização posterior

🔌 Conexões e Integrações
API OpenAI Vision
O aplicativo utiliza a API OpenAI Vision para análise de imagens e extração de texto. É necessário configurar uma chave de API válida no arquivo .env.
Backend API
A comunicação com o backend é feita através de uma API RESTful. O endpoint padrão para verificação de saúde da API é:
GET /api/health
Um status 200 OK indica que a API está funcionando corretamente.
🛠️ Tecnologias Utilizadas

React Native: Framework para desenvolvimento móvel multiplataforma
Expo: Plataforma para simplificar o desenvolvimento React Native
OpenAI Vision API: Serviço de IA para processamento de imagens
React Navigation: Navegação entre telas
AsyncStorage: Armazenamento local de dados
Axios: Cliente HTTP para requisições à API
NetInfo: Monitoramento de conectividade de rede

📝 Tratamento de Erros
Problemas de Conectividade
O aplicativo inclui um sistema robusto de tratamento de erros de conectividade, permitindo:

Verificação do status da API em intervalos regulares
Indicação visual do estado de conectividade
Modo offline com sincronização posterior
Armazenamento local de formulários quando não há conexão

Erros de OCR
A aplicação inclui mecanismos para lidar com imprecisões no reconhecimento de texto:

Interface para correção manual de campos
Destaque visual de campos com baixa confiança
Validação de dados específica para informações médicas

🔒 Segurança e Privacidade

Criptografia: Dados em repouso e em trânsito são criptografados
Autenticação: Sistema de login seguro com tokens JWT
Conformidade: Implementação de medidas de segurança em conformidade com HIPAA e LGPD
Anonimização: Dados sensíveis são anonimizados antes de serem enviados para processamento na nuvem
