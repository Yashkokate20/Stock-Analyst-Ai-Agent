# 🚀 Setup Guide - Stock Analyst AI Agent 

This guide will walk you through the complete setup process for the Stock Analyst AI Agent 2.0 workflow.

## 📋 Prerequisites Checklist

Before you begin, ensure you have the following:

- [ ] **n8n instance** (version 1.0 or higher)
- [ ] **Google Gemini API access** (Google AI Studio account)
- [ ] **Twelve Data API account** (free tier available)
- [ ] **Chart-IMG API account** (for professional charts)
- [ ] **Telegram Bot** (created via @BotFather)
- [ ] **Basic understanding** of n8n workflows and API integrations

## 🔑 API Keys & Credentials Setup

### 1. Google Gemini API Key

1. **Visit Google AI Studio**: Go to [https://ai.google.dev/](https://ai.google.dev/)
2. **Sign in** with your Google account
3. **Create API Key**: Click "Get API Key" and create a new key
4. **Copy the key** - you'll need it for n8n credentials
5. **Set quotas**: Ensure your API has sufficient quota for requests

**Important**: Store this key securely and never commit it to version control.

### 2. Twelve Data API Key

1. **Visit Twelve Data**: Go to [https://twelvedata.com/](https://twelvedata.com/)
2. **Sign up** for a free account
3. **Navigate to API**: Go to your dashboard and find the API section
4. **Copy your API key** - the free tier allows 8 requests per minute
5. **Check limits**: Monitor your usage to avoid hitting rate limits

**Free Tier Limitations**:
- 8 requests per minute
- 800 requests per day
- Basic data access

### 3. Chart-IMG API Key

1. **Visit Chart-IMG**: Go to [https://chart-img.com/](https://chart-img.com/)
2. **Create account** and sign up
3. **Get API key** from your dashboard
4. **Note pricing**: Check their pricing for your usage needs
5. **Test access**: Make a test request to verify the key works

### 4. Telegram Bot Setup

1. **Open Telegram** and search for `@BotFather`
2. **Start conversation** with BotFather
3. **Create bot**: Send `/newbot` command
4. **Choose name**: Follow prompts to name your bot
5. **Get token**: Copy the bot token provided
6. **Set commands** (optional): Use `/setcommands` to set up bot commands

**Example Bot Commands**:
```
analyze - Analyze a stock (e.g., /analyze AAPL)
help - Show available commands
about - About this bot
```

## 🛠️ n8n Installation & Configuration

### Step 1: Import Workflow

1. **Open n8n**: Navigate to your n8n instance
2. **Go to Workflows**: Click on "Workflows" in the sidebar
3. **Import**: Click "Import from file" button
4. **Select file**: Choose `Stock_analyst_Ai_Agent_2_0.json`
5. **Import**: Click "Import" to add the workflow

### Step 2: Configure Credentials

#### Google Gemini Credentials

1. **Navigate to Credentials**: Go to Settings > Credentials
2. **Add Credential**: Click "Add Credential"
3. **Select Type**: Choose "Google Gemini API"
4. **Configure**:
   - **Name**: `Google Gemini(PaLM) Api account`
   - **API Key**: Paste your Google Gemini API key
5. **Save**: Click "Save" to store the credential

#### Telegram Bot Credentials

1. **Add new credential**: Click "Add Credential"
2. **Select Type**: Choose "Telegram Bot API"
3. **Configure**:
   - **Name**: `Telegram account`
   - **Access Token**: Paste your bot token from BotFather
4. **Save**: Click "Save"

### Step 3: Update API Keys in Workflow

#### Twelve Data API Key

1. **Open workflow**: Navigate to the imported workflow
2. **Find node**: Locate "Twelve URL Generator" node
3. **Edit node**: Click to open the node editor
4. **Update system message**: Replace the API key in the system message:
   ```
   🔑 Here's the Twelve Data API Key: 
   YOUR_TWELVE_DATA_API_KEY_HERE
   ```
5. **Save**: Click "Save" to update the node

#### Chart-IMG API Key

1. **Find node**: Locate "CHART IMAGE GENERATION" node
2. **Edit node**: Click to open the node editor
3. **Update headers**: In the header parameters, update:
   - **Header Name**: `x-api-key`
   - **Value**: `YOUR_CHART_IMG_API_KEY_HERE`
4. **Save**: Click "Save"

### Step 4: Configure Webhook URLs

1. **Check webhook nodes**: Ensure all webhook URLs are correctly configured
2. **Update if needed**: If you're using a different n8n instance, update webhook URLs
3. **Test webhooks**: Use the "Test" button in each webhook node

### Step 5: Activate Workflow

1. **Toggle Active**: Click the "Active" switch at the top of the workflow
2. **Check status**: Ensure the workflow shows as "Active"
3. **Monitor**: Watch for any error messages or issues

## 🧪 Testing Your Setup

### Test 1: Basic Telegram Response

1. **Open Telegram**: Go to your bot's chat
2. **Send test message**: Type any stock symbol (e.g., `AAPL`)
3. **Check response**: You should receive both a chart and analysis
4. **Verify timing**: Response should arrive within 10-30 seconds

### Test 2: Different Stock Symbols

Test with various symbols:
- **US Stocks**: `AAPL`, `GOOGL`, `MSFT`
- **International**: `TATAMOTORS.BSE`, `TSLA`
- **Invalid symbols**: Test error handling

### Test 3: Multiple Requests

1. **Send multiple requests**: Test rate limiting
2. **Check all responses**: Ensure all requests are processed
3. **Monitor logs**: Check n8n execution history

## 🔍 Troubleshooting Common Issues

### Issue 1: Workflow Not Triggering

**Symptoms**: No response from Telegram bot
**Solutions**:
- Check webhook configuration
- Verify bot token is correct
- Ensure workflow is active
- Check n8n logs for errors

### Issue 2: API Rate Limits

**Symptoms**: "Rate limit exceeded" errors
**Solutions**:
- Upgrade Twelve Data plan
- Implement request throttling
- Add retry logic with delays
- Monitor API usage dashboard

### Issue 3: Chart Generation Fails

**Symptoms**: No chart image sent
**Solutions**:
- Verify Chart-IMG API key
- Check JSON format in "CHART IMG JSON" node
- Test API endpoint manually
- Review Chart-IMG documentation

### Issue 4: AI Analysis Errors

**Symptoms**: Empty or error responses from Gemini
**Solutions**:
- Check Google Gemini API quota
- Verify API key permissions
- Test with simpler prompts
- Check for API service issues

## 📊 Monitoring & Maintenance

### Daily Monitoring

- **Check execution history** in n8n
- **Monitor API usage** across all services
- **Review error logs** for recurring issues
- **Test bot functionality** with sample requests

### Weekly Maintenance

- **Update API keys** if needed
- **Review rate limits** and upgrade if necessary
- **Check for n8n updates** and new features
- **Backup workflow configuration**

### Monthly Review

- **Analyze usage patterns** and optimize
- **Review API costs** and optimize plans
- **Update documentation** if workflow changes
- **Test disaster recovery** procedures

## 🔒 Security Best Practices

### API Key Security

- **Never commit API keys** to version control
- **Use environment variables** when possible
- **Rotate keys regularly** (quarterly)
- **Monitor for unauthorized usage**

### Webhook Security

- **Use HTTPS endpoints** only
- **Implement webhook verification** when possible
- **Monitor webhook logs** for suspicious activity
- **Limit webhook access** to trusted sources

### Data Privacy

- **Don't log sensitive data** in n8n
- **Implement data retention policies**
- **Use secure transmission** for all API calls
- **Comply with data protection regulations**

## 📈 Performance Optimization

### Workflow Optimization

- **Minimize API calls** where possible
- **Implement caching** for frequently requested data
- **Use async processing** for non-blocking operations
- **Optimize JSON processing** nodes

### API Optimization

- **Batch requests** when possible
- **Use appropriate intervals** for data fetching
- **Implement exponential backoff** for retries
- **Monitor response times**

## 🆘 Getting Help

### Documentation Resources

- **n8n Documentation**: [https://docs.n8n.io/](https://docs.n8n.io/)
- **Google Gemini API Docs**: [https://ai.google.dev/docs](https://ai.google.dev/docs)
- **Twelve Data API Docs**: [https://twelvedata.com/docs](https://twelvedata.com/docs)
- **Chart-IMG API Docs**: [https://chart-img.com/docs](https://chart-img.com/docs)

### Community Support

- **n8n Community**: [https://community.n8n.io/](https://community.n8n.io/)
- **GitHub Issues**: Report bugs and request features
- **Discord/Telegram**: Join project-specific channels

### Professional Support

- **Paid Support**: Consider paid support for production deployments
- **Custom Development**: Hire developers for custom modifications
- **Consulting**: Get professional advice for complex setups

## 🎯 Next Steps

Once your setup is complete:

1. **Customize analysis prompts** to match your needs
2. **Add additional stock exchanges** or data sources
3. **Implement portfolio tracking** features
4. **Add alert functionality** for price targets
5. **Create scheduled reports** for regular analysis

## 📋 Setup Checklist

Use this checklist to ensure everything is properly configured:

- [ ] n8n instance running and accessible
- [ ] Workflow imported successfully
- [ ] Google Gemini API key configured
- [ ] Twelve Data API key updated in workflow
- [ ] Chart-IMG API key configured
- [ ] Telegram bot created and token configured
- [ ] All credentials saved in n8n
- [ ] Webhook URLs configured correctly
- [ ] Workflow activated
- [ ] Basic functionality tested
- [ ] Error handling tested
- [ ] Performance optimized
- [ ] Security measures implemented
- [ ] Monitoring set up
- [ ] Documentation updated

---

**🎉 Congratulations!** Your Stock Analyst AI Agent 2.0 is now ready to provide intelligent market analysis through Telegram!
