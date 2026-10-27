<img width="1200" height="300" alt="banner" src="https://github.com/user-attachments/assets/fe5fb7cf-8ffe-4995-a893-9b3f70968e95" /><div align="center">

![Up<svg xmlns="http://www.w3.org/2000/svg" width="1200" height="300" viewBox="0 0 1200 300">
  <defs>
    <linearGradient id="bg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#050505"/>
      <stop offset="100%" stop-color="#1a1a1a"/>
    </linearGradient>
    <radialGradient id="glow" cx="0.15" cy="0.5" r="0.6">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0.07"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0"/>
    </radialGradient>
    <linearGradient id="slab" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0.10"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0.02"/>
    </linearGradient>

    <!-- Grille -->
    <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M40 0 L0 0 0 40" fill="none" stroke="#ffffff" stroke-width="1"/>
    </pattern>
    <!-- La grille s'efface vers la gauche pour laisser le texte lisible -->
    <linearGradient id="fadeGrad" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0.15"/>
      <stop offset="55%" stop-color="#ffffff" stop-opacity="0.6"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="1"/>
    </linearGradient>
    <mask id="fade">
      <rect width="1200" height="300" fill="url(#fadeGrad)"/>
    </mask>

    <!-- Faisceau lumineux qui parcourt la grille -->
    <linearGradient id="beam" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#ffffff" stop-opacity="0"/>
      <stop offset="50%" stop-color="#ffffff" stop-opacity="0.10"/>
      <stop offset="100%" stop-color="#ffffff" stop-opacity="0"/>
    </linearGradient>

    <!-- Reflet qui balaie le nom -->
    <linearGradient id="shine" x1="0" y1="0" x2="1" y2="0">
      <stop offset="0%" stop-color="#000000" stop-opacity="0"/>
      <stop offset="50%" stop-color="#000000" stop-opacity="0.5"/>
      <stop offset="100%" stop-color="#000000" stop-opacity="0"/>
    </linearGradient>
    <clipPath id="nameClip">
      <text x="80" y="150" class="name">Baptiste Wagée</text>
    </clipPath>

    <!-- Effet machine à écrire -->
    <clipPath id="typing">
      <rect x="80" y="195" width="595" height="40">
        <animate attributeName="width" values="0;595;595;0" keyTimes="0;0.35;0.9;1" dur="8s" repeatCount="indefinite"/>
      </rect>
    </clipPath>

    <style>
      .cursor { animation: blink 1s steps(1) infinite; }
      @keyframes blink { 50% { opacity: 0 } }
      .name { font: 800 64px 'Segoe UI', 'Helvetica Neue', Arial, sans-serif; }
      .sub  { font: 500 20px 'Segoe UI', 'Helvetica Neue', Arial, sans-serif; letter-spacing: 5px; }
      .wave { fill: none; stroke: #ffffff; stroke-linecap: round; }
    </style>
  </defs>

  <!-- Fond -->
  <rect width="1200" height="300" fill="url(#bg)"/>

  <!-- Grille qui défile doucement -->
  <g mask="url(#fade)" opacity="0.07">
    <rect x="-40" y="-40" width="1280" height="380" fill="url(#grid)">
      <animateTransform attributeName="transform" type="translate" values="0,0;40,40" dur="4s" repeatCount="indefinite"/>
    </rect>
  </g>

  <!-- Faisceau -->
  <rect x="-300" y="0" width="300" height="300" fill="url(#beam)">
    <animate attributeName="x" values="-300;1200" dur="5s" repeatCount="indefinite"/>
  </rect>

  <rect width="1200" height="300" fill="url(#glow)"/>

  <!-- Bande diagonale -->
  <path d="M1200 0 L940 0 L800 300 L1200 300 Z" fill="url(#slab)"/>
  <path d="M1200 40 L1010 40 L890 300 L1200 300 Z" fill="#ffffff" opacity="0.04"/>
  <line x1="940" y1="0" x2="800" y2="300" stroke="#ffffff" stroke-opacity="0.25" stroke-width="1"/>

  <!-- Vagues animées (période 600px, elles bouclent sans coupure) -->
  <path class="wave" stroke-opacity="0.22" stroke-width="2"
        d="M0 255 C150 225 150 225 300 255 S450 285 600 255 S750 225 900 255 S1050 285 1200 255 S1350 225 1500 255 S1650 285 1800 255">
    <animateTransform attributeName="transform" type="translate" values="0,0;-600,0" dur="9s" repeatCount="indefinite"/>
  </path>
  <path class="wave" stroke-opacity="0.13" stroke-width="1.5"
        d="M0 268 C150 238 150 238 300 268 S450 298 600 268 S750 238 900 268 S1050 298 1200 268 S1350 238 1500 268 S1650 298 1800 268">
    <animateTransform attributeName="transform" type="translate" values="-600,0;0,0" dur="12s" repeatCount="indefinite"/>
  </path>
  <path class="wave" stroke-opacity="0.08" stroke-width="1"
        d="M0 240 C150 200 150 200 300 240 S450 280 600 240 S750 200 900 240 S1050 280 1200 240 S1350 200 1500 240 S1650 280 1800 240">
    <animateTransform attributeName="transform" type="translate" values="0,0;-600,0" dur="15s" repeatCount="indefinite"/>
  </path>

  <!-- Nom -->
  <text x="80" y="150" class="name" fill="#ffffff">Baptiste Wagée</text>
  <g clip-path="url(#nameClip)">
    <rect x="-200" y="80" width="120" height="90" fill="url(#shine)" transform="skewX(-20)">
      <animate attributeName="x" values="-200;800;800" keyTimes="0;0.4;1" dur="6s" repeatCount="indefinite"/>
    </rect>
  </g>

  <!-- Trait qui s'allonge -->
  <rect x="82" y="178" width="44" height="4" rx="2" fill="#ffffff">
    <animate attributeName="width" values="44;110;44" dur="4s" repeatCount="indefinite"/>
  </rect>

  <!-- Sous-titre tapé -->
  <text x="82" y="222" class="sub" fill="#bdbdbd" clip-path="url(#typing)">DÉVELOPPEUR WEB · BUT INFORMATIQUE</text>
  <rect class="cursor" x="677" y="204" width="3" height="24" fill="#ffffff">
    <animate attributeName="x" values="82;677;677;82" keyTimes="0;0.35;0.9;1" dur="8s" repeatCount="indefinite"/>
  </rect>
</svg>
loading banner.svg…]()



[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/baptiste-wag%C3%A9e-a79844392/)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://baptistewagee.fr)
[![Gmail](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:wageebaptiste.pro@gmail.com)

</div>

---

## 👨‍💻 À propos de moi

Passionné par le web, l'IA et les nouvelles technologies, j'ai déjà conçu différentes applications, dont une application d'information sportive utilisée par une communauté internationale. Ce profil GitHub centralise mes projets académiques et personnels, et me sert à documenter ma progression technique (versioning, structuration du code, bonnes pratiques).

- 🎓 **Formation actuelle :** BUT Informatique — IUT de l'Artois, Lens (depuis 2025)

---

## 🛠️ Mes projets

| Projet | Description | Langages |
| :--- | :--- | :--- |
| 🌐 **[Portfolio personnel](https://baptistewagee.fr)** | Mon site portfolio, hébergé sur Vercel avec un nom de domaine personnel (baptistewagee.fr). | HTML, CSS, JS |
| 🏎️ **[Overtake](https://github.com/baptiste-wagee/Overtake)** | Projet web personnel sur la F1 : interface responsive et moderne, intégration de modules dynamiques en JavaScript, gestion et versioning du code via GitHub. | HTML, CSS, JS |
| 👻 **[Pacman](https://github.com/baptiste-wagee/PacMan)** | Projet Java Pro : gestion des interfaces FXML, gestion du code pour les bots et la carte (map), suivi des bugs et des versions via Git. | Java, FXML |
| 🍕 **[Pizz'Eli](https://github.com/baptiste-wagee/Pizz-Eli)** | Site vitrine "one-page" pour une pizzeria : structure épurée et moderne, alignement et organisation soignés, animations JavaScript (dont une transition de logo au scroll). | HTML, CSS, JS |
| 💡 **[Lights-Off](https://github.com/baptiste-wagee/Lights-Off)** | Jeu de réflexion et de logique en JavaFX : éteindre une grille de lumières en gérant l'inversion d'état des voisins (projet du module R2.02). | Java, JavaFX |
| 🐾 **[Tamagotchi](https://github.com/baptiste-wagee/Tamagotchi/tree/main)** | Apprentissage de la programmation orientée objet en Java à travers la création d'un animal virtuel. | Java |
| 🎵 **[JS Wagee](https://github.com/baptiste-wagee/Site-JS-Wagee)** | Site vitrine réalisé pour mettre en avant des productions musicales. | HTML, CSS |

---

## 📝 Langages & technologies

<p align="left">
  <img src="https://skillicons.dev/icons?i=html,css,js,php,md,java,py,mysql,bash" />
</p>

## 💻 Logiciels & outils

<p align="left">
  <img src="https://skillicons.dev/icons?i=vscode,idea,eclipse,git,github,gitlab,gradle" />
</p>

![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=flat-square&logo=wireshark&logoColor=white)
![Canva](https://img.shields.io/badge/Canva-00C4CC?style=flat-square&logo=canva&logoColor=white)
![Microsoft Office](https://img.shields.io/badge/Office-D83B01?style=flat-square&logo=microsoft-office&logoColor=white)

## 🖥️ Systèmes

<p align="left">
  <img src="https://skillicons.dev/icons?i=windows,linux" />
</p>

<div align="center">

## ✉️ Me contacter

Si mon profil ou mes compétences vous intéressent pour une alternance, un stage ou un projet, n'hésitez pas à me contacter :

📧 [wageebaptiste.pro@gmail.com](mailto:wageebaptiste.pro@gmail.com) • 💼 [LinkedIn](https://www.linkedin.com/in/baptiste-wag%C3%A9e-a79844392/) • 🌐 [baptistewagee.fr](https://baptistewagee.fr)

</div>
