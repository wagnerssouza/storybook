
# Storybook

### 1. Crie um projeto Angular 
`npx -p @angular/cli ng new storybook`  
 
### 2. Adicione o storybook ao projeto
Digite: `cd storybook` e depois `npx -p @storybook/cli sb init` 

Para maiores informações, acesse:  
[https://www.learnstorybook.com/intro-to-storybook/angular/pt/get-started/](https://www.learnstorybook.com/intro-to-storybook/angular/pt/get-started/)

### 3. Crie um simples componente
Vamos criar um simples componente `button`, ele também servirá para a  exibição no storybook

Acesse `cd src/app` e para criar o component: `ng g c button`  
Você pode ver a estrura do componente criado aqui:  
`caminho github do component`

### 4. Criando arquivo .stories
Na estrutura do componente `button` que acabamos de criar, vamos adicionar nossa storie. 

Crie um arquivo, por ex: `button.stories.ts`. O nome do arquivo precisa necessariamente ter `.stories.ts`.

### 5. Criando uma storie simples
```javascript
import { ButtonComponent } from  './button.component';
export const ButtonStorie = () => ({
  component:  ButtonComponent,
});
```
`link do github do button.stories`

### 6. Acesse o diretório `src/stories` e crie seus arquivos `.stories`
Em `src/stories` você pode criar seus arquivos para agrupar stories.

A própria instalação do storybook cria 2 deles:
`0-Welcome.stories.ts` e `1-Button.stories.ts`

### 7. Agrupando `stories`
acesse o arquivo `1-Button.stories.ts` em `src/stories` que foi criado quando adicionamos o storybook no nosso projeto.  

Apague todo o conteúdo e adicione o código abaixo:

```javascript
import { storiesOf } from '@storybook/angular';
import { ButtonStorie } from 'src/app/button/button.stories';

storiesOf('Buttons', module)
  .add('Button - Default', ButtonStorie)
```

### 8. Executando em localhost

Para executar em localhost seu projeto, abra duas abas do seu terminal.

Angular - `http://localhost:4200` - comando `ng serve`  
Storybook - `http://localhost:6006` comando `npm run storybook`

ng serve  
rodar storybook
npm run storybook
