# GHO Semantic search with Langchain, Pinecone, and GPT with Next.js

## Running the app

In this section I will walk you through how to deploy and run this app.

### Prerequisites

To run this app, you need the following:

1. An [OpenAI](https://platform.openai.com/) API key
2. [Pinecone](https://app.pinecone.io/) API Key

### Up and running

To run the app locally, follow these steps:

1. Clone this repo

```sh
git clone git@github.com:dabit3/semantic-search-nextjs-pinecone-langchain-chatgpt.git
```

2. Change into the directory and install the dependencies using either NPM or Yarn

3. Copy `.example.env.local` to a new file called `.env.local` and update with your API keys and environment.

    __Be sure your environment is an actual environment given to you by Pinecone, like `us-west4-gcp-free`__

4. (Optional) - Add your own custom text or markdown files into the `/documents` folder.

5. Run the app:

```sh
npm run dev
```

### Need to know

When creating the embeddings and the index, it can take up to 2-4 minutes for the index to fully initialize. There is a settimeout function of 180 seconds in the `utils` that waits for the index to be created.

If the initialization takes longer, then it will fail the first time you try to create the embeddings. If this happens, visit [the Pinecone console](https://app.pinecone.io/) to watch and wait for the status of your index being created to finish, then run the function again.

### Data

To add more data, add text files to the `/documents` folder. These can be text, markdown, or PDF files.