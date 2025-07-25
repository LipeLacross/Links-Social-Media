## 🌐 [English Version of README](README_EN.md)

# Social Media Links

A centralized hub for social media links with a modern look, smooth animations, and a custom loading screen. Built with **Vue 3** and **Vite**, this project serves as a fast and responsive platform to showcase all your professional and social contacts in one place.

## 🔨 Project Features

- **Profile View:** Animated profile picture, name, and profession.
- **Social Links:** Direct access to Instagram, LinkedIn, YouTube, GitHub, and portfolio, each with customized icons and colors.
- **Modern Animations:** Animated elements on hover, entry animations for components, and interactive profile picture click effects.
- **Loading Screen:** Splash screen with loading animation, motivational messages, and a progress bar.

### 📸 Visual Example of the Project

![chrome-capture-2024-9-14](https://github.com/user-attachments/assets/7da67b9d-cb01-46e8-be42-8c2793d31adb)

## ✔️ Technologies and Tools Used

- **Vue.js 3:** For building the user interface and experience.
- **JavaScript (ES6+):** For interactivity, animation logic, and component behavior.
- **HTML5:** Project structure.
- **CSS3:** Modern styles, responsiveness, and advanced animations.
- **Vite:** Fast development and build tool.
- **Vercel:** Continuous deployment and static hosting platform.

## 📁 Project Structure

- **public/**
  - `favicon.ico`: Website favicon.
- **README.md / README_EN.md:** Project documentation in Portuguese and English.
- **index.html:** Main HTML file of the app.
- **jsconfig.json:** JS/TS import path configuration.
- **package.json / package-lock.json:** Project dependencies and scripts.
- **vite.config.js:** Vite aliases and configuration.
- **src/**
  - **App.vue:** Root component that manages the loading screen and social links.
  - **main.js:** Vue application entry point.
  - **assets/**: Images and icons (profile pictures, logos, and social media icons).
  - **components/**
    - `LoadingScreen.vue`: Custom loading screen with animations and motivational messages.
    - `SocialLinks.vue`: Main block with profile and social media links.

## 🛠️ How to Run the Project

Follow the steps below to run the project locally:

1. **Ensure Node.js is installed**:
   - You can verify installation by running:
     ```
     node -v
     ```
   - If not installed, download the recommended version from [nodejs.org](https://nodejs.org/).

2. **Clone the repository**:
   ```
   git clone https://github.com/LipeLacross/Links-Social-Media.git
   cd Links-Social-Media
   ```

3. **Install dependencies**:
   ```
   npm install
   ```

4. **Start the development server**:
   ```
   npm run dev
   ```
   - Open your browser at [http://localhost:5173](http://localhost:5173), or the port displayed in your terminal.

## 🌐 Deployment

- The project can be deployed easily using **Netlify**, **Vercel**, or any static hosting service that supports Node.js/Vite.
- To deploy on Netlify:
  1. Log in to [netlify.com](https://www.netlify.com/).
  2. Click on "New Site from Git," connect your GitHub account, and select the repository.
  3. Set the build command to:
     ```
     npm run build
     ```
  4. Set the publish directory to:
     ```
     dist
     ```
  5. Complete the process and your site will be live!
