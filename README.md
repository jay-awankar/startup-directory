<div align="center">
  <br />
    <img src="https://github.com/user-attachments/assets/471e2baa-8781-43b8-aaed-62e313d03e99" alt="Project Banner">
  <br />

  <div>
    <img src="https://img.shields.io/badge/-Typescript-black?style=for-the-badge&logoColor=white&logo=react&color=3178C6" alt="typescript" />
    <img src="https://img.shields.io/badge/-Next_JS-black?style=for-the-badge&logoColor=white&logo=nextdotjs&color=000000" alt="nextdotjs" />
    <img src="https://img.shields.io/badge/-Tailwind_CSS-black?style=for-the-badge&logoColor=white&logo=tailwindcss&color=06B6D4" alt="tailwindcss" />
    <img src="https://img.shields.io/badge/-Sanity-black?style=for-the-badge&logoColor=white&logo=sanity&color=F03E2F" alt="sanity" />

  </div>

<h3 align="center">Startup Directory Platform</h3>

   <div align="center">
     This project is built in <b>Next.js</b> using <b>TailwindCSS</b> and <b>Sanity</b>.
    </div>
</div>

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)
5. 🚀 [Code Flow](#code-flow)

## <a name="introduction">🤖 Introduction</a>

A Next.js 15 platform where entrepreneurs can submit their startup ideas for virtual pitch competitions, browse other
pitches, and gain exposure through a clean minimalistic design for a smooth user experience.

## <a name="tech-stack">⚙️ Tech Stack</a>

- React 19
- Next.js 15
- Sanity
- TailwindCSS
- ShadCN
- TypeScript

## <a name="features">🔋 Features</a>

👉 **Live Content API**: Displays the latest startup ideas dynamically on the homepage using Sanity's Content API.

👉 **GitHub Authentication**: Allows users to log in easily using their GitHub account.

👉 **Pitch Submission**: Users can submit startup ideas, including title, description, category, and multimedia links (
image or video).

👉 **View Pitches**: Browse through submitted ideas with filtering options by category.

👉 **Pitch Details Page**: Click on any pitch to view its details, with multimedia and description displayed.

👉 **Profile Page**: Users can view the list of pitches they've submitted.

👉 **Editor Picks**: Admins can highlight top startup ideas using the "Editor Picks" feature managed via Sanity Studio.

👉 **Views Counter**: Tracks the number of views for each pitch instead of an upvote system.

👉 **Search**: Search functionality to load and view pitches efficiently.

👉 **Minimalistic Design**: Fresh and simple UI with only the essential pages for ease of use and a clean aesthetic.

and many more, including the latest **React 19**, **Next.js 15** and **Sanity** features alongside code architecture and
reusability

## <a name="quick-start">🤸 Quick Start</a>

**Prerequisites**

- [Git](https://git-scm.com/)
- [Node.js](https://nodejs.org/en)
- [npm](https://www.npmjs.com/) (Node Package Manager)



Replace the placeholder values with your actual Sanity credentials. You can obtain these credentials by signing up &
creating a new project on the [Sanity website](https://www.sanity.io/).


## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying) for more details.


## <a name="code-flow">🚀 Code Flow</a>

**Create App**
```bash
npm i create-next-app@latest ./
```
```bash
Typescript
ESLint
Tailwindcss
No SRC directory
App Router
Turbopack
```

**Next Auth**
```bash
npm i next-auth@beta
npx auth secret
```

**Setup Next Auth** [Visit](https://authjs.dev/getting-started/installation)

create auth.ts in root directory <br />
import nextauth and specify provider (GitHub) <br />
mkdir in app as >> api >> auth >> [...nextauth] <br />
authentication >> OAuth >> GitHub >> Developer Setting >> New OAuth App
```env
AUTH_SECRET= 
AUTH_GITHUB_ID=
AUTH_GITHUB_SECRET=
```

**Tailwind Dependencies**
```bash
npm i tailwindcss-animate
npm i @tailwindcss/typography
```

**Add Global Css**
```bash
@layer utilities 
    {
    .class-name 
        {
        @apply styles
    }
}
```

**ShadCN**
```bash
npx shadcn@latest init
```
add components as required

**Setup Sanity** [Visit](https://www.sanity.io/)
```bash
npm create sanity@latest -- --project "key" --dataset production --template clean
npm i next-sanity@canary
```
remove --turbo from dev (SCRIPT) <br />
sanity schema

**Set Up Environment Variables**

create a new file named `.env.local` in the root of your project and add the following content:

```env
NEXT_PUBLIC_SANITY_PROJECT_ID=
NEXT_PUBLIC_SANITY_DATASET=
NEXT_PUBLIC_SANITY_API_VERSION='vX'

AUTH_SECRET= 
AUTH_GITHUB_ID=
AUTH_GITHUB_SECRET=
```

**StartupCardType**
```bash
npx sanity@latest schema extract --path=./sanity/extract.json
npx sanity@latest typegen generate
```

**Update SCRIPT** (package.json)
``bash
"predev": "npm run typegen", 
"prebuild": "npm run typegen",
"typegen": "sanity schema extract --path=./sanity/extract.json && sanity typegen generate"
```
```bash
npm run typegen
```

**Sanity Write Token**

create api token in sanity in your project
update env file:
```env
SANITY_WRITE_TOKEN=
```

**Other Installatons**

```bash
npm i @types/markdown-it

npm i @uiw/react-md-editor

npm i slugify
```

Slugify - to transform a string into web url