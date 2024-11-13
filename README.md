<div align="center">
  <a href="https://exfunc.com">
    <img src="https://img.shields.io/badge/Visit-exfunc.com-white" alt="Visit exfunc.com">
  </a>
</div>
<div>
  <p align="center">
    <a href="https://x.com/exfunchq">
      <img src="https://img.shields.io/badge/Follow%20on%20X-000000?style=for-the-badge&logo=x&logoColor=white" alt="Follow on X" />
    </a>
    <a href="https://www.linkedin.com/company/exfunc">
      <img src="https://img.shields.io/badge/Follow%20on%20LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="Follow on LinkedIn" />
    </a>
    <a href="https://discord.com/invite/58CBc3Kd">
      <img src="https://img.shields.io/badge/Join%20our%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Join our Discord" />
    </a>
  </p>
</div>

# Exfunc

## What is Exfunc?

[Exfunc](https://exfunc.com) is an API service for performing tasks on the web. With one line of code, you can fetch business reviews on Yelp, search properties on Zillow, or extract contact information from any company website. We take care of the rest from provisioning infrastructure to scaling browser automations. Check out our [documentation](https://docs.exfunc.com)!

## How to use it?

Check out the following resources to get started:
- [x] **API**: [Documentation](https://docs.exfunc.com)
- [x] **SDKs**: [Python](https://github.com/carvedai/exfunc-py), [Typescript](https://github.com/carvedai/exfunc-js)
- [ ] Want an SDK or Integration? Let us know by opening an issue.

### API Key

To use the API, you need to sign up on [Exfunc](https://app.exfunc.com/auth/signup) and get an API key.

## Using Python SDK

### Installation

```bash
pip install exfunc
```

### Search People on LinkedIn

```python
import os
from exfunc import Exfunc

exfunc = Exfunc(api_key=os.getenv("EXFUNC_API_KEY", ""))

response = exfunc.linkedin.search_people(request={
  "locations": ["United States"],
  "seniorities": ["c_suite"],
  "company_sizes": ["51-200"],
})
print(response)
```

## Using Node SDK

### Installation

```bash
npm add exfunc
```

### Get Tweet

```js
import { Exfunc } from "exfunc";

const exfunc = new Exfunc({
  apiKey: process.env["EXFUNC_API_KEY"] ?? "",
});

async function run() {
  const result = await exfunc.twitter.getTweet({
    tweetId: "<id>",
  });

  // Handle the result
  console.log(result);
}

run();
```

## Demo

https://github.com/user-attachments/assets/23e58739-4372-4d7a-92a0-225eec42a290
