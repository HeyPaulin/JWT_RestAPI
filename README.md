# JWT_RestAPI

Documentação para JWT_RestAPI

Visão Geral
Esse é um aplicativo REST API simples, construído usando Spring Boot, Spring Security e JWT para autenticação e autorização. O aplicativo inclui funções de usuário e endpoints seguros que são acessíveis com base nas funções do usuário.

Estrutura do Projeto

O projeto consiste em seis pacotes principais:

1. application
2. config
3. controller
4. model
5. security
6. service
![Estrutura](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/4e60f045-aba6-417c-b31e-8004ad526c96)


1. application
JwtRestApiApplication
![application](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/f0b68d4c-cc66-4a4e-b603-50486fdfff34)
. Ponto de entrada para o aplicativo Spring Boot.
. Escaneia os componentes Spring no pacote com.example.

2. config
SecurityConfig
![config1](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/48e9626b-9bca-4dc3-9b8d-946173daa36e)
![config2](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/608d8cca-3ee8-46d0-b606-20bd4f65b7b9)
. Configura a segurança do aplicativo.
. Desabilita a proteção CSRF.
. Configura a segurança HTTP para permitir o acesso a determinados endpoints com base em funções.
. Define três usuários em memória: admin, moderador e comum, com suas respectivas funções.

3. controller
AuthController
![controller1](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/d79d6393-9118-4e4c-b24a-9d7e191a39a0)
![controller2](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/7d2da67b-9ebc-47fb-879f-9fed2aedaa3b)
. Define endpoints REST para login e acesso baseado em funções.
. Usa AuthService para gerar e extrair tokens JWT.
. Fornece endpoints para obter os detalhes do usuário autenticado com base nas funções.

4. model
LoginRequest
![model](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/6dd37149-ada0-4cb8-bde5-d2313c2ccf37)
. Uma classe de modelo simples para solicitações de login.
. Contém campos de nome de usuário e senha com os respectivos getters e setters.

5. security
JwtUtil
![security1](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/bf09b0b1-fd52-4510-bee5-389f15de4409)
. Classe utilitária para gerar e extrair tokens JWT.
. Define a geração de chave secreta e configurações de expiração do token.
. Usa a biblioteca JJWT para operações JWT.

6. service
AuthService
![service](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/401ac513-79d2-45a6-a8cc-fb3d1879e0d7)
. Fornece serviços para gerar e extrair tokens JWT.
. Usa JwtUtil para operações de token.




POST Login
![Post Login](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/740cba6d-56c7-4214-a163-bfe31a9f37fa)

Extract Username
![Extract Username](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/30eb562e-7c51-4f64-8f60-6c187993f02d)

Get User
![Get User](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/942a99aa-eb1e-4dd3-97a3-3744466cd061)

Get Admin
![Get Admin](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/b4508009-053a-4ded-8f14-70e87048bcfa)

Get Moderador 
![Get Moderador](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/520eddc4-59cb-4536-a047-ccc83f12d74f)

Get Comum
![Get Comum](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/07bb5575-df25-4e4c-9b04-7aca4b1778c1)

DIAGRAMA
![WhatsApp Image 2024-06-15 at 20 29 27](https://github.com/HeyPaulin/JWT_RestAPI/assets/101124585/f6997cc7-c155-4c1a-bb7f-3e12ac7852c2)


