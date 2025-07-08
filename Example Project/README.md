# Example Project

This project is a modern React + TypeScript application bootstrapped with Vite. It demonstrates the use of a custom file uploader component, allowing users to upload, preview, and delete files with a user-friendly interface.

## 📺 Project Demo Videos

- **Full Project Overview:**  
  [Watch Example Project.mp4](./media/File%20Uploader%20Package.mp4)

## Features

- Drag & drop file upload and file selector support
- File type and size validation (supports `.jpg`, `.jpeg`, `.png`, `.txt`, `.pdf` up to 6MB)
- Duplicate file detection with overwrite confirmation
- Persistent storage using `localStorage`
- File deletion from preview and storage
- Responsive and accessible UI

## Project Structure

```
.
├── Example Project/                # Usage example consuming this plugin
│   ├── src/
│   │   ├── App.tsx                 # Demonstrates plugin usage
│   └── ...
├── src/                            # Source code for the file-uploader-plugin
│   ├── components/
│   │   ├── FilesSave.tsx
│   │   ├── PreviewFiles.tsx
│   │   └── RenderPreviewContent.tsx
│   └── index.tsx                   # Entry point of the plugin
├── rollup.config.mjs               # Bundler config for package build
├── package.json                    # Package metadata and dependencies
├── tsconfig.json                   # TypeScript configuration
├── README.md                       # You’re reading this!
└── .gitignore
```

## Usage

The main application imports the `file-uploader-plugin` package and renders it in [`App.tsx`](src/App.tsx):

```tsx
import FileUpload from 'file-uploader-plugin';

const App = () => (
  <FileUpload />
);

export default App;
```

## Installing the Local Plugin

To use the local version of the file uploader plugin instead of an npm-published version:

1. **Uninstall the npm package** from the main project:

  ```sh
  npm uninstall file-uploader-plugin
  ```

2. **Link the local package** by installing it directly from the local folder:

  ```sh
  npm install "../"
  ```

3. Now, the example project will use the local build of the package. Any changes you make to the package source code (in `File Uploader Package/src/`) should be followed by running the build script in the package directory:

  ```sh
  npm run build
  ```

4. After building, your changes will be reflected in the example project.

## Development Workflow for the Plugin

1. Edit the source files in file-uploader-package/src/

2. Build the plugin:

  ```sh
  cd ..
  npm install
  npm run build
  ```

3. Return to Example Project, and restart the dev server if needed

## License

This project and the file-uploader-plugin are licensed under the ISC License.

---

**Author:** Aman Sharma