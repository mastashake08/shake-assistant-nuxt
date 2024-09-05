
# Nuxt Prompt App

A simple Nuxt.js application that uses the JavaScript `prompt` API to display a dialog with a user-defined message. This app includes a custom component styled with TailwindCSS, allowing users to enter a message and display it using the browser's native prompt dialog.

## Features

- Custom Vue component with a text input and a button.
- Utilizes the JavaScript `prompt` API to display a dialog box.
- TailwindCSS for styling and responsive design.

## Prerequisites

- [Node.js](https://nodejs.org/) (v12.x or later)
- [npm](https://www.npmjs.com/) (v6.x or later)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/nuxt-prompt-app.git
   cd nuxt-prompt-app
   ```

2. Install the dependencies:

   ```bash
   npm install
   ```

## Usage

1. Start the development server:

   ```bash
   npm run dev
   ```

2. Open your browser and navigate to `http://localhost:3000` to see the app in action.

## Component Details

The `PromptComponent` allows users to:

- Enter a message in the text box.
- Click the "Show Prompt" button to display the JavaScript `prompt` dialog with the entered message.
- View the output of the `prompt` dialog below the button.

### Example Usage

To use the `PromptComponent`, simply add it to any page or component:

```vue
<template>
  <div class="container mx-auto my-8">
    <PromptComponent />
  </div>
</template>

<script>
import PromptComponent from '@/components/PromptComponent.vue';

export default {
  components: {
    PromptComponent,
  },
};
</script>
```

## TailwindCSS Configuration

This project uses TailwindCSS for styling. To customize the styles:

1. Edit the `tailwind.config.js` file.
2. Add or modify styles in `assets/css/tailwind.css`.

## Build for Production

To build the app for production:

```bash
npm run build
```

## Deployment

After building the app, deploy the contents of the `dist/` directory to your preferred hosting platform.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgements

- [Nuxt.js](https://nuxtjs.org/)
- [TailwindCSS](https://tailwindcss.com/)
```

### Key Sections Included

- **Project Title and Description**: Provides a brief overview of what the project does.
- **Features**: Lists the main features of the application.
- **Prerequisites**: Specifies the required versions of Node.js and npm.
- **Installation and Usage**: Step-by-step instructions to clone, install dependencies, and run the project.
- **Component Details**: Details on how to use the main `PromptComponent`.
- **TailwindCSS Configuration**: Instructions on how to modify the styling.
- **Build and Deployment**: Guidelines for building and deploying the app.
- **Contributing**: How to contribute to the project.
- **License and Acknowledgements**: Credits to the tools and frameworks used.
