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
![Package.json Configuration Example](https://i.ibb.co.com/x1zRStR/Screenshot-16.png)

---

### Step 2: Run the Command

To generate the TypeScript types, simply run the following command in your terminal:

```bash
npm run typegen
```

---

### Result

Once the command is executed successfully, you will see the following confirmation:

✅ **Generated TypeScript types for 15 schema types and 2 GROQ queries** in one file:  
`./src/sanity/types.ts`

---

This refined version is clearer, uses proper headings, and has a consistent structure! Let me know if you’d like further tweaks! 😊
