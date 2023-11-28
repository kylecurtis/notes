
<br>

---

<br>

## Installing HDRIs

<br>

### Step 1: Open Preferences
Access the Preferences window through `Edit > Preferences` or by using the shortcut `Ctrl ,`. This is where you can customize Blender's settings to optimize your workflow.

<br>

### Step 2: Open Lights Settings
Navigate to the Lights section. This area allows you to manage various lighting settings, crucial for achieving realistic renders.

<br>

### Step 3: Install HDRIs
Click the Install button for HDRIs. This step is about adding high-quality environmental textures to your scene, which significantly enhances realism and depth.

![[Preferences-Lights-Menu.png]]

<br>

### Step 4: Add HDRI from Directory
Add the HDRI from an unzipped directory. Ensure that your HDRI files are uncompressed and stored in an easily accessible location. This makes them readily available for your projects.

<br>

---

<br>

## Shader Editor (Recommended)

<br>

### Introduction
The Shader Editor is a powerful tool in Blender that allows for advanced manipulation of materials and textures. Setting the shader type to "World" affects the entire scene's environmental lighting.

<br>

### Step 1: Access and Prepare Shader Editor
Open the Shader Editor and set the shader type to "World". If there's an existing shader, consider removing it for a fresh start. Click the "New" button to create a new world shader.

![Default Shader Editor Setup](default-shader-editor.png)

<br>

### Step 2: Add Environment Texture Node
Press `Shift A` to add new nodes. Search for and add an "Environment Texture" node. This node is key for implementing HDRI lighting, as it maps the HDRI onto your scene's environment.

![Environment Texture Node](environment-texture-node.png)

<br>

### Step 3: Connect Nodes
Connect the `color` output of the Environment Texture node to the `color` input on the Background node. This linkage allows your HDRI to illuminate the scene.

![HDRI Environment Texture Node Connection](hdri-environment-texture-node.png)

*Tip: At this stage, your scene should adopt a solid color in the Rendered preview, indicating that the HDRI is affecting the scene's lighting.*

<br>

### Step 4: Add Mapping Network
Select the Environment Texture node and press `Ctrl T` (ensure Node Wrangler addon is enabled for this shortcut) to add a mapping network. This network provides control over how the HDRI is projected onto the scene.

<br>

### Step 5: Load HDRI File
Open the HDRI file by clicking the `Open` button on the Environment Texture node. Navigate to your desired HDR file. The choice of HDRI can dramatically change the mood and realism of your scene.

![Loading HDRI](hdri-open.png)

<br>

### Step 6: Adjust HDRI Orientation
Modify the `Z` axis rotation in the Mapping node to rotate the HDRI. This step is crucial for aligning the HDRI's lighting and reflections with your scene's geometry and artistic vision.

![Adjusting HDRI with Mapping Node](hdri-mapping-node.png)

*Additional Tip: To adjust the intensity of the HDRI's light, tweak the Strength parameter in the Background node. This can help achieve the desired balance between realism and artistic style.*


<br>

---

<br>

### Troubleshooting Common Issues
- **HDRI Not Visible**: Ensure the Environment Texture node is properly connected. If the HDRI still doesn't appear, check if the file path to the HDRI is correct.
- **Lighting Looks Unrealistic**: Experiment with different HDRIs and adjust the Strength and Rotation settings. Each HDRI has unique characteristics that can vastly affect the scene.
