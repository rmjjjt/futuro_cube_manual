## Starting scripts in the standard way

During debugging all scripts can be started by using shell commands. But at regular run, there are differences for **MyCube** scripts and scripts in **FLASH**. **MyCube** is a special case - it has a dedicated start and is repeating the **MENU GESTURE** in **GAME MENU**.

On the other hand, scripts in **FLASH** can have their own designed **ICON** placed on a specific side and menu, plus they can have their own sounds for name and explanations. This is achieved by adding **ICON** information into the script text file, which is compiled and later parsed by the cube and automatically set up in the menu. For details how to use it, look at the `ICON()` function in the API. In case no **ICON** is defined for the scripts that reside in **FLASH**, a new icon will appear in the **BLUE MENU** instead of **CONNECT GAME**, which will then start the script by selecting it in the standard way.

From FW 4.5 at multiple scripts, the environment is a slightly different situation. Scripts that have no **ICON** defined are placed in an extra **WHITE** menu with dice symbols 1 to 6.