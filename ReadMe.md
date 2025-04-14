<h1 align="center"> 
🏊 Olympics Manager 🏊
</h1>
</p>
<p align="center"> 
  <a href="https://github.com/jkengineer42/Olympics-Manager">
    <img src="https://img.shields.io/github/contributors/jkengineer42/Olympics-Manager.svg?style=for-the-badge" alt="Contributors" /> </a>
  <a href="https://github.com/jkengineer42/Olympics-Manager">
    <img alt="Issues" src="https://img.shields.io/github/issues/jkengineer42/Olympics-Manager?style=for-the-badge">
    </a>
  <a href="https://github.com/jkengineer42/Olympics-Manager">
    <img alt="Forks" src="https://img.shields.io/github/forks/jkengineer42/Olympics-Manager.svg?style=for-the-badge"></a>
  <a href="https://github.com/jkengineer42/Olympics-Manager">
    <img alt="Stars" src="https://img.shields.io/github/stars/jkengineer42/Olympics-Manager.svg?style=for-the-badge"></a>
  <a href="https://raw.githubusercontent.com/jkengineer42/Olympics-Manager/master/LICENSE">
    <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" alt="License" /> </a>
</p>

## Table of Contents

* [About The Project](#about-the-project)
  * [Built With](#built-with)
* [Installation and usage](#installation-and-usage)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [Usage](#usage)
  * [Features](#features)
  * [Athlete Data Files](#athlete-data-files)
  * [Demo Data](#demo-data)
* [Contributors](#contributors)
* [License](#license)


## About The Project

**Olympics Manager** (`CER-J-O MANAGEMENT`) is a program written in C designed to help coaches monitor and analyze their athletes' performances. Coaches can record new training sessions and evaluate progress using advanced statistical tools.

The application allows for managing multiple athletes, tracking their performance across various events over time, and provides insights into their progress and ranking.

### Built With

*   **Language:** C
*   **Standard Libraries:**
    *   `stdio.h`
    *   `stdlib.h`
    *   `string.h`
    *   `unistd.h`
    *   `sys/ioctl.h` (Likely for `system("clear")` or terminal size - may vary)
    *   `errno.h`
    *   `float.h`
    *   `ctype.h`
    *   `stdbool.h`
    *   `dirent.h` (For loading athlete files from the directory)
*   **Custom Headers:**
    *   `function.h`
    *   `file.h` (Implied - handles file operations)

## Installation and usage

Follow these steps to get the Olympics Manager running on your system.

### Prerequisites

*   A C compiler (like GCC) installed on your system.
*   The standard C libraries listed under [Built With](#built-with).

### Installation

1.  Clone the repository (if applicable) or ensure all source files (`main.c`, `functions.c`, `file.c`, `function.h`, `file.h`, etc.) are in the same directory.
2.  Open your terminal in the project directory.
3.  Compile the program using GCC:
    ```bash
    gcc -o main main.c functions.c file.c -I.
    ```
    *Note: Ensure `functions.c` and `file.c` contain the implementation for the functions declared in their respective header files.*

### Usage

1.  **Run the program:**
    Execute the compiled program from your terminal:
    ```bash
    ./main
    ```
2.  **Navigate the Menu:**
    Upon launching, you'll see the main menu:
    ```
    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    

                 CER-J-O MANAGEMENT 

    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    °ₒ°ₒ°    

    1. Ajouter un nouvel athlète
    2. Ajouter une performance pour un athlète
    3. Consulter l'historique des entraînements
    4. Consulter les statistiques sur les athlètes
    5. Quitter
    =====================================
    Entrez votre choix: 
    ```
    Enter the number corresponding to the action you want to perform.

3.  **Follow Prompts:** The program will guide you through each selected option, asking for necessary information like athlete names, dates, event types, and times.

### Features

The program offers the following functionalities accessible via the main menu:

1.  **Ajouter un nouvel athlète:**
    *   Allows adding a new athlete by name. Creates a corresponding `.txt` file.
    *   Prevents adding an athlete if a file with that name already exists.
2.  **Ajouter une performance pour un athlète:**
    *   Adds a new performance record (date, event type, time, relay position if applicable) to an existing athlete's file.
    *   Includes validation for date format, time input, and relay position.
3.  **Consulter l'historique des entraînements:**
    *   Search and display performance history based on athlete name, date, or event type.
4.  **Consulter les statistiques sur les athlètes (Advanced Stats Menu):**
    *   **Afficher la progression d'un athlète:** Compare an athlete's performance between two specific dates for a given event.
    *   **Afficher les statistiques d'un athlète pour une épreuve:** Calculate and display the best, worst, and average time for an athlete in a specific event.
    *   **Qui envoyer au JO?:** Identify and display the top 3 athletes for a given event based on their average performance times.
5.  **Quitter:** Exits the program.

### Athlete Data Files

Athlete data is stored in individual text files named after the athlete (e.g., `leonardo.txt`). The program automatically loads data from any `.txt` files present in its execution directory upon startup.

**File Format:**

<img width="328" alt="Capture d’écran 2024-05-26 à 03 25 41" src="https://github.com/jkengineer42/CER-J-OManagement/assets/167258198/7c14f8b5-9370-4a25-894f-9465c5a8591d">

1.  **Line 1:** Athlete's Name
2.  **Line 2:** Total number of recorded performances.
3.  **Subsequent Lines (one per performance):**
    *   `Date (YYYY-MM-DD)`
    *   `Event Type` (e.g., `100m`, `400m`, `5000m`, `marathon`, `relais 4 x 400 m`)
    *   `Time (in seconds)` (float format)
    *   `Relay Position` (integer 1-4, or 0 if not a relay event)

### Demo Data

To help you get started and test the features, sample athlete files are provided:

*   `lorenzo.txt`
*   `leonardo.txt`
*   `fabrizio.txt`
*   `marco.txt`

Place these files in the same directory as the compiled `main` executable. The program will load them automatically.

## Contributors

*   **[@KUGANESAN Arun](https://www.github.com/)**
*   **[@KONDA-MOUGNONGUI Jérémie](https://www.github.com/jkengineer42)**
*   **[@BOUHOU Haytham](https://www.github.com/HAYTHAM2005)**

## License

Distributed under the MIT License. See `LICENSE` file for more information.
