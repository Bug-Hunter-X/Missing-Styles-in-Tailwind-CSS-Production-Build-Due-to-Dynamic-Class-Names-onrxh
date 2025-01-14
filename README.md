# Missing Styles in Tailwind CSS Production Build Due to Dynamic Class Names

This repository demonstrates a common issue encountered when using Tailwind CSS with frameworks utilizing server-side rendering (SSR) like Next.js or Nuxt.js.  The problem stems from Tailwind's PurgeCSS failing to identify dynamically generated class names, leading to missing styles in the production build.

The `bug.js` file showcases the issue: classes added based on conditional logic or runtime data are not included in the optimized CSS.  The `bugSolution.js` file provides a solution by configuring PurgeCSS to correctly handle these scenarios.

## Steps to Reproduce

1. Clone the repository.
2. Install dependencies using `npm install`.
3. Run the development server.
4. Observe the styles are correctly applied.
5. Build the application for production.
6. Note that the styles generated dynamically are missing.

## Solution

The solution involves adjusting the PurgeCSS configuration within your Tailwind CSS setup. Refer to `bugSolution.js` for an example of how to properly configure the PurgeCSS options to include dynamically generated classes.