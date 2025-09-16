# Environment Variables Configuration

## Create your .env file

Create a `.env` file in your BlogWebsite directory with the following content:

```
# MongoDB Database Connection
MONGODB_URI=mongodb://localhost:27017/blogDB

# For production (MongoDB Atlas), use:
# MONGODB_URI=mongodb+srv://username:password@cluster.mongodb.net/blogDB?retryWrites=true&w=majority

# Session Secret Key (for user authentication)
SESSION_SECRET=your-super-secret-session-key-here-make-it-long-and-random

# Server Configuration
PORT=3000

# Environment (development/production)
NODE_ENV=development
```

## What each variable does:

### 1. MONGODB_URI
- **Purpose**: Database connection string
- **Local**: `mongodb://localhost:27017/blogDB`
- **Production**: Your MongoDB Atlas connection string
- **Example**: `mongodb+srv://username:password@cluster.mongodb.net/blogDB?retryWrites=true&w=majority`

### 2. SESSION_SECRET
- **Purpose**: Secret key for encrypting user sessions
- **Important**: Make this long and random for security
- **Example**: `myblog-super-secret-key-2024-xyz789abc123`
- **Security**: Never share this key publicly

### 3. PORT
- **Purpose**: Port number for your server
- **Default**: 3000
- **Production**: Vercel will set this automatically

### 4. NODE_ENV
- **Purpose**: Environment type
- **Development**: `development`
- **Production**: `production`

## Security Notes:

- ✅ Never commit .env files to version control
- ✅ Keep your SESSION_SECRET private
- ✅ Use different secrets for development and production
- ✅ Make SESSION_SECRET at least 32 characters long
