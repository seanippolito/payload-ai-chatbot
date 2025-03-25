# Quick Start

The chatbot template is a web application built using [Next.js](https://nextjs.org) and the [AI SDK](https://sdk.vercel.ai) that can be used as a starting point for building your own AI applications. The template is designed to be easily customizable and extendable, allowing you to add new features and integrations as needed.

Deploying to [Vercel](https://vercel.com) is the quickest way to get started with the chatbot template, as it automatically sets up the project by connecting to integrations and deploys it to the cloud. You can then later develop the project locally and push changes to the Vercel project.

### Pre-requisites:

- Vercel account and [Vercel CLI](https://vercel.com/docs/cli)
- GitHub/GitLab/Bitbucket account
- API Keys from three AI model providers:
  - [xAI](https://console.x.ai/)
  - [Open Router](https://openrouter.ai/settings/keys)
  - [OpenAI](https://platform.openai.com/account/api-keys)
  - [Fireworks](https://fireworks.ai/account/api-keys)

### About Payload CMS

This project uses [Payload CMS](https://payloadcms.com) as its headless content management system. Payload CMS provides:

- A powerful admin interface for managing content
- Built-in authentication and authorization
- REST and GraphQL APIs
- TypeScript support
- Custom field types and validation
- File uploads and media management
- Role-based access control

The CMS is configured to work seamlessly with the chatbot template, allowing you to:

- Manage chat history and conversations
- Configure AI model settings
- Store and manage user data
- Customize the chatbot's behavior and appearance

#### Accessing the Admin Interface

The Payload CMS admin interface is available at `/admin` after deployment. You can access it by:

1. Visiting your deployed site
2. Adding `/admin` to the URL
3. Logging in with your admin credentials

#### Key Features

- **Content Management**: Create and manage content types for your chatbot
- **User Management**: Handle user roles and permissions
- **Media Library**: Upload and manage files and images
- **API Access**: Use REST or GraphQL APIs to interact with your content
- **Custom Fields**: Define custom field types for specific needs
- **Access Control**: Set up role-based permissions for different user types

#### Environment Variables

Make sure to set up the following environment variables for Payload CMS:

```env
PAYLOAD_SECRET=your-secret-key
```

### Deploy to Vercel

To deploy the chatbot template to Vercel, click the button below to enter the 1-click deploy flow.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fvercel%2Fai-chatbot&env=AUTH_SECRET&envDescription=Generate%20a%20random%20secret%20to%20use%20for%20authentication&envLink=https%3A%2F%2Fgenerate-secret.vercel.app%2F32&project-name=my-awesome-chatbot&repository-name=my-awesome-chatbot&demo-title=AI%20Chatbot&demo-description=An%20Open-Source%20AI%20Chatbot%20Template%20Built%20With%20Next.js%20and%20the%20AI%20SDK%20by%20Vercel&demo-url=https%3A%2F%2Fchat.vercel.ai&products=%5B%7B%22type%22%3A%22integration%22%2C%22protocol%22%3A%22ai%22%2C%22productSlug%22%3A%22grok%22%2C%22integrationSlug%22%3A%22xai%22%7D%2C%7B%22type%22%3A%22integration%22%2C%22protocol%22%3A%22ai%22%2C%22productSlug%22%3A%22api-key%22%2C%22integrationSlug%22%3A%22groq%22%7D%2C%7B%22type%22%3A%22integration%22%2C%22protocol%22%3A%22storage%22%2C%22productSlug%22%3A%22neon%22%2C%22integrationSlug%22%3A%22neon%22%7D%2C%7B%22type%22%3A%22blob%22%7D%5D)

During the flow, you will be prompted to create and connect to a postgres database and blob store. You will also need to provide environment variables for the application.

After deploying the project, you can access the chatbot template by visiting the URL provided by Vercel.

### Local Development

To develop the chatbot template locally, you can clone the repository and link it to your Vercel project. This will allow you to pull the environment variables from the Vercel project and use them locally.

```bash
git clone https://github.com/<username>/<repository>
cd <repository>
pnpm install

vercel link
vercel env pull
```

After linking the project, you can start the development server by running:

```bash
pnpm dev
```

The chatbot template will be available at `http://localhost:3000`.
