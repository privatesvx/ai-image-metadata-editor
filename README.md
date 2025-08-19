# AI Image Metadata Editor
A single-file, pure HTML tool for viewing and editing AI generated image metadata directly in your browser. No installation or internet connection required. The tool is primarily designed for reading and editing image metadata in the Automatic1111/Forge web UI format, though other common formats are partially supported.

## Demo
https://xypher7.github.io/ai-image-metadata-editor

## Usage
No need for prior setup, just open the HTML file with the web browser of your choice and drag an image file. Alternatively, you can use the version hosted on GitHub through the link provided above.

### Adding Checkpoint Resources
Large files greater than 2GB rely on the 3rd party library <a name="unique-anchor-name" href='https://www.npmjs.com/package/hash-wasm'>hash-wasm</a> due to serverless HTML limitations. Online connectivity is required to fetch the dependency. Optionally, if you wish to maintain everything local, you may download the <a name="unique-anchor-name" href='https://cdn.jsdelivr.net/npm/hash-wasm@4/dist/sha256.umd.min.js'>sha256.umd.min.js</a> file, place it in the same directory as the HTML file, and replace this line
```html
<script src="https://cdn.jsdelivr.net/npm/hash-wasm@4/dist/sha256.umd.min.js"></script>
```
 with 
```html
 <script src="sha256.umd.min.js"></script>
```

## Features
- **View metadata** from AI generated images.
- **Edit and save image metadata** in Automatic1111/Forge format. 
    - Metadata from other formats will be partially converted (basic info only).
- **Supported file types**: JPG, PNG, and WEBP.
- **Drag-and-drop support** for adding safetensors files as resources in metadata.
- **Resource links**: LoRA and Checkpoints automatically link to CivitAI.
- **Offline execution**: Runs entirely in your browser—no server, no external dependencies.

## Preview
![App Screenshot](https://image.civitai.com/xG1nkqKTMzGDvpLrqFT7WA/5b30fbe1-bbce-4e83-9b99-bcf11aa71ceb/original=true,quality=90/Screenshot%202024-09-29%20001102.jpeg)
