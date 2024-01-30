# datafun-04-jupyter
This repository contains the resources and instructions for starting a new Python project with a virtual environment.
## How to Install and Run the Project

To set up and run the project locally, follow these steps:

1. **Create and Activate the Virtual Environment:**
   - Open your Project folder in the terminal (PowerShell or Command Prompt).
   - Create a virtual environment named `.venv` by running:
     ```
     python -m venv .venv
     ```
   - Activate the virtual environment:
     - On Windows:
       ```
       .\.venv\Scripts\Activate
       ```
     - On macOS and Linux:
       ```
       source .venv/bin/activate
       ```

2. **Install Dependencies:**
   - Choose one of the following options based on your preference:
   
     - **Option 1: Install packages separately:**
       ```
       py -m pip install jupyterlab
       py -m pip install numpy
       py -m pip install pandas
       py -m pip install matplotlib 
       py -m pip install seaborn
       py -m pip install scipy
       ```
     
     - **Option 2: Install packages on one line:**
       ```
       py -m pip install jupyterlab numpy pandas matplotlib seaborn scipy
       ```
     
     - **Option 3: Install packages using requirements.txt:**
       - Create a file named `requirements.txt` in the root folder of your repository.
       - Add the following content to `requirements.txt`:
         ```
         jupyterlab 
         numpy 
         pandas
         matplotlib 
         seaborn 
         scipy
         ```
       - Install the packages listed in the requirements file with the following command:
         ```
         py -m pip install -r requirements.txt
         ```

3. **Run the Project:**
   - After installing the dependencies, you can now run your project using the appropriate commands.
   - Ensure your virtual environment is activated when running your project.
