# Atividades Node.js, NPM & React

## Como comecar

```bash
# 1. Instalar dependencias
npm install

# 2. Iniciar servidor de desenvolvimento
npm run dev

# 3. Abrir no navegador (geralmente http://localhost:5173)

# 4. Editar src/App.jsx e salvar - o navegador atualiza automaticamente!
```

---

## Exercicio 1 - react-icons (EXEMPLO PRONTO)

**Pacote:** `react-icons` - Milhares de icones prontos
**Status:** Ja implementado como referencia
```bash
npm install react-icons
```

```jsx
import { FaReact, FaNodeJs } from 'react-icons/fa'
<FaReact color="#61dafb" />
```

---

## Exercicio 2 - react-confetti

**Pacote:** `react-confetti` - Confetes animados na tela

```bash
npm install react-confetti
```

**Passos:**
1. Descomente `import Confetti from 'react-confetti'`
2. Na area de preview, adicione:
   ```jsx
   {showConfetti && <Confetti width={window.innerWidth} height={window.innerHeight} />}
   ```

---

## Exercicio 3 - dayjs

**Pacote:** `dayjs` - Datas faceis de manipular

```bash
npm install dayjs
```

**Passos:**
1. Descomente `import dayjs from 'dayjs'`
2. Substitua os `???` na preview por chamadas dayjs:
   - `dayjs().format('DD/MM/YYYY')`
   - `dayjs().format('HH:mm:ss')`
   - `dayjs().format('dddd')`
   - `dayjs('2026-12-25').diff(dayjs(), 'day')`
   - `dayjs().diff(dayjs('2000-01-01'), 'day')`

---

## Exercicio 4 - react-toastify

**Pacote:** `react-toastify` - Notificacoes bonitas

```bash
npm install react-toastify
```

**Passos:**
1. Descomente os 2 imports (ToastContainer, toast e o CSS)
2. Adicione `<ToastContainer />` antes do `</>`
3. Substitua os `alert()` por `toast.success()`, `toast.error()`, etc.

---

## Exercicio 5 - uuid

**Pacote:** `uuid` - IDs unicos

```bash
npm install uuid
```

**Passos:**
1. Descomente `import { v4 as uuidv4 } from 'uuid'`
2. No onClick do botao "Adicionar", crie o usuario:
   ```jsx
   const novoUsuario = {
     id: uuidv4(),
     nome: nomeInput,
     criadoEm: new Date().toLocaleString()
   }
   setUsuarios([...usuarios, novoUsuario])
   setNomeInput('')
   ```

---

## Exercicio 6 - react-spinners

**Pacote:** `react-spinners` - Animacoes de carregamento

```bash
npm install react-spinners
```

**Passos:**
1. Descomente o import dos spinners
2. Substitua os `<span>` pelos componentes:
   ```jsx
   <ClipLoader color="#58a6ff" loading={loading} size={50} />
   <BounceLoader color="#7ee787" loading={loading} size={60} />
   ```

---

## Exercicio 7 - react-type-animation

**Pacote:** `react-type-animation` - Efeito de maquina de escrever

```bash
npm install react-type-animation
```

**Passos:**
1. Descomente o import
2. Substitua o `<h2>` estatico por:
   ```jsx
   <TypeAnimation
     sequence={['Eu amo React!', 2000, 'Eu amo Node.js!', 2000]}
     wrapper="h2"
     speed={50}
     repeat={Infinity}
     style={{ color: '#58a6ff' }}
   />
   ```

---

## Exercicio Bonus

Combine 2+ pacotes de forma criativa. Ideias no site!

---

## Comandos NPM aprendidos

| Comando | O que faz |
|---------|-----------|
| `npm init` | Cria o package.json |
| `npm install pacote` | Instala um pacote |
| `npm install` | Instala tudo do package.json |
| `npm run dev` | Roda o script "dev" (Vite) |
| `npm uninstall pacote` | Remove um pacote |
| `node_modules/` | Pasta com os pacotes instalados |
| `package-lock.json` | Trava as versoes exatas |
