# Custom Auth (Autenticação customizada) — PT
App reutilizável para fazer autenticação de usuário customizada, utilizando apenas de e-mail e senha para entrar (fazer log-in).

## Sobre
O App desenvolvido se trata de um outro método de autenticação, diferente do padrão do django (que usa nome de usuário e senha). Nesse método de autenticação o usuário deverá inserir seu e-mail e senha, sem obrigatoriedade de inserir quaisquer outros valores.

## Como usar
Para usar o App, basta seguir os passos abaixo:

### Início
- baixar o código deste repositório;
- copiar a pasta do app: ``custom_auth``;
- colar a pasta do item acima dentro da mesma pasta do seu arquivo manage.py;

### Implementação
- alterar o arquivo ``settings.py`` do projeto que quer utilizar a autenticação, adicionando o seguinte:

  ``` python
  AUTH_USER_MODEL = 'customauth.MyUser' # não alterar
  LOGIN_REDIRECT_URL = '/sua_url' # Coloque a url deseja pós login (autenticar no sistema)
  LOGIN_REDIRECT_URL = '/sua_url' # Coloque a url deseja pós logout (encerrar sessão no sistema)
  ```
- no mesmo arquivo, adicione o app aos ``INSTALLED_APPS``
  
Pronto! Agora seu sistema de login deve estar corretamente configurado.

> O App atualmente só conta com registro, login e logout
  
# Custom Auth (Custom Authentication) — EN
Reusable App to make custom user authentication in websites, using only e-mail address and password for log-in yourself.

## About
The developed App is about other authentication way, unlike django's default (which uses username and password). In this authentication way the user must insert your email and password, he doesn't need enter other values.
