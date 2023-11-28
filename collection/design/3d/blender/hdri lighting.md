<br>

---

<br>


## Installing HDRIs

1. Open Preferences

`Edit > Preferences` or `Ctrl ,`

2. Open Lights Settings

3. Click Install button for HDRIs

4. Add the HDRI from an unzipped directory

<br>

---

<br>


## Shader Editor (Recommended)

Open the Shader Editor and set the shader type to "World".

Remove any existing shader (if necessary) and click the "New" button.

The Shader Editor should now look like this:

![[default-shader-editor.png]]

Press `Shift A` to add a new node and search for "Environment Texture".

Add the Environment Texture node and connect the `color` value to the `color` value on the Background node. 

![[hdri-environment-texture-node.png]]


(This should paint your scene a solid color when viewing in Rendered preview).

Select the Environment Texture node and press `Ctrl T` to add a mapping network.


![[hdri-mapping-node.png]]

Now add the HDRI file in the Environment Texture node by pressing the `Open` button and locating the desired hdr file.

To rotate the HDRI, change the `Z` axis rotation value in the Mapping node. 