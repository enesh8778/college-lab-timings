COLLEGE LAB TIMINGS — HACKATHON STARTER

Files:
- site/index.html: website page
- site/styles.css: Microsoft-inspired styling
- site/data.json: sample lab timetable data
- .github/workflows/deploy.yml: automatic upload to Azure Storage on push to main

LOCAL PREVIEW:
Open site/index.html in a browser. If the browser blocks fetch() for data.json from a file URL, use VS Code Live Server or another local web server.

GITHUB SETUP:
1. Create a GitHub repository.
2. Upload all files and folders from this package (keep the .github folder).
3. In GitHub repository Settings > Secrets and variables > Actions, add:
   - AZURE_STORAGE_ACCOUNT = eneshstorage (or your actual storage account name)
   - AZURE_STORAGE_KEY = your storage account access key
4. Push/commit to the main branch. Open the Actions tab and check the workflow run.
5. Ensure Azure Static website hosting is enabled and the $web container is available.

SECURITY:
Store the storage key only in GitHub Actions secrets. Never put it in index.html, data.json, or any public file.
The workflow uploads only the ./site folder into $web.
Sample timetable entries are placeholders; replace them with accurate college schedule information.
