# Containerly

![Containerly](splash.png)

Containerly is a modern container deployment platform that makes it easy to deploy and manage containerized applications. Built with Next.js and Docker, it offers a seamless experience for developers to deploy their applications with just a few clicks.

## Features

- 🚀 One-click deployments
- 🔒 Secure container isolation
- 📊 Resource monitoring and management
- 👥 User authentication with Google
- 💳 Premium tier with expanded capabilities
- 🎯 Resource limits and quotas
- 🔄 Container lifecycle management

## Architecture

The application is built using:

- **Frontend**: Next.js 14 with React
- **Backend**: Node.js with Docker API integration
- **Authentication**: NextAuth.js with Google provider
- **Styling**: Tailwind CSS
- **State Management**: React Hooks
- **Monitoring**: Real-time Docker stats

## Resource Limits

Free and Premium tiers have different container limits:
```javascript
const CONTAINER_LIMITS = {
FREE: 3,
PREMIUM: 10
};
```

Container sizes and their resource allocations:
```javascript
javascript
const RESOURCE_LIMITS = {
small: {
memory: '16m',
cpus: '0.1'
},
medium: {
memory: '32m',
cpus: '0.2'
},
large: {
memory: '64m',
cpus: '0.4'
}
};
```
## Screenshots

### Dashboard
![Dashboard View](dashboard.png)

### Admin Panel
![Admin Panel](admin.png)

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/yourusername/containerly.git
cd containerly
```

2. Install dependencies:
```bash
npm install
```

3. Configure environment variables:
```bash
cp .env.example .env.local
```

4. Start the development server:
```bash
npm run dev
```

5. Open [http://localhost:3000](http://localhost:3000) in your browser.

## Docker Setup

The application can be deployed using Docker Compose:

```bash
docker-compose up -d
```

This will start:
- Nginx reverse proxy
- Containerly application
- Docker-in-Docker service for container management

## Security

Containerly implements several security measures:

- Container isolation with resource limits
- No privileged access
- Secure environment variable handling
- Rate limiting
- CSRF protection

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

For support, email support@containerly.app or open an issue in the GitHub repository.
