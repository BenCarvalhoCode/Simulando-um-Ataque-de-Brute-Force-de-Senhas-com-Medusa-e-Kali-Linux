# Simulando-um-Ataque-de-Brute-Force-de-Senhas-com-Medusa-e-Kali-Linux
## Primeiro passo: Configurar ambientes e encontrar qual porta está aberta
- Iniciei o mapeamento utilizando o NMAP para realizar a enumeração na máquina alvo. Em segundos, retornou um serviço FTP ativo, funcional e com uma porta aberta. Já tenho meu canal de acesso à máquina vulnerável;
  
## Segundo passo: Criação de wordlists
- Neste momento, precisei definir quais seriam os usuários e senhas utilizados para o Brute Force ser executado. Adicionei usuários e senhas de maneira reduzida e selecionada, a fim de obter um espaço amostral reduzido para facilitar o acompanhamento e estudo;
- Neste ambiente de testes mais enxuto, é possível analisar o comportamento da ferramenta caso a caso, favorecendo a prática e somando conhecimento ao desafio;
- Outro ponto interessante é a possibilidade de checar com clareza falsos positivos e os padrões;

## Terceiro passo: Brute Force com Medusa contra o FTP
- Tendo os dados necessários após mapear e enumerar, chegou o momento do ataque ao FTP;
- Enviei o comando utilizando o Medusa, com os devidos parâmetros, a fim de obter os dados do servidor e descobrir qual par teria sucesso;

## Quarto passo: DVWA -> autenticação web, atacando fomrulários
- A primeira ação tomada foi entender como ocorre a comunicação entre o client/servidor e quais mensagens são disparadas. Para isto, utilizei o par 'teste', 'teste';
- Com as mensagens de erro em mãos, pude buscar padrões e identificar onde está o ponto frágil na autenticação;
- Agora, só faltava definir os parâmetros para o Medusa reproduzir a requisição de login;
- 
### Qualquer descuido é uma brecha para ataque. A cada nova camada de segurança, existirá uma nova vulnerabilidade, porém precisamos sempre mitigar os riscos cumprindo os protocolos já existentes;
  Um sistema robusto depende de usuários que cumpram os parâmetros, sendo assim, a cybersegurança é uma malha de contribuição. 

## Sexto passo: Password spraying em SMB com enumeração de usuários.
- Utilizando a enumeração SMB para identificar usuários expostos e configurações de permissão vulneráveis;
- Após enumerar os usuários, criei duas wordlists (users, password) para basear o ataque;
- Tendo os dados em mãos, utilizei o Medusa com os parâmetros para ataque via SMB com duas threads simultâneas;
- Obtive com sucesso a lista de dados de acesso com par validado. Sendo assim, testei o login através do SmbClient;

# Após todos os passos, os aprendizados principais que levo são os seguintes:
## Formas de Defesa
- Segmentação da Rede;
- Senhas fortes e com data de expiração;
- Bloqueio de IPs após múltiplas tentativas de Login;
- Monitoramento inteligente do sistema através de IA;
- Autenticação Multifator;

## Pontos importantes
- Toda brecha precisa de atenção;
- Sempre analisar se dados estão expostos de forma indevida;
- Invesitir em treinamento de segurança e buscar formas de dificultar acesso não autorizado;



