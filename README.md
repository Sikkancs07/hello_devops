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

```text
my-devops-app/
├── .devcontainer/
│   ├── devcontainer.json
│   └── Dockerfile
├── app/
├── public/
├── package.json
├── vite.config.ts
├── Dockerfile
└── README.md
```
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
```

Ezután az alkalmazás elérhető a http://localhost:5173 címen.

Build (production)
npm run build


Ez a parancs a dist/ könyvtárba készíti el a production-ready fájlokat.

## 🐳 Docker használata
Docker image építése
docker build -t my-devops-app .

Docker konténer futtatása
docker run -p 4000:3000 my-devops-app


Ezután az alkalmazás elérhető a http://localhost:4000 címen.

## 💻 Dev Container

A projekt tartalmaz egy .devcontainer mappát, amely lehetővé teszi, hogy az alkalmazás egy konténerizált fejlesztői környezetben fusson (pl. GitHub Codespaces vagy VS Code Dev Containers használatával).

Klónozd le a repository-t. Ha zip-ként töltöd le, akkor a kibontásnál töröld a végéről a "-master" részt.


Dev Container használata lépésről lépésre:

```Ordered list
1. Nyisd meg a projektet VS Code-ban.
2. Telepítsd a Dev Containers bővítményt, ha még nincs.
3. Parancspaletta megnyitása: Ctrl + Shift + P
4. Válaszd: Dev Containers: Reopen in Container
5. Az első indulás után automatikusan fut az npm install
```

Indítsd az appot a konténeren belül:

```bash
npm run dev
```

A fejlesztői szerver elérhető lesz: http://localhost:5173


## 📝 Git (Trunk-based development)

A projekt Git verziókezeléssel készült

A main branch a trunk

A fejlesztés külön feature brancben történt

Minden commit jól olvasható, informatív üzenettel rendelkezik