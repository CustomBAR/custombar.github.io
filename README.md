# CustomBAR

## Version 3.0.0

## Overview

CustomBAR is a 90s-styled progress bar designed for streamers on Rumble. It dynamically updates based on your follower count and displays your progress towards your goals.

## Installation

### Prerequisites

1. **Install Node.js**:
   - **Windows**:
     1. Visit the [Node.js download page](https://nodejs.org/).
     2. Download the Windows installer (`.msi`) for the LTS (Long-Term Support) version.
     3. Run the installer and follow the setup wizard. Make sure to check the box that says “Automatically install the necessary tools” to install `npm` along with Node.js.
     4. Once installed, you can verify the installation by opening Command Prompt and running:
        ```bash
        node -v
        npm -v
        ```
     - This will display the installed versions of Node.js and npm.

   - **macOS**:
     1. Visit the [Node.js download page](https://nodejs.org/).
     2. Download the macOS installer (`.pkg`) for the LTS version.
     3. Open the downloaded file and follow the instructions in the installer.
     4. After installation, open Terminal and run:
        ```bash
        node -v
        npm -v
        ```
     - This will display the installed versions of Node.js and npm.

   - **Linux**:
     1. Open Terminal.
     2. Update your package index:
        ```bash
        sudo apt update
        ```
     3. Install Node.js and npm:
        ```bash
        sudo apt install nodejs npm
        ```
     4. Verify the installation by running:
        ```bash
        node -v
        npm -v
        ```
     - This will display the installed versions of Node.js and npm.

### Setting Up CustomBAR

1. **Clone the Repository**:
    - Open Terminal or Command Prompt.
    - Run the following command to clone the repository:
      ```bash
      git clone https://github.com/tinyplayerss/custombar.git
      ```
    - Change into the project directory:
      ```bash
      cd custombar
      ```

2. **Install Dependencies**:
    - Run the following command to install the required Node.js packages:
      ```bash
      npm install
      ```
    - This will read the `package.json` file and install all necessary dependencies.

3. **Configure Your API Key**:
   - Open `server.js` in a text editor (e.g., VSCode, Sublime Text).
   - Find the line with `const externalApiUrl = 'YOUR_API_URL';` and replace `'YOUR_API_URL'` with your actual API URL.
   - You can find your API URL at `https://rumble.com/account/livestream-api`
   - Save the file.

4. **Start the Server**:
    - In Terminal or Command Prompt, run:
      ```bash
      npm start
      ```
    - This will start the server, and you should see output indicating that the server is running.

5. **Open Your Browser**:
   - Open a web browser and navigate to `http://localhost:3000` to view the progress bar.

## Integrating with OBS (Open Broadcaster Software)

To display the progress bar on your stream, follow these steps:

1. **Run the Local Server**:
    - Ensure that your server is running by executing `npm start`.

2. **Add a Browser Source in OBS**:
    - Open OBS Studio.
    - Click the `+` button in the "Sources" panel and select `Browser`.
    - Name the source (e.g., "Follower Progress Bar") and click `OK`.

3. **Configure the Browser Source**:
    - In the "URL" field, enter `http://localhost:3000`.
    - Set the width and height to match the dimensions of your progress bar (e.g., 600x150).
    - Click `OK` to add the source.

4. **Adjust the Layout**:
    - Position and resize the browser source in your OBS scene as needed.

## Troubleshooting

- **If the Progress Bar Does Not Load**:
    - Ensure the local server is running and accessible at `http://localhost:3000`.
    - Check for any errors in the browser console or the terminal running the server.

- **If the Progress Bar Is Not Updating**:
    - Check the API response by visiting `http://localhost:3000/api/followers` in your browser.
    - Verify that your API URL is correctly set and that there are no issues with the external API.

## License

This project is licensed under the MIT License.

## Contributing

Feel free to submit issues or pull requests if you have suggestions or improvements!

---

Happy streaming, and best of luck with your follower goals!

---
