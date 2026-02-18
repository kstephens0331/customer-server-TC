# Customer Server - Terracotta Construction

## Overview

A dedicated Express 5 email notification server built for the Terracotta Construction contact form. This lightweight service handles form submissions, validates input data, and dispatches email notifications via Nodemailer. Designed to run as a standalone microservice behind the Terracotta Construction client website.

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Runtime | Node.js |
| Framework | Express 5 |
| Email | Nodemailer |
| Security | CORS |
| Validation | Custom middleware |

## Features

- **Email Sending** -- Automated email dispatch to business inbox when customers submit the contact form
- **Form Validation** -- Server-side validation of name, email, phone, and message fields before processing
- **CORS Configuration** -- Restricted cross-origin access to authorized Terracotta Construction domains only
- **Error Handling** -- Structured error responses with meaningful status codes for the frontend
- **Lightweight Deployment** -- Minimal footprint server designed for single-purpose operation

## Getting Started

### Prerequisites

- Node.js 18+
- SMTP credentials (Gmail, SendGrid, or other provider)

### Installation

```bash
# Clone the repository
git clone https://github.com/kstephens0331/customer-server-TC.git
cd customer-server-TC

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env
# Edit .env with SMTP host, port, credentials, and recipient address

# Start the server
npm start
```

The server starts on the port defined in your environment configuration.

## Project Structure

```
customer-server-TC/
├── server.js                # Main Express application
├── routes/
│   └── contact.js           # Contact form submission endpoint
├── middleware/
│   └── validate.js          # Input validation middleware
├── utils/
│   └── mailer.js            # Nodemailer transport configuration
├── .env.example             # Environment variable template
├── package.json
└── README.md
```

## License

All rights reserved. Proprietary client project for Terracotta Construction.

---

**Built by StephensCode LLC**
