# GitHub Personal Access Token Documentation

## Overview
This document contains information about the GitHub Personal Access Token (classic) created for n8n-heroku automation.

## Token Details
- **Token Name**: n8n-heroku-automation-token
- **Token Type**: Classic Personal Access Token
- **Scopes**: repo (Full control of private repositories)
- **Created Date**: September 11, 2025
- **Expiration**: 30 days (October 11, 2025)

## Token Value
**⚠️ SECURITY NOTICE**: The actual token value should be stored securely and never committed to this repository.

Token format: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

## Usage Instructions

### For Git Operations
```bash
# Use token as password for HTTPS Git operations
git clone https://username:TOKEN@github.com/ccoolavi/n8n-heroku.git
```

### For API Calls
```bash
# Use token in Authorization header
curl -H "Authorization: token YOUR_TOKEN" https://api.github.com/repos/ccoolavi/n8n-heroku
```

### For n8n Workflows
1. Store the token as an environment variable or credential in n8n
2. Use it in HTTP Request nodes for GitHub API calls
3. Set Authorization header: `Bearer YOUR_TOKEN`

## Security Best Practices

1. **Never commit the actual token to any repository**
2. **Store in environment variables**: Set as `GITHUB_TOKEN` in your environment
3. **Use secret management**: Store in secure credential managers
4. **Rotate regularly**: Regenerate tokens before expiration
5. **Monitor usage**: Check GitHub settings for token activity
6. **Revoke if compromised**: Immediately delete token if suspected compromise

## Steps to Regenerate Token

1. Go to GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. Click "Generate new token (classic)"
3. Set Note: `n8n-heroku-automation-token`
4. Select expiration period
5. Check `repo` scope for full repository access
6. Click "Generate token"
7. **Copy the token immediately** (it won't be shown again)
8. Update the token in all systems using it
9. Delete the old token

## Troubleshooting

- **403 Forbidden**: Check token scopes and expiration
- **401 Unauthorized**: Verify token format and validity
- **Token expired**: Generate a new token following the steps above

## Related Documentation

- [GitHub Personal Access Token Documentation](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
- [GitHub API Authentication](https://docs.github.com/en/rest/overview/other-authentication-methods)
- [n8n HTTP Request Node](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.httprequest/)

---

**Last Updated**: September 11, 2025  
**Created By**: Automated setup process
