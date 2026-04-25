# file-downloader
## GitHub Download Proxy

Download large files through GitHub's infrastructure. Perfect for bypassing download restrictions or unreliable connections.

## Available Methods

### Method 1: GitHub Artifacts (Temporary)
- **Workflow**: `fetch-artifact.yml`
- **Max size**: 2GB per file
- **Retention**: 1-90 days
- **Best for**: One-time downloads

### Method 2: GitHub Releases (Permanent)
- **Workflow**: `fetch-release.yml`
- **Max size**: Unlimited
- **Retention**: Forever
- **Best for**: Files you need to keep or share

## Quick Start

### Method 1: Download as Artifact (Temporary)
1. Go to **Actions** → **"Fetch File as Artifact"**
2. Click **"Run workflow"**
3. Enter:
   - **URL**: The file download link
   - **Filename**: Desired name (e.g., `hadoop-3.3.6.tar.gz`)
4. Click **"Run workflow"**
5. After completion, scroll down to **Artifacts** section
6. Click filename to download

### Method 2: Download as Release (Permanent)
1. Go to **Actions** → **"Fetch File as Release"**
2. Click **"Run workflow"**
3. Enter:
   - **URL**: The file download link
   - **Tag**: Version tag (e.g., `hadoop-3.3.6`)
   - **Filename**: Desired name (e.g., `hadoop-3.3.6.tar.gz`)
4. Click **"Run workflow"**
5. Go to **Releases** (right sidebar) to download

## Example Usage

```
URL: https://archive.apache.org/dist/hadoop/common/hadoop-3.3.6/hadoop-3.3.6.tar.gz
Filename: hadoop-3.3.6.tar.gz
Tag: hadoop-3.3.6
```

## Important Notes

- **Method 1** artifacts expire (default: 1 day)
- **Method 2** releases are permanent and shareable
- Default timeout: 10 minutes (adjust in workflow)
- Ensure the repository is public for artifact access
- Check `Settings → Actions → General → Workflow permissions` is set to **"Read and write"**

## Troubleshooting

### "Artifacts not showing"
- Workflow must complete successfully (green checkmark)
- Scroll to very bottom of workflow run page
- Check if retention period expired

### "Workflow failed"
- Verify URL is accessible
- Check for file size limits
- Increase timeout in workflow file

### "Permission denied"
- Go to **Settings → Actions → General**
- Enable **"Read and write permissions"**
- Rerun the workflow

## Workflow Files

```
.github/workflows/
├── fetch-artifact.yml    # Method 1: Temporary artifact download
└── fetch-release.yml      # Method 2: Permanent release download
```

## Privacy

Files are stored in your GitHub repository. Use private repos if downloading sensitive content.

## License

MIT - Use at your own risk. Respect copyright laws.

#Iraninternetblackout
#digitalblackoutlran
