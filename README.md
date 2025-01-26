# typegen-next.js-15-and-sanity
i will show  you how to impliment typgen with next.js 15  and sanity cms


<h2>Generate TypeScript Types </h2>

<h3>Add Type-safety to your project and reduce the likelihood that you will write code that produces errors.</h3>

<p>In the case of working with Sanity TypeGen, it can create Types for Sanity Studio schema types and GROQ query results. So, as you build out your front end, you only access values within documents that exist, as well as defensively code against values that could be null.</p>

<h1>Extracting schema</h1>

<p>You're able to use the Sanity CLI from inside the Next.js application because of the sanity.cli.ts file at the root of your project.</p>

<h1>Run the following command in your terminal</h1>

```
npx sanity@latest schema extract --path=./src/sanity/extract.json

```

<h2>Re-run this every time you modify your schema types</h2>

<p>The --path argument is provided so the schema file is written to the same folder as all our other Sanity utilities.</p>

<p>You should see a response like the one below and a newly generated extract.json file in your src/sanity directory.</p>

<h1>✅ Extracted schema</h1>

<p>This file contains all the details about your Sanity Studio schema types, which TypeGen will need to create types from.</p>

<h1>Generating types</h1>

<p>By default, TypeGen will create a file for types at the project's root. Again, to keep Sanity-specific files colocated, we can preconfigure some defaults and keep the project root tidy.</p>

<h1>Create a new file at the root of your project</h1>

```
sanity-typegen.json

{
  "path": "./src/**/*.{ts,tsx,js,jsx}",
  "schema": "./src/sanity/extract.json",
  "generates": "./src/sanity/types.ts"
}

```

<h2>The configuration here will:</h2>

<p>Scan the src directory for GROQ queries to create Types.
Additionally, use the extract.json file created during the previous task.
Write a new types.ts file with our other Sanity utilities.</p>

<h2>Run the following command in your terminal</h2>

```
npx sanity@latest typegen generate

```

<h2>✅ Generated TypeScript types for 15 schema types and 2 GROQ queries in 1 files into: ./src/sanity/types.ts</h2>

