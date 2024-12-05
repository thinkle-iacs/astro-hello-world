# Getting Started: File Structure and Running in Debug Mode

[Back to Overview](../README.md) | [Next: Your first change](./2-first-change.md)

## Project Structure Overview

Understanding the project structure is key to making changes effectively. 
First, a warning: this project has a *lot* of folders! I haven't hidden any of the folders from you this time because as you troubleshoot the various phases of the project, you made need access to all the different configuration files that help your project run. That said, you can *ignore* most files and folders here: if a folder or file starts with a `.`, that's a sign it's what's called a "configuration file" and probably can be ignored for now.

Here’s a breakdown of the files you need:

### `src/` Folder

- **Purpose**: Contains all your source code—the heart of your project.

### `src/pages/` Folder

- **Purpose**: Contains the source code for each page in your website.
- **Details**: Subfolders here will create subdirectories in your website.
  - Example: The `index.astro` file is the root page of your site.

### `src/components/` Folder

- **Purpose**: Contains reusable components that you can import into pages.
- **Details**: To start with, we have a Page component, which contains all the basic
  required HTML elements around your page and should be on every page. Then we also have
  a Project component with the idea that you'd have a template for each project you highlight
  on your portfolio.

  ### `src/styles/styles.css`

  This file is *imported* in your `main.js` file which is built with vite, a system which can bundle various libraries into your final
  website code.

  You can write CSS directly in this file if you learn some CSS for this
  project, or if libraries require you to add CSS import statements, you
  can add them to this file so your site will build correctly.


### `public/` Folder
- **Purpose**: Contains static assets like images, fonts, and other files that you might want to reference in your project. This folder will not be "built" or "bundled" but rather the files will simply be referenced directly at the base URL of your project.

## Running the Project to Test It

You should be able to run your project by hitting "Launch Astro" from the Run and Debug side-panel.

If that fails, you can go to a terminal and run:

```sh
npm run dev
```

Note: this assumes you're in a Github Codespace and everything got installed correctly.
If not, try going to the terminal and running:

```sh
npm install
```

## The other folders and files

Here's an overview of the rest of the file structure:

### `dist/` Folder
- **Purpose**: Contains the output from the Astro build process.
- **Details**: This folder is generated when you run `npm run build`. It includes all the compiled assets ready for deployment. It should never be added to version control.

### `node_modules/` Folder
- **Purpose**: Contains all the npm packages that your project depends on.
- **Details**: This folder is populated when you run `npm install` and should not be modified manually.

### `.github/workflows/` Folder
- **Purpose**: Contains GitHub Actions configurations for Continuous Integration (CI) and Continuous Deployment (CD).
- **Details**: For example, `deploy.yml` automates the process of deploying your built site to GitHub Pages.

### `.vscode/` Folder
- **Purpose**: Contains configurations for Visual Studio Code (the editor you're using in Github Codespaces), such as settings, extensions, and debug configurations.
- **Details**: Helps maintain consistency in development settings across different environments.

### `astro.config.mjs` and `vite.config.js`
- **astro.config.mjs**: The main configuration file for Astro, where you can set global configurations for your project. Astro is the site generator that creates HTML files based on your source code.
- **vite.config.js**: Configuration file for Vite, which allows customization of the build process, such as defining plugins, modifying build outputs, and more. Vite helps you "bundle" JavaScript and CSS from various libraries into one project.

### `instructions/` Folder
- **Purpose**: Contains markdown files that provide guidance and instructions for using the project, such as the one you're reading now.
- **Tip**: If you click on a markdown file, you'll see the source code for it, which just looks like text. If you click on the "Preview" icon (it looks like a two-page book with a magnifying glass), it will open the "pretty" version of the rendered markdown.
