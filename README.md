Nome: Márcio Caprioli Dias
RGM: 26590905
Turma: 8º Semestre de Engenharia de Software
Universidade Cruzeiro do Sul

# Projeto Integrador Transdisciplinar (PIT) II

O projeto tem como objetivo desenvolver um sistema de vendas de Cupcakes pela internet (e-commerce). A plataforma permite que seja acessado através das plataformas Desktop e Mobile, e o cliente realize as compras dos produtos de onde estiver. Além disso, o sistema oferece funcionalidades de comunicação via Whatsapp com um colaborador da loja para tirar dúvidas e auxiliar o cliente nas suas compras.

## Menu

- **História de usuários**: [histórias](./Documentação do projeto/PIC_atividade_engenharia_software_I.pdf)
- **Diagrama de banco de dados**: [imagem](./documentacoes/diagrama_de_banco_de_dados.PNG)
- **Diagrama de implantação**: [imagem](./documentacoes/diagrama_de_implantacao.png)
- **Diagrama de caso de uso**: [imagem](./documentacoes/caso_de_uso.PNG)
- **whireframe**: [link](https://whimsical.com/LEfbfkMyv4sePLp43sAfW6)

## Pré-requisitos

- **WIX**: [Log in](https://pt.wix.com)
- **GITHUB**: [Acessar e repositório](https://github.com)
- **MySQL**: [Instalar MySQL](https://dev.mysql.com/downloads/installer/)

---

## Configuração do Projeto

### 1. **Clone o repositório**

```bash
   git clone https://github.com/marciocaprioli/ProjetoIntegrador.git
```

### 2. **Crie o projeto no site do WIX**

#### **Passos para criar o projeto:**

2.1. **Abra o site do WIX**.
   - Realize o login;
   - Crie o projeto;
   - Iniciar chat com o apoio da IA para obter um painel de controle personalizado;

![1 Criar projeto Captura de tela_9-11-2024_91051_manage wix com](https://github.com/user-attachments/assets/0f637dab-07aa-4b70-b259-6ab41e28bc1d)


   - Descreva com detalhes as histótias de usuários para a criação dos painéis de cada tela da aplicação;
   - Será direcionado para as configurações de domínio, caso queira vincular um já existente, ou criar um novo;
   - Configure os pedidos online;
   - Configure os métodos de pagamentos;

![2 Captura de tela_9-11-2024_9294_manage wix com](https://github.com/user-attachments/assets/458671e6-9c05-4b69-9f6e-bb0c8be75361)


   - Após as configurações, edite o catálogo incluíndo as fotos e dados dos produtos que serão divulgados na aplicação;

![3 Captura de tela_9-11-2024_93240_manage wix com](https://github.com/user-attachments/assets/d9bd172b-2d12-41f1-ad44-8662185ddedf)


   - Edite as automações disponíveis na plataforma para otimizar as tarefas da aplicação.

![4 Captura de tela_9-11-2024_93439_manage wix com](https://github.com/user-attachments/assets/d467e0ce-9171-4680-bd8c-bb1902cb2b85)


2.1.1 **Edição do site**:

   - Clique em "Editar site" para realizar o front-end da aplicação contendo os elementos, as informações, seções, páginas, menu;
   - Realize os ajustes necessários na opção de Design;

![5 Captura de tela_9-11-2024_93946_editor wix com](https://github.com/user-attachments/assets/ef1afac5-e217-40e5-9e72-0d1d13a7ae30)


   - Edite o site para a visualização nas plataformas Deskop e Mobile para proporcionar uma experiência multiplataforma.
     

2.1.2 **Salvar, Visualizar e Publicar**:
   - Após as edições salve o projeto;
   - Visualize para a verificação das telas e funcionalidades;
   - Publique para disponibilizar o site para acesso ao público.

![image](https://github.com/user-attachments/assets/ed07690d-d9b1-42c9-a53c-e0df14077131)


3. **Execute o script**:
   - Clique no botão de **Executar** (ícone de raio) ou pressione **Ctrl + Enter** para rodar o script e criar as tabelas e o usuário padrão.

   ![Executando script](https://github.com/user-attachments/assets/2da67832-1186-4bdc-9d73-834e1f49418a)

4. **Atualize o schema para verificar as tabelas criadas**:
   - No painel esquerdo, clique com o **botão direito** sobre o banco de dados e selecione **Refresh All** para atualizar a visualização.

   ![Atualizando schema](https://github.com/user-attachments/assets/ab3322df-9c3f-4b90-bc65-19ce50c064f7)

5. **Verifique o usuário admin**:
   - Agora, você deve ter um **usuário admin** registrado na tabela, pronto para ser utilizado nos testes e na aplicação.

   ![Usuário admin](https://github.com/user-attachments/assets/bb11c043-d033-4685-8de7-6d75798708d8)

---

Seguindo esses passos, você terá o banco de dados configurado e pronto para uso com o projeto.

### 3. **Rode a API Node.js**

Certifique-se de acessar o terminal na raiz do projeto da API para executar as instruções abaixo.

#### 1. **Instale as dependências**

Execute o comando abaixo para instalar todas as dependências necessárias:

```bash
npm install
```

#### 2. **Configure as variáveis de ambiente**

Crie um arquivo chamado `prod.env` na raiz do projeto com as seguintes configurações:

> **Dica:** Verifique se as configurações para se conectar ao MySQL estão corretas. Por padrão, o host, port e user são definidos como abaixo, mas ajuste conforme necessário para sua conexão.

Além disso, você encontrará configurações opcionais para salvar imagens na AWS S3. Caso não configure esses campos, o sistema continuará funcional, mas sem suporte para upload de imagens.

PORT=3000  
MY_SQL_HOST="localhost"  
MY_SQL_PORT="3306"  
MY_SQL_USER="root"  
MY_SQL_PASSWORD=""  
MY_SQL_DATABASE="my_light_app"  
AWS_BUCKET=  
AWS_REGION=  
AWS_ACCESS_KEY_ID=  
AWS_SECRET_ACCESS_KEY=  

> **Nota:** Se a porta 3000 estiver em uso, você pode alterá-la no arquivo `prod.env` modificando o valor da variável PORT.

#### 3. **Inicie a API**

Compile e inicie a API com o comando:

```bash
npm rum build:ts
npm run build
```

#### 4. **Acesse a API**

A API estará disponível no endereço:  
<http://localhost:3000>  

Caso a porta 3000 esteja ocupada, altere o valor no arquivo `prod.env`.

#### 5. **Testando a API**

Verifique se tudo está funcionando corretamente acessando a seguinte URI no navegador:  
<http://localhost:3000/casas>  

Isso irá listar os registros de "casas" disponíveis para logar no sistema, como a casa padrão.

![Listagem de casas](https://github.com/user-attachments/assets/a69ed109-da9f-4e0d-9deb-4183e300b356)

### 4. **Rodar o projeto front-end Flutter**

Caso tenha dificuldades de configurar o ambiente para rodar o Flutter, acompanhe este vídeo:  
[Como configurar ambiente Flutter](https://www.youtube.com/watch?v=42jiTBFmeIA)

#### 1. **Instale as dependências**

No diretório do projeto (pasta `front`), instale todas as dependências necessárias com o comando:

```bash
flutter pub get
```

#### 2. **Configure um dispositivo para rodar o projeto**

- **Emulador Android**: Inicie um emulador pelo Android Studio.

#### 3. **Rode o projeto**

Certifique-se de que um dispositivo ou emulador está disponível e execute:

```bash
flutter run
```

> **Dica**: Se estiver usando o VSCode, verifique se o emulador carregou corretamente, se o projeto está aberto na raiz e se o dispositivo foi detectado.

![Verificação no VSCode](https://github.com/user-attachments/assets/0af6fd40-2819-44e6-a675-abe655494dfc)

#### 4. **Defina o domínio da API**

Durante a execução, o sistema pedirá que você informe o **domínio da API**. Isso é necessário porque o projeto foi pensado como um **white label**, e cada servidor depende do "condomínio" em questão.

![Selecionando Domínio da API](https://github.com/user-attachments/assets/283cec70-efea-4237-91dd-2e658fb204f9)

- **Emulador Android**: Caso a API esteja rodando localmente, utilize:  
  <http://10.0.2.2:3000>

- **Dispositivo Físico ou emulador iOS**: Utilize:  
  <http://localhost:3000>

> **Nota**: Certifique-se de que a API está rodando na porta correta. Verifique a porta em uso.

![Verificação da API](https://github.com/user-attachments/assets/2310432d-d3db-45d6-9771-4e308f299137)

#### 5. **Feche e abra o sistema**

Após definir o domínio da API, o sistema solicitará que você o reinicie. Em seguida, realize o login com um usuário já registrado.

#### 6. **Login no sistema**

Utilize um usuário registrado na tabela de "casas", como o usuário **DEFAULT**, para acessar o sistema.

![Login com usuário DEFAULT](https://github.com/user-attachments/assets/ade25f58-bfe9-4483-8a31-8318978fe743)

---

Seguindo esses passos, o projeto Flutter estará em execução e você poderá utilizar o sistema conforme necessário.
