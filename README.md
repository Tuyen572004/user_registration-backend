# NestJS Authentication Backend

This is a NestJS backend application implementing JWT-based authentication with access and refresh tokens, using PostgreSQL database.

## Features

- User registration and login
- JWT access and refresh token authentication
- Protected routes with guards
- Token refresh mechanism
- PostgreSQL database with TypeORM
- CORS enabled for frontend integration

## API Endpoints

- `POST /auth/register` - Register a new user
- `POST /auth/login` - Login user
- `POST /auth/refresh` - Refresh access token
- `POST /auth/logout` - Logout user (requires auth)
- `GET /profile` - Get user profile (requires auth)

## Setup

1. Install dependencies:
   ```bash
   npm install
   ```

2. Create `.env` file with:
   ```
   DATABASE_URL=postgresql://postgres:QgpKsMcynycBYtMPOjxOiIvtPSXEAkKm@tramway.proxy.rlwy.net:16029/railway
   JWT_ACCESS_SECRET=your_access_secret
   JWT_REFRESH_SECRET=your_refresh_secret
   PORT=3000
   CORS_ORIGIN=http://localhost:3000
   ```

3. Run the application:
   ```bash
   npm run start:dev
   ```

## Deployment to Railway

1. Sign up for Railway at https://railway.app

2. Install Railway CLI:
   ```bash
   npm install -g @railway/cli
   ```

3. Login to Railway:
   ```bash
   railway login
   ```

4. Initialize Railway project in the backend directory:
   ```bash
   cd backend
   railway init
   ```
   - Choose "Empty Project" or select Node.js if prompted.

5. Add PostgreSQL database:
   ```bash
   railway add postgresql
   ```
   - This will create a database and provide a `DATABASE_URL` environment variable.

6. Set environment variables in Railway:
   - Go to your Railway project dashboard.
   - In the "Variables" tab, add:
     - `JWT_ACCESS_SECRET`: A secure random string
     - `JWT_REFRESH_SECRET`: Another secure random string
     - `CORS_ORIGIN`: Your frontend URL (e.g., https://your-frontend.vercel.app)
     - `PORT`: 3000 (Railway sets this automatically, but confirm)

7. Deploy:
   ```bash
   railway up
   ```
   - This will build and deploy your application.

8. Get the deployment URL:
   - After deployment, Railway will provide a URL like `https://your-project.up.railway.app`

9. Update your frontend to use this backend URL.

## Environment Variables

- `DATABASE_URL`: PostgreSQL connection string
- `JWT_ACCESS_SECRET`: Secret for signing access tokens
- `JWT_REFRESH_SECRET`: Secret for signing refresh tokens
- `PORT`: Port to run the server (default 3000)
- `CORS_ORIGIN`: Allowed origin for CORS
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ npm install -g @nestjs/mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.

## Resources

Check out a few resources that may come in handy when working with NestJS:

- Visit the [NestJS Documentation](https://docs.nestjs.com) to learn more about the framework.
- For questions and support, please visit our [Discord channel](https://discord.gg/G7Qnnhy).
- To dive deeper and get more hands-on experience, check out our official video [courses](https://courses.nestjs.com/).
- Deploy your application to AWS with the help of [NestJS Mau](https://mau.nestjs.com) in just a few clicks.
- Visualize your application graph and interact with the NestJS application in real-time using [NestJS Devtools](https://devtools.nestjs.com).
- Need help with your project (part-time to full-time)? Check out our official [enterprise support](https://enterprise.nestjs.com).
- To stay in the loop and get updates, follow us on [X](https://x.com/nestframework) and [LinkedIn](https://linkedin.com/company/nestjs).
- Looking for a job, or have a job to offer? Check out our official [Jobs board](https://jobs.nestjs.com).

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://twitter.com/kammysliwiec)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).
