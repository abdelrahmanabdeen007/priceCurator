# PriceCurator SETUP Guide

## Google OAuth Setup
To set up Google OAuth for PriceCurator:  
1. Go to the Google Developer Console.  
2. Create a new project.  
3. Navigate to the "Credentials" tab.  
4. Click on "Create Credentials" and select "OAuth 2.0 Client IDs".  
5. Configure the consent screen and add the required scopes.  
6. Obtain your client ID and client secret.

## Local Development Setup
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/PriceCurator.git
   ```  
2. Install dependencies:  
   ```bash
   cd PriceCurator  
   npm install
   ```  
3. Start the local server:  
   ```bash
   npm start
   ``` 

## API Configuration
- Configure environment variables in a `.env` file based on `.env.example` provided in the repository.  
- Ensure all secrets are stored securely and not hardcoded.

## Environment Setup
- Ensure you have installed the following:  
  - Node.js (version X.X.X)
  - MongoDB (or your preferred database)
  
## Browser Support
PriceCurator supports the latest versions of:  
- Chrome  
- Firefox  
- Safari  
- Edge  

## Performance Optimization Tips
- Utilize lazy loading for images and assets.  
- Minimize bundle sizes with code splitting and tree shaking.  
- Leverage browser caching by setting appropriate HTTP headers.

## Testing Checklist
- Ensure the following are tested:  
1. Authentication flow  
2. All API endpoints  
3. UI responsiveness  
4. Browser compatibility  

## Common Issues and Solutions
- **Issue:** Google OAuth not working  
   **Solution:** Ensure that redirect URIs are properly set in the Google Developer Console.  
- **Issue:** Local server won't start  
   **Solution:** Check for port conflicts or missing dependencies.

## Deployment Preparation
- Run build command:  
   ```bash
   npm run build
   ```  
- Ensure that environment variables are set correctly on the production server.  
- Use a CI/CD pipeline for automatic deployment where possible.