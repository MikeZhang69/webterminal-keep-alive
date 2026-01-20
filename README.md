# Webterminal Keep-Alive

This repository contains a GitHub Actions workflow that keeps the [Webterminal HuggingFace Space](https://huggingface.co/spaces/MikeZhang69/Webterminal) awake 24/7.

## What it does

The workflow sends a ping to the HuggingFace Space every 10 minutes using HTTP requests, preventing the space from going to sleep due to inactivity.

## Workflow Details

- **Schedule**: Runs every 10 minutes (`*/10 * * * *`)
- **Trigger**: Automatic schedule + manual trigger option
- **Action**: Sends an HTTP request to the HuggingFace Space URL

## Repository Structure

```
.
├── .github/
│   └── workflows/
│       └── keep-alive.yml    # GitHub Actions workflow
└── README.md                 # This file
```

## Setup Instructions

1. Repository was cloned and workflow added automatically
2. Enable GitHub Actions in the repository settings
3. The workflow will start running automatically

## Monitoring

You can monitor the workflow runs by:
- Visiting the "Actions" tab in this GitHub repository
- Checking the run history and logs
- Manually triggering the workflow if needed

## Benefits

- ✅ Prevents HuggingFace Space from sleeping
- ✅ Ensures 24/7 availability
- ✅ Free solution using GitHub Actions
- ✅ Automatic monitoring and retry logic

## Notes

- GitHub Actions provides free tier with 2,000 minutes/month
- Each ping takes less than 1 second, so well within limits
- If the workflow ever fails, it will retry automatically on the next scheduled run
