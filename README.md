### Configuração do ESLint para Cypress

Este projeto tem como objetivo configurar o ESLint para garantir boas práticas e padronização de código nos testes automatizados escritos com Cypress.

### ⚙️ Pré-requisitos

Node.js instalado

Projeto com Cypress já configurado

### Passo a passo da configuração

1️⃣ Instalar o ESLint

Instale a versão específica do ESLint utilizada no projeto:

```
npm i eslint@8.43.0 -D 

```

### 2️⃣ Inicializar o ESLint

Execute o comando abaixo para iniciar a configuração do ESLint:

```
npx eslint --init
```

Criar o arquivo **.eslintrc.json** na raiz do projeto.

Copie o conteúdo do arquivo abaixo:

```
{
  "env": {
    "browser": true,
    "es2021": true,
    "node": true
  },
  "extends": "eslint:recommended",
  "parserOptions": {
    "ecmaVersion": 12
  },
  "rules": {
    "indent": ["error", 2],
    "linebreak-style": ["error", "unix"],
    "quotes": ["error", "single"],
    "semi": ["error", "never"],
    "no-trailing-spaces": ["error"]
  }
}
```

### 3️⃣ Instalar o plugin do ESLint para Cypress

Instale a biblioteca para o Cypress:

```
npm i eslint-plugin-cypress@2.13.3 -D
```

### 4️⃣ Criar configuração específica para testes Cypress

Crie um arquivo **.eslintrc.json** dentro do diretório **cypress/** com o seguinte conteúdo:
```
{
  "extends": [
    "plugin:cypress/recommended"
  ],
  "rules": {
    "no-multiple-empty-lines": ["error", { "max": 0 }]
  }
}
```

**Obs:** As regras definidas acima podem ser personalizadas conforme a necessidade do projeto atuado, abaixo a documentação oficional do ESlint para mais detalhes:

https://eslint.org/docs/latest/rules/

### 📄 **Licença** ###
Este projeto está licenciado sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.