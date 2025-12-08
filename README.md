# My DevOps App

Ez a projekt egy egyszerű React + Vite alapú "Hello Word" webalkalmazás, amely bemutatja az alapvető DevOps lépéseket:

- Kódkészítés
- Verziókövetés (trunk-based Git használattal)
- Buildelés (`npm run build`)
- Dockerizálás
- Dev Container használata (VS Code támogatással)

A projekt HTTP-n keresztül elérhető:  
→ [http://localhost:5173](http://localhost:5173) (fejlesztés közben)  
→ [http://localhost:4000](http://localhost:4000) (Docker konténerből)

---

## ⚙️ Tech stack

- React + Vite
- Node.js 20
- Docker
- VS Code + Dev Containers bővítmény

---

## 📁 Projekt felépítése
my-devops-app/
├── public/
├── src/
├── .devcontainer/
│ ├── devcontainer.json
│ └── Dockerfile
├── package.json
├── vite.config.ts
├── Dockerfile
└── README.md

---

## 🧪 Előkészületek

A projekt futtatásához szükséges:

- [Node.js (v18+)](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [Visual Studio Code](https://code.visualstudio.com/)
  - **Dev Containers** bővítmény telepítve

---

## 📦 Telepítés és buildelés

A következő parancsok a projekt gyökerében (ahol a `package.json` található) futtathatók:

### Fejlesztői környezet indítása

```bash
npm install
npm run dev