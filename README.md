# Public Job Listings

This repository contains automatically updated job listings from Public's Workable API. The data is updated daily and can be accessed in two ways:

1. **Raw JSON Data:**
   - Production data: [workable_public_jobs.json](./workable_public_jobs.json)
   - Test data: [workable_public_jobs_test.json](./workable_public_jobs_test.json)

2. **Web Interface:**
   - Visit [https://your-username.github.io/workable-jobs-public](https://your-username.github.io/workable-jobs-public) to view the job listings in a user-friendly interface

## Data Format

Each job listing contains the following information:
```json
{
  "id": "string",
  "title": "string",
  "department": "string",
  "locations": ["string"],
  "shortlink": "string",
  "positionType": "string",
  "workplaceType": "string",
  "description": "string",
  "requirements": "string",
  "benefits": "string"
}
```

## API Usage

The JSON files can be accessed directly via GitHub's raw content URLs:

```javascript
const JOBS_URL = 'https://raw.githubusercontent.com/your-username/workable-jobs-public/main/workable_public_jobs.json';

async function fetchJobs() {
    const response = await fetch(JOBS_URL);
    const jobs = await response.json();
    return jobs;
}
```

## Updates

This repository is automatically updated daily at 1 AM UTC through a GitHub Actions workflow in the private repository.

## License

This data is provided for public use but remains subject to Public's terms and conditions.
