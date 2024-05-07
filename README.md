# Open Sensor Library

## Requirements

- [Composer](https://getcomposer.org/)
- [Docker](https://www.docker.com/)
- [Node Version Manager](https://github.com/nvm-sh/nvm)
- [Node.js](https://nodejs.org/)
- [Sass](https://sass-lang.com/)

## Setup

1. Use the Node.js version specified in the `.nvmrc` file.

   ```sh
   nvm use
   ```

2. Install the dependencies.

   ```sh
   npm install
   composer install
   ```

3. Run the build.

   ```sh
   npm run build
   ```

4. Start the local development environment.

   ```sh
   docker-compose up -d
   ```

5. Open "http://localhost:8080/" in a web browser.

### Restoring from a backup

1. Move required files.

   - `mediawiki/LocalSettings.php`
   - `mediawiki/images/`

2. Import database.

   ```sh
   docker exec -i osl-database mysql -umediawiki -pmediawiki mediawiki < mysql.sql
   ```

   Replace `mysql.sql` with the path of the dump file.
