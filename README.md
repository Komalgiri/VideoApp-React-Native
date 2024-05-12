# Video App

This React Native application allows users to browse and search for videos stored in a Supabase database. The app integrates video playback using the React Native Video component and fetches video data from Supabase.

## Features

- Browse a list of videos fetched from a Supabase database.
- Search for specific videos by title using the search bar.
- View video details and play videos directly within the app.

## Installation

To run this project locally on your machine, follow these steps:

### Prerequisites

- Node.js (v14.x or higher) and npm installed on your machine.
- Expo CLI (for React Native development) globally installed (`npm install -g expo-cli`).

### Clone the Repository

```bash
git clone https://github.com/your-username/video-app.git
cd video-app
```

### Install Dependencies

```bash
npm install
```

### Configure Supabase

1. Sign up or log in to [Supabase](https://supabase.io/) and create a new project.
2. Navigate to your project dashboard and locate your Supabase URL and public API key.
3. Replace `supabaseUrl` and `supabaseKey` in `App.js` with your Supabase URL and API key respectively.

### Set up the Database

1. Inside your Supabase project, navigate to the SQL editor or go to "SQL" in the left sidebar.
2. Create a table named `videos` with the following schema:

   ```sql
   CREATE TABLE videos (
     id SERIAL PRIMARY KEY,
     title TEXT,
     channel TEXT,
     description TEXT,
     likes INTEGER,
     video_url TEXT
   );
   ```

3. Insert video data into the `videos` table using SQL `INSERT` statements or the Supabase dashboard interface. Here are example `INSERT` commands for inserting 8 videos:

   ```sql
   INSERT INTO videos (title, channel, description, likes, video_url)
   VALUES
     (
      );

### Run the App

```bash
npm start
```

This will start the Expo development server. You can run the app on an iOS or Android simulator/emulator or scan the QR code with the Expo Go app on your mobile device.

## Project Structure

- `App.js`: Main entry point of the application containing the React Native components.
- `VideoPlayer.js`: Component for rendering and playing videos using `react-native-video`.
- `package.json`: Node.js configuration file with project dependencies and scripts.
- `node_modules/`: Directory containing npm packages installed for the project.
- `assets/`: Directory for static assets such as images or videos.

## Contributing

Contributions to this project are welcome! Feel free to open issues or pull requests for bug fixes, feature requests, or enhancements.

## License

This project is licensed under the [MIT License](LICENSE).

