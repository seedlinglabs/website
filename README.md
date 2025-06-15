# Seedling Labs Website

This repository contains the source code for the Seedling Labs website, which is automatically deployed to AWS S3 using AWS CodePipeline.

## Project Structure

```
.
├── src/               # Source files
│   └── index.html    # Main website file
├── buildspec.yml     # AWS CodePipeline build specification
└── README.md         # This file
```

## Local Development

1. Clone the repository
2. Open `src/index.html` in your browser to view the website locally

## Deployment

The website is automatically deployed to AWS S3 (seedlinglabs.com) using AWS CodePipeline. The deployment process:

1. Triggers on changes to the main branch
2. Builds the website using the specifications in `buildspec.yml`
3. Deploys the built files to the S3 bucket

## AWS Setup Requirements

1. S3 Bucket: `seedlinglabs.com`
   - Configured for static website hosting
   - Bucket policy allowing public read access
   - CloudFront distribution (optional, for HTTPS)

2. CodePipeline:
   - Source stage: GitHub repository
   - Build stage: AWS CodeBuild using `buildspec.yml`
   - Deploy stage: S3 bucket deployment

## Contributing

1. Create a new branch for your changes
2. Make your changes
3. Submit a pull request to the main branch
4. Once approved, the changes will be automatically deployed

## License

© 2025 Seedling Labs. All rights reserved.
