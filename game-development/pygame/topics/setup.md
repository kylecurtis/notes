This step assumes that you have the latest version of python installed on your system (or any modern Python-3 version).

<br>

---

<br>


## 1. Open Terminal

To access your terminal or command prompt:

- **Windows**: Press `Win + R`, type `cmd`, then press `Enter`.
- **macOS**: Press `Cmd + Space`, type `Terminal`, and press `Enter`.
- **Linux**: Depending on your distro, you can open it from the menu, or press `Ctrl + Alt + T`.

<br>

---

<br>

## 2. Navigate to Your Project Location

Use the `cd` command to navigate to where you want your project to be:

```bash
cd C:\Users\Username\Documents\Projects
```

<br>

---

<br>

## 3. Create a New Project Folder

To create a new directory for your project:

```bash
mkdir my_pygame_project
```

<br>

---

<br>

## 4. Navigate into Your Project Folder

To navigate into your project folder:

```bash
cd my_pygame_project
```

<br>

---

<br>

## 5. Set up a Virtual Environment

Set up a virtual environment using the built-in `venv` module:

```bash
python3 -m venv venv
```

This will create a new folder named `venv` in your project folder.

<br>

---

<br>

## 6. Activate the Virtual Environment

- **Windows**: Activate the environment using:

    ```bash
    .\venv\Scripts\activate
    ```

- **Unix or MacOS**: Activate the environment using:

    ```bash
    source venv/bin/activate
    ```

Your shell prompt should now start with the name of the environment.

<br>

---

<br>

## 7. Install Pygame

With your virtual environment active, install Pygame:

```bash
pip install pygame
```

<br>

---

<br>

## 8. Test Pygame Installation

You can check your installation by running the following in your Python interpreter:

```python
import pygame
print(pygame.ver)
```

If Pygame is correctly installed, this will print out the version number without any errors.

<br>

---

<br>

## 9. Deactivate the Virtual Environment

Once you're done, you can deactivate the virtual environment by typing:

```bash
deactivate
```

Your terminal prompt should return back to normal, indicating the virtual environment is no longer active.

---

Your Pygame setup is now complete!