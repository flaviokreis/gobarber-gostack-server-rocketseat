# GoBarber NodeJS
## Este projeto faz parte do curso GoStack 9.0 da Rocketseat

O aplicativo GoBarber tem como objetivo permitir que usuários agendem horários em barbearias (ou salão de beleza). Do outro lado o barbeiro vai poder ver a agenda de horários marcados.

Este git é a parte backend do aplicativo, desenvolvido em NodeJS utilizando o framework Express!

### Framework/plataforma
- [NodeJS](https://nodejs.org)
- [Express](https://expressjs.com)

### Formatação
- ESlint (padrão AirBnb)
- Prettier
- EditorConfig

### Banco de dados
- Sequelize: Banco de dados relacional, utilizando Postgres
- Mongoose: Bando de dados não relacional, utilizando Mongo
- Redis: Banco de dados chave/valor de alto desempenho

### Ambiente
- Nodemon: Reiniciar o serviço ao realizar qualquer alteração
- Sentry: Debug do projeto
- Dotenv: Adicionar informações sensíveis, como key de serviços
- Sucrase: Utilização do padrão atual Javascript no NodeJS
- Yarn: Alternativa ao NPM

### Outros
- jwt: Autenticação de usuário
- bcrypt: Criação de hash do password para salvar no banco de dados
- bee-queue: Execução da fila de envio de emails (utilizando o banco de dados Redis)
- date-fns: Formatação/helper de datas
- handlebars: Utilizado para formatar HTML para envio de email
- multer: Upload de arquivos
- youch
- yup: Validação de campos

## Como utilizar esse projeto
- Crie o banco de dados postgres  
`docker run --name database -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres:11`
- Crie o banco de dados Mongo  
`docker run --name mongobarber -p 27017:27017 -d -t mongo`
- Crie o banco de dados Mongo  
`docker run --name redisbarber -p 6379:6379 -d -t redis:alpine`
- Crie um arquivo .env utilizando o .env.example como referência e configure o banco de dados (postgres), mongo, redis, o servidor de email e o sentry.
- Rode o server: `yarn dev` para iniciar o server
- Rode o server: `yarn queue` para iniciar a fila que vai enviar os emails de cancelamento de serviço
