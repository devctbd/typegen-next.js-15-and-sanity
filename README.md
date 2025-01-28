Here’s a cleaner and more polished version of your `README.md` content:

---

# Typegen with Next.js 15 and Sanity CMS

This guide demonstrates how to implement TypeScript type generation (`typegen`) with Next.js 15 and the latest version of Sanity CMS.

---

## Generate TypeScript Types

### Step 1: Extracting the Schema

Add the following command to the `scripts` section of your `package.json` file:

```json
"typegen": "sanity schema extract --path=./src/sanity/extract.json && sanity typegen generate"
```

Example screenshot for reference:  
![Example screenshot for reference](https://i.ibb.co.com/x1zRStR/Screenshot-16.png)

---

### Step 2: Generate TypeScript Types

create a new json file in your root directory:

```bash
sanity-typegen.json
```

```json
{
  "path": "./src/**/*.{ts,tsx,js,jsx}",
  "schema": "./src/sanity/extract.json",
  "generates": "./src/sanity/types.ts"
}
```

### Step 3: Run the Command

To generate the TypeScript types, simply run the following command in your terminal:

```bash
npm run typegen
```

---

### Result

After successfully executing the command, you will receive the following confirmation:

✅ **TypeScript types generated for 15 schema types and 2 GROQ queries** in a single file:  
`./src/sanity/types.ts`

---

This version improves clarity, maintains proper headings, and ensures a consistent structure. Feel free to ask for additional changes! 😊
