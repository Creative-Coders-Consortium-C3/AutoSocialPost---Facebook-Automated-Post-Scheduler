# AutoSocialPost - Facebook Automated Post Scheduler 📱

A powerful Python-based tool that helps you automate and schedule multiple Facebook posts (text/images) using Google Colab. Perfect for social media managers, content creators, and businesses who want to plan their Facebook content in advance.

## 📔 Quick Start

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1XzOS7M6ZQbtJ5FJZykNJlEJHHYlubVcJ?usp=sharing)

Click the "Open in Colab" button above to get started immediately with the notebook, or [click here](https://colab.research.google.com/drive/1XzOS7M6ZQbtJ5FJZykNJlEJHHYlubVcJ?usp=sharing) to open the notebook directly.

## 🌟 Features

- Schedule multiple posts (text or photos) automatically
- Support for custom time slots and intervals
- Automated image upload from Google Drive
- Post scheduling for up to 30 days in advance
- Custom timezone support
- Automatic cleanup of used images from Google Drive
- Detailed logging and error handling
- View all scheduled posts in one place

## 📋 Prerequisites

Before you begin, ensure you have:

1. A Facebook Developer Account and App
2. A Facebook Page (you need to be an admin)
3. Google Account (for Google Colab and Drive)
4. Facebook Access Token with necessary permissions:
   - `pages_show_list`
   - `pages_read_engagement`
   - `pages_manage_posts`
   - `pages_manage_metadata`

## 🚀 Setup Instructions

1. Open the notebook in Google Colab using the link above
2. Mount your Google Drive
3. Install required dependencies:
   ```python
   !pip install facebook-sdk pytz google-auth-oauthlib google-auth-httplib2 google-api-python-client
   ```

## 📝 Usage Guide

### 1. Authentication

- Enter your Facebook Access Token when prompted
- Select the Facebook Page you want to post to
- The tool will authenticate with Google Drive automatically

### 2. Content Type Selection

Choose between two post types:
- **Text Posts**: Simple text-based updates
- **Photo Posts**: Images uploaded from your Google Drive

### 3. For Photo Posts

Prepare your Google Drive:
1. Create a folder in Google Drive for your images
2. Copy the folder ID (from the URL)
3. Have your images ready in the folder
4. Enter the folder ID when prompted

### 4. Scheduling Parameters

You'll need to provide:

| Parameter | Description | Example |
|-----------|-------------|---------|
| Posts per day | Number of posts to schedule daily | `3` |
| First post time | Start date and time | `2024-10-24 09:00` |
| Time gap | Minutes between posts | `120` |
| Total days | Number of days to schedule (max 30) | `7` |
| Timezone | Your local timezone | `US/Pacific` |
| Caption | Text for post or image caption | `"Check out our latest product!"` |

### 5. Post Management

The tool will:
- Schedule posts according to your parameters
- Delete used images from Drive (for photo posts)
- Display a summary of scheduled posts
- Show any failed scheduling attempts

## ⚠️ Limitations

- Maximum scheduling period is 30 days
- Minimum 20 minutes gap between current time and first post
- Rate limiting may apply based on Facebook's API restrictions
- Image posts must be from Google Drive URLs

## 🔍 Troubleshooting

Common issues and solutions:

1. **Invalid Access Token**
   - Ensure token has required permissions
   - Generate a new token if expired

2. **Failed Image Upload**
   - Check image format (JPG/PNG recommended)
   - Verify Drive folder permissions
   - Ensure images are under Facebook's size limits

3. **Scheduling Failures**
   - Check time gaps (minimum 20 minutes from now)
   - Verify page permissions
   - Check API rate limits

## 📊 Logging

The tool provides detailed logs for:
- Authentication status
- Post scheduling attempts
- Image processing
- Error messages
- API responses

## 🤝 Contributing

Feel free to:
- Report issues
- Suggest improvements
- Submit pull requests

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Facebook Graph API
- Google Colab
- Google Drive API

---

Made with ❤️ for the Creative Coders Consortium (C³) community
