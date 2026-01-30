# 🛋️ FurniMarket

> O marketplace móvel definitivo para comprar e vender móveis únicos.

![Badge License](https://img.shields.io/badge/license-MIT-green)
![Badge React Native](https://img.shields.io/badge/React_Native-0.72-blue)
![Badge Expo](https://img.shields.io/badge/Expo-49-black)
![Badge TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)

## 📄 Sobre o Projeto

O **FurniMarket** é um aplicativo mobile desenvolvido para facilitar a conexão entre vendedores e compradores de móveis usados e artesanais. Com uma interface limpa e intuitiva, o app permite anunciar produtos, favoritar itens de interesse e entrar em contato direto com vendedores via WhatsApp.

O projeto foi construído utilizando a arquitetura moderna do **Expo Router** e foca em performance e experiência do usuário (UX).

---

## ✨ Funcionalidades

* **🔐 Autenticação Segura:** Login e cadastro de usuários via **Clerk**.
* **🏠 Feed Interativo:** Listagem de produtos com rolagem infinita e atualização (pull-to-refresh).
* **🔍 Busca Inteligente:** Pesquisa em tempo real por título ou descrição do móvel.
* **❤️ Favoritos:** Sistema para curtir e salvar anúncios, persistindo a escolha do usuário.
* **📸 Upload de Imagens:** Integração nativa com Câmera e Galeria para fotos dos produtos.
* **📦 Gestão de Anúncios (CRUD):** O usuário pode criar, editar e excluir seus próprios anúncios.
* **💬 Contato Direto:** Deep Linking para abrir conversa no WhatsApp ou discador do celular.
* **📱 Design Responsivo:** Interface adaptada para iOS e Android, respeitando Safe Areas (Notch/Ilha Dinâmica).

---

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido utilizando as seguintes tecnologias:

* **[React Native](https://reactnative.dev/)** - Framework principal.
* **[Expo](https://expo.dev/)** - Plataforma de desenvolvimento e Build.
* **[Expo Router](https://docs.expo.dev/router/introduction/)** - Roteamento baseado em arquivos.
* **[TypeScript](https://www.typescriptlang.org/)** - Tipagem estática para segurança do código.
* **[Clerk](https://clerk.com/)** - Gestão de Autenticação e Usuários.
* **[PostgreSQL](https://www.postgresql.org/)** - Banco de dados (via Drizzle/Prisma ou drivers diretos).
* **Safe Area Context** - Gestão de insets para dispositivos modernos.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos

* Node.js instalado.
* Gerenciador de pacotes (NPM ou Yarn).
* App **Expo Go** instalado no seu celular (ou emulador Android/iOS configurado).

### Instalação

1.  **Clone o repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/furnimarket.git](https://github.com/seu-usuario/furnimarket.git)
    cd furnimarket
    ```

2.  **Instale as dependências:**
    ```bash
    npm install
    # ou
    yarn install
    ```

3.  **Configure as Variáveis de Ambiente:**
    Crie um arquivo `.env` na raiz do projeto e adicione suas chaves (exemplo):
    ```env
    EXPO_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_...
    DATABASE_URL=postgres://...
    ```

4.  **Execute o projeto:**
    ```bash
    npx expo start
    ```

5.  **Abra no celular:**
    Escaneie o QR Code gerado no terminal com o app **Expo Go**.

---

## 📂 Estrutura de Pastas

A arquitetura do projeto segue o padrão de componentes atomizados e roteamento do Expo:


```
furnimarket/
├── app/                     # Rotas e Telas (Expo Router)
│ ├── (app)/                 # Telas autenticadas
│ │ ├── (tabs)/              # Navegação inferior
│ │ ├── details/[id].tsx     # Detalhes do item
│ │ └── edit/[id].tsx        # Edição do item
│ └── _layout.tsx            # Layout Raiz (Providers)
└── src/
  ├── components/            # Componentes Reutilizáveis
  │ ├── feed/                # Componentes do Feed (Card, Header)
  │ ├── item-details/        # Componentes de Detalhes
  │ └── my-items/            # Componentes de Meus Anúncios
  ├── db/                    # Lógica de Banco de Dados (Schema, Actions)
  └── hooks/                 # Hooks customizados
```
---

# Imagens do projeto

<img width="1080" height="752" alt="Untitled design (3)" src="https://github.com/user-attachments/assets/d580c119-d7ca-4285-9b2c-756943c1a584" />

---

## 📝 Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Feito com 💜 pela equipe FurniMarket.
