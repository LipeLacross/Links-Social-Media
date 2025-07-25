## 🌐 [English Version of README](README_EN.md)

# Links de Redes Sociais

Centralizador de links de redes sociais com visual moderno, animações e tela de carregamento personalizada. Desenvolvido em **Vue 3** juntamente com **Vite**, este projeto serve como um hub rápido e responsivo para você divulgar todos os seus contatos profissionais e sociais em um só lugar.

## 🔨 Funcionalidades do Projeto

- **Visualização do Perfil:** Foto de perfil animada, nome e profissão.
- **Links Sociais:** Acesso direto para Instagram, LinkedIn, YouTube, GitHub e portfólio, cada um com ícone e cor personalizados.
- **Animações Modernas:** Elementos animados ao passar o mouse, durante a entrada de componentes e interatividade ao clicar na foto.
- **Tela de Carregamento:** Splash screen com loading, mensagens motivacionais e barra de progresso.

### 📸 Exemplo Visual do Projeto

![chrome-capture-2024-9-14](https://github.com/user-attachments/assets/7da67b9d-cb01-46e8-be42-8c2793d31adb)

## ✔️ Técnicas e Tecnologias Utilizadas

- **Vue.js 3:** Construção de interface/user experience.
- **JavaScript ES6+:** Interatividade, lógica de animação e componentes.
- **HTML5:** Estrutura.
- **CSS3:** Estilos modernos, responsividade e animações avançadas.
- **Vite:** Desenvolvimento e build ultra rápido.
- **Vercel:** Deploy contínuo e hospedagem estática.

## 📁 Estrutura do Projeto

- **public/**
  - favicon.ico: Ícone do site.
- **README.md / README_EN.md:** Documentação (pt-BR e inglês).
- **index.html:** HTML principal do app.
- **jsconfig.json:** Configuração de caminho de imports JS/TS.
- **package.json / package-lock.json:** Dependências e scripts do projeto.
- **vite.config.js:** Alias e configuração do Vite.
- **src/**
  - **App.vue:** Componente raiz que carrega tela de loading e links sociais.
  - **main.js:** Ponto de entrada da aplicação Vue.
  - **assets/:** Imagens e ícones (perfil, logos e redes).
  - **components/**
    - **LoadingScreen.vue:** Tela de loading personalizada com animação e mensagens motivacionais.
    - **SocialLinks.vue:** Bloco principal com perfil e links para redes sociais.

## 🛠️ Abrir e Rodar o Projeto

Para iniciar o projeto localmente, siga os passos abaixo:

1. **Certifique-se de que o Node.js está instalado**:
   - O [Node.js](https://nodejs.org/) é necessário para rodar o projeto. Você pode verificar com:
     ```
     node -v
     ```
   - Se não estiver instalado, baixe a versão recomendada no site.

2. **Clone o Repositório**:
   - Execute no terminal:
     ```
     git clone https://github.com/LipeLacross/Links-Social-Media.git
     cd Links-Social-Media
     ```

3. **Instale as dependências**:
   ```
   npm install
   ```

4. **Inicie o servidor de desenvolvimento**:
   ```
   npm run dev
   ```
   - Abra o navegador em [http://localhost:5173](http://localhost:5173) ou na porta mostrada pelo terminal.

## 🌐 Deploy

- O projeto pode ser publicado rapidamente no **Netlify**, **Vercel** ou qualquer host de páginas estáticas que rode Node.js/Vite.
- Para deploy no Netlify:
  1. Faça login em [netlify.com](https://www.netlify.com/).
  2. Clique em "New Site from Git", conecte sua conta do GitHub e escolha o repositório.
  3. Em **build command**, use: `npm run build`
  4. Em **publish directory**, use: `dist`
  5. Complete o processo e seu site estará online!
