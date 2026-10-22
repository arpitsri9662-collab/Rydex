<div align="center">

# 🚗 Rydex

### Your Ride. Your Route. Your Rydex.

**A modern ride-booking platform connecting riders, ride partners, and administrators through a seamless digital experience.**

[![Live Demo](https://img.shields.io/badge/🌐_Live_Demo-Visit_Rydex-2563EB?style=for-the-badge)](https://rydex-sepia.vercel.app/)
[![GitHub Repository](https://img.shields.io/badge/GitHub-Source_Code-181717?style=for-the-badge\&logo=github)](https://github.com/arpitsri9662-collab/Rydex)

<br />

[Live Application](https://rydex-sepia.vercel.app/) • [Source Code](https://github.com/arpitsri9662-collab/Rydex) • [Report an Issue](https://github.com/arpitsri9662-collab/Rydex/issues)

</div>

---

## 📖 About the Project

**Rydex** is a full-stack ride-booking web application designed to simplify the interaction between riders and ride partners.

The platform provides dedicated experiences for users, partners, and administrators. Riders can access ride-booking functionality, partners can manage their ride-related activities, and administrators can review partner applications, verify identities, and oversee platform operations.

Built with modern web technologies, Rydex combines responsive interfaces, authentication, database integration, real-time communication infrastructure, and payment integration to deliver a scalable foundation for a ride-booking service.

> 🎯 **Project Goal:** Build a full-stack ride-booking platform with role-based dashboards, partner verification, and streamlined ride management.

## ✨ Key Features

### 👤 User Dashboard

* User authentication and account access.
* Ride-booking workflow.
* Access to ride-related information and booking details.
* Personalized user experience.
* Responsive interface for different screen sizes.

### 🚘 Partner Dashboard

* Dedicated dashboard for ride partners.
* Partner onboarding and verification workflow.
* Video-based KYC submission and verification status.
* Ride-request management functionality.
* Vehicle-related information and management.

### 🛡️ Admin Dashboard

* Dedicated administrative interface.
* Review pending partner applications.
* Approve or reject partner applications.
* Review pending video KYC submissions.
* Review vehicle-related submissions.
* View dashboard statistics and earnings information.
* Secure logout functionality.

### 🔐 Authentication & Authorization

* Google OAuth authentication.
* Credentials-based authentication.
* Role-based access control.
* Protected dashboard pages.
* Server-side session verification.
* Role-aware access to administrative functionality.

### 📹 Video KYC

* Video-based identity verification workflow for partners.
* Administrative review of pending verification requests.
* Verification-status management.

### ⚡ Real-Time Communication

* Separate Socket.IO-compatible backend infrastructure for real-time application communication.
* Dedicated socket server for handling supported real-time events.
* Configurable frontend-to-backend connection.

### 💳 Payment Integration

* Razorpay integration for payment-related functionality.
* Environment-based configuration for sensitive payment credentials.

### ☁️ Deployment

* Frontend deployment using Vercel.
* Separate socket server deployment using Render.
* GitHub-based source-code management.
* Environment-variable configuration for deployment environments.

---

## 🖥️ Live Demo

**Try the deployed application:**

### 🌐 [Launch Rydex](https://rydex-sepia.vercel.app/)

Explore the application and its available features.

> **Note:** Some features may require authentication or the appropriate account role. Administrative and partner features depend on account permissions and configured backend services.

## 🛠️ Tech Stack

| Category                 | Technologies                        |
| ------------------------ | ----------------------------------- |
| Frontend                 | Next.js, React, TypeScript          |
| Styling                  | Tailwind CSS                        |
| Backend                  | Next.js API routes, Node.js         |
| Authentication           | Auth.js / NextAuth.js, Google OAuth |
| Database                 | MongoDB                             |
| ODM                      | Mongoose                            |
| Real-Time Infrastructure | Socket server, Express.js           |
| Payments                 | Razorpay                            |
| Media Storage            | Cloudinary                          |
| UI & Icons               | Lucide React                        |
| Deployment               | Vercel, Render                      |
| Version Control          | Git, GitHub                         |

---

## 🏗️ Application Architecture

Rydex separates its web application from its socket server to keep the deployment structure organized.

```text
                        ┌─────────────────────┐
                        │       RYDEX         │
                        │    Web Platform     │
                        └──────────┬──────────┘
                                   │
                        ┌──────────▼──────────┐
                        │      Next.js        │
                        │  React + TypeScript │
                        └──────────┬──────────┘
                                   │
                    ┌──────────────┼──────────────┐
                    │              │              │
             ┌──────▼─────┐ ┌──────▼─────┐ ┌─────▼──────┐
             │    User    │ │   Partner  │ │   Admin    │
             │  Dashboard │ │  Dashboard │ │ Dashboard  │
             └────────────┘ └────────────┘ └────────────┘
                                   │
                        ┌──────────▼──────────┐
                        │ Authentication &    │
                        │ Application APIs    │
                        └──────────┬──────────┘
                                   │
                   ┌───────────────┼───────────────┐
                   │               │               │
            ┌──────▼─────┐ ┌───────▼──────┐ ┌──────▼──────┐
            │  MongoDB   │ │   Razorpay   │ │  Cloudinary │
            │  Database  │ │   Payments   │ │ Media Store │
            └────────────┘ └──────────────┘ └─────────────┘

                        ┌────────────────────┐
                        │    Socket Server   │
                        │ Express + Node.js  │
                        └────────────────────┘
```

*Conceptual architecture illustrating the major components and integrations. Actual request flows depend on the implementation of each feature.*

## 📂 Project Structure

The GitHub repository contains the Next.js application and the separate socket server.

```text
Rydex/
│
├── rydex/
│   ├── public/
│   ├── src/
│   │   ├── app/
│   │   │   ├── api/
│   │   │   ├── admin/
│   │   │   ├── partner/
│   │   │   └── user/
│   │   ├── components/
│   │   ├── lib/
│   │   ├── models/
│   │   └── auth.ts
│   ├── .gitignore
│   ├── package.json
│   └── ...
│
├── socketServer/
│   ├── package.json
│   ├── .gitignore
│   └── ...
│
└── README.md
```

*The directory tree is illustrative; individual filenames and routes may differ from the current repository.*

## 🚀 Getting Started

Follow these steps to run Rydex locally.

### Prerequisites

Install the following tools:

* [Node.js](https://nodejs.org/)
* [Git](https://git-scm.com/)
* [MongoDB](https://www.mongodb.com/)
* A code editor such as [Visual Studio Code](https://code.visualstudio.com/)

You may also need credentials for Google OAuth, Razorpay, and Cloudinary, depending on which features you want to test.

### 1. Clone the Repository

```bash
git clone https://github.com/arpitsri9662-collab/Rydex.git
```

Navigate to the repository:

```bash
cd Rydex
```

### 2. Set Up the Next.js Application

```bash
cd rydex
npm install
```

Create a `.env.local` file in the `rydex` directory.

Add the environment variables required by your application:

```env
# Database
MONGODB_URI=your_mongodb_connection_string

# Authentication
AUTH_SECRET=your_auth_secret
AUTH_GOOGLE_ID=your_google_oauth_client_id
AUTH_GOOGLE_SECRET=your_google_oauth_client_secret

# Socket Server
NEXT_PUBLIC_SOCKET_SERVER_URL=http://localhost:8000

# Cloudinary
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret

# Razorpay
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret
```

**Important:**

* These are example variable names. Match them to the variables actually referenced in your source code.
* Add any additional variables required by your implementation.
* Never commit `.env.local`, OAuth secrets, database credentials, or payment secrets to GitHub.
* Only expose variables with the `NEXT_PUBLIC_` prefix when they are safe to share with browser-side code.

Start the development server:

```bash
npm run dev
```

Open http://localhost:3000 in your browser.

### 3. Set Up the Socket Server

Open another terminal from the repository root:

```bash
cd socketServer
npm install
```

Configure the socket server's required environment variables according to its source code and deployment settings.

Start the socket server using its available development script:

```bash
npm run dev
```

If the project does not define a `dev` script, check `socketServer/package.json` and use the appropriate script.

The socket server is expected to run on port `8000` in the local configuration described for this project.

### 4. Verify the Application

Once both services are running:

1. Open the Next.js application.
2. Test the configured login methods.
3. Check the appropriate dashboard for each account role.
4. Test the available ride-booking workflows.
5. Verify partner KYC and administrative review features.
6. Confirm that the frontend can connect to the socket server.

---

## 🔑 Authentication & Role-Based Access

Rydex uses authentication and role-based authorization to separate the experiences of different account types.

| Role    | Access                                             |
| ------- | -------------------------------------------------- |
| User    | User-facing ride and account functionality         |
| Partner | Partner-facing ride and verification functionality |
| Admin   | Administrative review and management functionality |

Dashboard access should be validated on the server, not only through frontend redirects.

Administrative APIs must independently verify the authenticated user's role before allowing access to sensitive information or performing privileged actions.

## 🌍 Deployment

Rydex uses a split deployment architecture.

| Component               | Platform                                               |
| ----------------------- | ------------------------------------------------------ |
| Next.js web application | [Vercel](https://vercel.com/)                          |
| Socket server           | [Render](https://render.com/)                          |
| Source code             | [GitHub](https://github.com/arpitsri9662-collab/Rydex) |

### Deployment Checklist

* Configure all required environment variables.
* Set the production MongoDB connection string.
* Register the correct Google OAuth redirect URI.
* Configure the production socket server URL.
* Add the deployed frontend origin to the socket server's CORS allowlist.
* Configure Razorpay credentials for the intended environment.
* Verify that protected routes and API endpoints enforce role-based authorization.
* Test the deployed application after each production release.

For Google OAuth, the callback URI generally follows this format:

```text
https://YOUR_DOMAIN/api/auth/callback/google
```

Use the actual deployed domain configured for your application.

## 🔒 Security Considerations

Security is essential for a ride-booking platform.

* Keep API secrets and database credentials out of source control.
* Enforce role-based authorization on protected API endpoints.
* Validate incoming requests on the server.
* Use secure session and cookie settings in production.
* Configure CORS to allow only trusted origins.
* Protect administrative operations from unauthorized access.
* Use HTTPS for production traffic.
* Use the appropriate Razorpay test or live credentials.
* Validate authentication and authorization after deployment.

## 🗺️ Future Enhancements

Potential areas for future development include:

* [ ] Live ride tracking on an interactive map.
* [ ] Real-time ride-request notifications.
* [ ] Improved ride-history and booking management.
* [ ] Partner earnings and analytics.
* [ ] Enhanced identity-verification workflows.
* [ ] Ride ratings and reviews.
* [ ] Improved mobile responsiveness and accessibility.
* [ ] Automated testing and CI/CD improvements.
* [ ] More comprehensive administrative analytics.

*These are potential enhancements, not claims that the features are already implemented.*

## 👨‍💻 Developer

**Arpit Srivastava**
Full Stack Developer | MERN Stack | Next.js

I enjoy building full-stack web applications that combine modern frontend experiences with secure backend systems, database integration, authentication, and scalable architecture.

* **GitHub:** [arpitsri9662-collab](https://github.com/arpitsri9662-collab)
* **Project Repository:** [Rydex](https://github.com/arpitsri9662-collab/Rydex)
* **Live Project:** [Rydex Web Application](https://rydex-sepia.vercel.app/)
* **Portfolio:** [Visit My Portfolio](https://my-portfolio-arpit9662.vercel.app/)
* **LinkedIn:** [Connect with Me](https://www.linkedin.com/in/arpit-srivastava-56a1872b1/)

## 🤝 Contributing

Contributions, suggestions, and feedback are welcome!

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test your implementation.
5. Submit a pull request describing your changes.

## 📄 License

No license has been specified here. If you intend to distribute this project for reuse, consider adding an appropriate `LICENSE` file to the repository.

---

<div align="center">

### 🚗 Rydex — Moving People, Connecting Journeys.

**Built with ❤️ by Arpit Srivastava**

[⭐ Explore the Repository](https://github.com/arpitsri9662-collab/Rydex) · [🌐 Visit the Live App](https://rydex-sepia.vercel.app/)

</div>
