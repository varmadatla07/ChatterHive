# ChatterHive

A cutting-edge social networking platform that leverages advanced NLP-driven content moderation and adaptive context-based authentication. This system seamlessly blends user engagement with robust security measures, fostering a safe and dynamic online community while ensuring user privacy and account protection."
This statement highlights the key features (social networking, automated moderation, and advanced authentication) while emphasizing the benefits (safety, engagement, and privacy) in a more impactful way.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies](#technologies)
- [Schema Diagram](#schema-diagram)
- [Getting Started](#getting-started)
- [Usage](#usage)


## Project Overview

The project is a social networking platform built using the MERN (MongoDB, Express.js, React.js, Node.js) stack. It incorporates two major features: an automated content moderation system and context-based authentication. These features are accompanied by common functionalities found in social media applications, such as profile creation, post creation and sharing, liking and commenting on posts, and following/unfollowing users.

## Automated Content Moderation

- The platform uses various NLP APIs for content moderation:
  - Perspective API: Filters spam, profanity, toxicity, harassment, etc.
  - TextRazor API: Used for content categorization

- A Flask application provides similar functionality to the Hugging Face Interface API:
  - Uses the BART Large MNLI model
  - Operates as a zero-shot classification pipeline
  - Built with PyTorch framework

- The system allows flexibility in API usage:
  - Different services can be chosen or disabled without affecting overall functionality
  - Uses a common interface for API interactions

- Content filtering process:
  - User posts undergo thorough filtering for compliance with community guidelines
  - Users can report inappropriate posts, triggering manual review

## Context-Based Authentication

- Enhances user account security by considering:
  - User location
  - IP address
  - Device information

- Features:
  - Users can manage their devices directly on the platform
  - Data is encrypted using AES algorithm and securely stored

- Security measures:
  - Suspicious login attempts trigger email notifications
  - Users must confirm identity to prevent unauthorized access

## User Roles

1. Admin:
   - Manages overall system
   - Handles moderator management
   - Oversees community management
   - Performs content moderation
   - Monitors user activity

2. Moderators:
   - Manage communities
   - Manually review reported posts
   - Perform other moderation-related tasks

3. General Users:
   - Make posts
   - Like comments
   - Perform other platform-specific actions



## Features

### User Management
- [x] User authentication and authorization (JWT)
- [x] User profile creation and management
- [x] Following/unfollowing users
- [x] Device management

### Content Interaction
- [x] Post creation and management
- [x] Commenting on posts
- [x] Liking posts and comments
- [x] Reporting posts

### Moderation and Administration
- [x] Content moderation
- [x] Admin dashboard
- [x] Moderator dashboard

### Security
- [x] Context-based authentication

### Notifications
- [x] Email notifications


## Technologies

- React.js
- Redux
- Node.js
- Express.js
- MongoDB
- Tailwind CSS
- JWT Authentication
- Passport.js
- Nodemailer
- Crypto-js
- Flask


### Configuration

Run the `admin_tool.sh` script from the server directory with permissions for executing the script. This script is used for configuring the admin account, creating the initial communities, and other settings.
```bash
./admin_tool.sh
``` 

<!-- #### `.env` Variables

For email service of context-based authentication, the following variables are required:

```bash
EMAIL=
PASSWORD=
EMAIL_SERVICE=
``` -->
<!-- 
For content moderation, you need the `PERSPECTIVE_API_KEY` and either the `INTERFACE_API_KEY` or `TEXTRAZOR_API_KEY`. Visit the following links to obtain the API keys:

- [Perspective API](https://developers.perspectiveapi.com/s/docs-get-started)
- [TextRazor API](https://www.textrazor.com/)
- [Hugging Face Interface API](https://huggingface.co/facebook/bart-large-mnli) -->

<!-- If you prefer, the Flask server can be run locally as an alternative to using the Hugging Face Interface API or TextRazor API. Refer to the `classifier_server` directory for more information. -->

<!-- 
>**Note:** Configuration for context-based authentication and content moderation features are **_not mandatory_** to run the application. However, these features will not be available if the configuration is not provided. -->


## Usage

### Admin

The admin dashboard is accessible via the `/admin route`. To set up the admin account, utilize the admin_tool.sh script. This account allows for the management of moderators, communities, and various administrative tasks. Additionally, you can enable or disable API services and switch between them directly from the admin dashboard.

### Moderator

Moderators are identified by their specific email domain, which is `@mod.chatterhive.com`. When a user registers with an email from this domain, they are automatically granted the moderator role. From the admin dashboard, moderators can be assigned to different communities as needed.

## Entity Relationship Diagram 
  - **Eraser Link** : <a href="https://app.eraser.io/workspace/HF6RDbHxgGun03x0HS8p?origin=share" target="_blank">eraser.io</a>
    
## Demo of the Project: 
  - **Demo Link** : <a href="https://chatterhive-frontend.onrender.com/signin" target="_blank">demo</a>



