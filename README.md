# PUML Preview Extension for Zed

This extension adds **PlantUML** preview to the [Zed code editor](https://zed.dev) from your `.puml` files.

## Features

- ▶️ One-click diagram preview via a built-in task
- 📁 Automatic output to `.uml/` directory in your project root

## Requirements

- **Java Runtime Environment (JRE)** installed and available in your system `PATH`
- **PlantUML JAR file** — download it from the [official PlantUML website](https://plantuml.com/download)
- Set the environment variable `PLANTUML_JAR_PATH` to point to your downloaded `.jar` file  
  Example (in your shell config like `.bashrc`, `.zshrc`, etc.):
  ```sh
  export PLANTUML_JAR_PATH="$HOME/tools/plantuml.jar"
  ```

## Usage

1. Open a `.puml` file in Zed.
2. Press `Alt + Shift + T` to open the tasks window.
3. Run the task: **“preview”**  
   This will:
   - Render your diagram as a PNG
   - Save it to `$ZED_WORKTREE_ROOT/.uml/` (i.e., a hidden `.uml` folder in your project root)
   - Show progress in the terminal panel
   - Auto-hide the panel on successful generation

> 💡 Tip: You can bind this task to a custom keybinding in Zed’s settings for even faster access.

## Output Location

Generated diagrams are saved as:
```
<your-project-root>/.uml/<filename>.png
```

You can open this `.png` file in any image viewer or embed it in documentation.
