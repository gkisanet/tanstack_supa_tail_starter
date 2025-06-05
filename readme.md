# Connecting to Supabase with an Individual .env File

This manual explains why and how to set up an individual `.env` file to securely store connection settings for Supabase.

## Why Use a .env File?
- **Security**: Sensitive credentials such as API keys, URLs, and secret tokens are stored locally and not committed to version control.
- **Environment Separation**: Easily manage different environments (development, testing, production) by loading different configuration files.
- **Convenience**: Centralized configuration makes it easier to update connection settings without modifying your code.

## Setting Up Your .env File
1. **Create the .env file**:  
    In your project root (or another specified directory), create a file named `.env`.

2. **Add Supabase Configuration Variables**:  
    Insert the required Supabase connection details. For example:
    ```
    SUPABASE_URL=https://your-project.supabase.co
    SUPABASE_ANON_KEY=your-anonymous-key

    ```
    Replace the sample values with your actual Supabase credentials.

3. **Load .env File in Your Project**:
    - **Node.js**: Install the dotenv package:
      ```
      npm install dotenv
      ```
      Then add the following line at the beginning of your entry point:
      ```js
      require('dotenv').config();
      ```
    - **Other Environments**: Check the documentation to load environment variables appropriately.

## Best Practices
- **Do Not Commit .env**: Add `.env` to your `.gitignore` file to ensure that sensitive information is not uploaded to version control.
- **Environment Isolation**: Use separate .env files for different environments (e.g., `.env.development`, `.env.production`) and load them accordingly.
- **Regular Updates**: Periodically review your credentials and environment configurations to prevent potential security risks.

This approach ensures that sensitive connection settings for Supabase are managed securely and efficiently across various development environments.
